
# Results vs. 3.11.0

- fork: python
- ref: 594de165bf2f21d6b28e
- machine: windows-amd64
- commit hash: 594de16
- commit date: 2022-11-28
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 193 ms: 1.06x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.45 ms: 1.16x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 57.1 ms: 1.24x faster                                                       |
| float          | 53.3 ms                                                                  | 48.3 ms: 1.10x faster                                                       |
| pidigits       | 147 ms                                                                   | 150 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 79.4 ms: 1.13x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.1 ms: 1.04x slower                                                       |
| regex_dna      | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.36 ms: 1.44x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 121 us: 1.23x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 176 us: 1.15x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 33.7 ms: 1.09x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.61 us: 1.07x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 49.2 ms: 1.06x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 88.8 ms: 1.04x faster                                                       |
| unpickle             | 8.01 us                                                                  | 7.78 us: 1.03x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.2 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 60.8 ms: 1.02x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.81 us: 1.05x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.85 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.9 ms: 1.24x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.0 ms: 1.19x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.14 ms: 1.17x faster                                                       |
| django_template | 23.9 ms                                                                  | 20.5 ms: 1.16x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.19x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.4 ns: 1.63x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.36 ms: 1.44x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 1.97 ms: 1.36x faster                                                       |
| richards                | 32.1 ms                                                                  | 23.8 ms: 1.35x faster                                                       |
| mypy2                   | 276 ms                                                                   | 215 ms: 1.29x faster                                                        |
| logging_silent          | 71.0 ns                                                                  | 56.7 ns: 1.25x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 20.3 us: 1.25x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 57.1 ms: 1.24x faster                                                       |
| genshi_text             | 17.3 ms                                                                  | 13.9 ms: 1.24x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 36.9 ms: 1.24x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 121 us: 1.23x faster                                                        |
| json                    | 3.20 ms                                                                  | 2.65 ms: 1.21x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 64.4 ms: 1.21x faster                                                       |
| fannkuch                | 255 ms                                                                   | 215 ms: 1.19x faster                                                        |
| genshi_xml              | 38.0 ms                                                                  | 32.0 ms: 1.19x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 61.0 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.24 ms: 1.18x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.14 ms: 1.17x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 900 ms: 1.17x faster                                                        |
| django_template         | 23.9 ms                                                                  | 20.5 ms: 1.16x faster                                                       |
| raytrace                | 206 ms                                                                   | 177 ms: 1.16x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 3.85 ms: 1.16x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.45 ms: 1.16x faster                                                       |
| go                      | 97.5 ms                                                                  | 84.3 ms: 1.16x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 443 ms: 1.16x faster                                                        |
| pickle_pure_python      | 203 us                                                                   | 176 us: 1.15x faster                                                        |
| scimark_lu              | 62.8 ms                                                                  | 55.0 ms: 1.14x faster                                                       |
| nqueens                 | 65.1 ms                                                                  | 57.1 ms: 1.14x faster                                                       |
| pyflate                 | 302 ms                                                                   | 266 ms: 1.14x faster                                                        |
| regex_compile           | 89.7 ms                                                                  | 79.4 ms: 1.13x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 168 ms: 1.12x faster                                                        |
| deepcopy                | 240 us                                                                   | 214 us: 1.12x faster                                                        |
| scimark_fft             | 183 ms                                                                   | 163 ms: 1.12x faster                                                        |
| deepcopy_reduce         | 2.06 us                                                                  | 1.84 us: 1.12x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 66.7 ms: 1.12x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 43.4 ms: 1.11x faster                                                       |
| chaos                   | 47.3 ms                                                                  | 42.5 ms: 1.11x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 838 us: 1.11x faster                                                        |
| float                   | 53.3 ms                                                                  | 48.3 ms: 1.10x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.52 sec: 1.10x faster                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.03 ms: 1.10x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 33.7 ms: 1.09x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.8 ms: 1.09x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 35.7 ms: 1.08x faster                                                       |
| pycparser               | 686 ms                                                                   | 638 ms: 1.07x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 40.5 ms: 1.07x faster                                                       |
| sympy_expand            | 298 ms                                                                   | 278 ms: 1.07x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.61 us: 1.07x faster                                                       |
| async_generators        | 180 ms                                                                   | 168 ms: 1.07x faster                                                        |
| xml_etree_generate      | 52.3 ms                                                                  | 49.2 ms: 1.06x faster                                                       |
| logging_format          | 7.13 us                                                                  | 6.73 us: 1.06x faster                                                       |
| 2to3                    | 204 ms                                                                   | 193 ms: 1.06x faster                                                        |
| sympy_str               | 184 ms                                                                   | 174 ms: 1.06x faster                                                        |
| coverage                | 55.3 ms                                                                  | 52.5 ms: 1.05x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.27 us: 1.05x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.73 ms: 1.05x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.0 ms: 1.05x faster                                                       |
| thrift                  | 487 us                                                                   | 466 us: 1.04x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 493 ms: 1.04x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 88.8 ms: 1.04x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 830 us: 1.03x faster                                                        |
| unpickle                | 8.01 us                                                                  | 7.78 us: 1.03x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.2 us: 1.03x faster                                                       |
| dask                    | 267 ms                                                                   | 261 ms: 1.02x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.56 sec: 1.02x faster                                                      |
| comprehensions          | 15.4 us                                                                  | 15.1 us: 1.02x faster                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 60.8 ms: 1.02x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 97.4 ms: 1.02x faster                                                       |
| coroutines              | 14.8 ms                                                                  | 14.6 ms: 1.01x faster                                                       |
| pathlib                 | 72.9 ms                                                                  | 73.7 ms: 1.01x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.0 us: 1.02x slower                                                       |
| pidigits                | 147 ms                                                                   | 150 ms: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 62.9 ms: 1.03x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 767 ms: 1.03x slower                                                        |
| generators              | 33.5 ms                                                                  | 34.8 ms: 1.04x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.74 us: 1.04x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 14.1 ms: 1.04x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.47 ms: 1.04x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 700 us: 1.05x slower                                                        |
| regex_dna               | 115 ms                                                                   | 121 ms: 1.05x slower                                                        |
| pickle                  | 6.47 us                                                                  | 6.81 us: 1.05x slower                                                       |
| pickle_list             | 2.70 us                                                                  | 2.85 us: 1.06x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 731 ms: 1.09x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (3): async_tree_memoization, tornado_http, async_tree_none
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
