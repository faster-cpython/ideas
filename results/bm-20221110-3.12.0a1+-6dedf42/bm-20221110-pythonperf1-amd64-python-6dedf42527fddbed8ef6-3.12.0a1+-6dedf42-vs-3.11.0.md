
# Results vs. 3.11.0

- fork: python
- ref: 6dedf42527fddbed8ef6
- machine: windows-amd64
- commit hash: 6dedf42
- commit date: 2022-11-10
- overall geometric mean: 1.05x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 198 ms: 1.03x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.64 ms: 1.11x faster                                                       |
| html5lib       | 38.5 ms                                                                  | 35.4 ms: 1.09x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 93.3 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 63.7 ms: 1.11x faster                                                       |
| float          | 53.3 ms                                                                  | 51.1 ms: 1.04x faster                                                       |
| pidigits       | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 85.8 ms: 1.05x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.64 ms: 1.00x slower                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.4 ms: 1.07x slower                                                       |
| regex_dna      | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.26 ms: 1.47x faster                                                       |
| unpickle_pure_python | 150 us                                                                   | 128 us: 1.16x faster                                                        |
| pickle_pure_python   | 203 us                                                                   | 188 us: 1.08x faster                                                        |
| unpickle_list        | 2.80 us                                                                  | 2.59 us: 1.08x faster                                                       |
| json_loads           | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                       |
| xml_etree_process    | 36.6 ms                                                                  | 35.4 ms: 1.03x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 90.3 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 51.3 ms: 1.02x faster                                                       |
| pickle_dict          | 18.6 us                                                                  | 18.9 us: 1.01x slower                                                       |
| pickle_list          | 2.70 us                                                                  | 2.76 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 63.7 ms: 1.03x slower                                                       |
| pickle               | 6.47 us                                                                  | 6.74 us: 1.04x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 14.9 ms: 1.16x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.40 ms: 1.13x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 34.0 ms: 1.12x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.9 ms: 1.09x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.12x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1+-6dedf42 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 7.71 ms                                                                  | 5.26 ms: 1.47x faster                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 32.0 ns: 1.35x faster                                                       |
| mypy2                   | 276 ms                                                                   | 223 ms: 1.24x faster                                                        |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.17 ms: 1.21x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.70 ms: 1.19x faster                                                       |
| richards                | 32.1 ms                                                                  | 27.1 ms: 1.18x faster                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 39.0 ms: 1.17x faster                                                       |
| unpickle_pure_python    | 150 us                                                                   | 128 us: 1.16x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 14.9 ms: 1.16x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.31 ms: 1.16x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 61.2 ns: 1.16x faster                                                       |
| mako                    | 7.20 ms                                                                  | 6.40 ms: 1.13x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 63.8 ms: 1.12x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 22.6 us: 1.12x faster                                                       |
| fannkuch                | 255 ms                                                                   | 228 ms: 1.12x faster                                                        |
| genshi_xml              | 38.0 ms                                                                  | 34.0 ms: 1.12x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 63.7 ms: 1.11x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.64 ms: 1.11x faster                                                       |
| scimark_sor             | 77.7 ms                                                                  | 70.5 ms: 1.10x faster                                                       |
| pyflate                 | 302 ms                                                                   | 275 ms: 1.10x faster                                                        |
| go                      | 97.5 ms                                                                  | 88.7 ms: 1.10x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 35.4 ms: 1.09x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.9 ms: 1.09x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 188 us: 1.08x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.59 us: 1.08x faster                                                       |
| mdp                     | 1.67 sec                                                                 | 1.55 sec: 1.08x faster                                                      |
| scimark_lu              | 62.8 ms                                                                  | 58.4 ms: 1.08x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 476 ms: 1.07x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 60.6 ms: 1.07x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 979 ms: 1.07x faster                                                        |
| raytrace                | 206 ms                                                                   | 192 ms: 1.07x faster                                                        |
| hexiom                  | 4.46 ms                                                                  | 4.17 ms: 1.07x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 171 ms: 1.07x faster                                                        |
| telco                   | 3.93 ms                                                                  | 3.70 ms: 1.06x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.7 ms: 1.06x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.29 us: 1.05x faster                                                       |
| sympy_str               | 184 ms                                                                   | 176 ms: 1.05x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.81 us: 1.05x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 85.8 ms: 1.05x faster                                                       |
| json_loads              | 13.5 us                                                                  | 13.0 us: 1.04x faster                                                       |
| float                   | 53.3 ms                                                                  | 51.1 ms: 1.04x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.97 us: 1.04x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 182 ms: 1.04x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 45.5 ms: 1.04x faster                                                       |
| deepcopy                | 240 us                                                                   | 231 us: 1.04x faster                                                        |
| xml_etree_process       | 36.6 ms                                                                  | 35.4 ms: 1.03x faster                                                       |
| pycparser               | 686 ms                                                                   | 665 ms: 1.03x faster                                                        |
| dulwich_log             | 43.4 ms                                                                  | 42.1 ms: 1.03x faster                                                       |
| 2to3                    | 204 ms                                                                   | 198 ms: 1.03x faster                                                        |
| sqlglot_optimize        | 34.5 ms                                                                  | 33.6 ms: 1.03x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.10 ms: 1.03x faster                                                       |
| bench_thread_pool       | 856 us                                                                   | 838 us: 1.02x faster                                                        |
| sympy_expand            | 298 ms                                                                   | 292 ms: 1.02x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 90.3 ms: 1.02x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 51.3 ms: 1.02x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.4 ms: 1.02x faster                                                       |
| thrift                  | 487 us                                                                   | 478 us: 1.02x faster                                                        |
| coverage                | 55.3 ms                                                                  | 54.4 ms: 1.02x faster                                                       |
| dask                    | 267 ms                                                                   | 263 ms: 1.01x faster                                                        |
| meteor_contest          | 74.4 ms                                                                  | 73.4 ms: 1.01x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 918 us: 1.01x faster                                                        |
| regex_effbot            | 1.63 ms                                                                  | 1.64 ms: 1.00x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 73.7 ms: 1.01x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.9 us: 1.01x slower                                                       |
| python_startup          | 18.4 ms                                                                  | 18.6 ms: 1.01x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 15.0 ms: 1.02x slower                                                       |
| tornado_http            | 91.8 ms                                                                  | 93.3 ms: 1.02x slower                                                       |
| async_generators        | 180 ms                                                                   | 183 ms: 1.02x slower                                                        |
| async_tree_none         | 313 ms                                                                   | 319 ms: 1.02x slower                                                        |
| pickle_list             | 2.70 us                                                                  | 2.76 us: 1.02x slower                                                       |
| bench_mp_pool           | 61.2 ms                                                                  | 62.8 ms: 1.03x slower                                                       |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 684 us: 1.03x slower                                                        |
| sqlite_synth            | 1.67 us                                                                  | 1.72 us: 1.03x slower                                                       |
| pidigits                | 147 ms                                                                   | 151 ms: 1.03x slower                                                        |
| xml_etree_iterparse     | 61.8 ms                                                                  | 63.7 ms: 1.03x slower                                                       |
| pickle                  | 6.47 us                                                                  | 6.74 us: 1.04x slower                                                       |
| async_tree_memoization  | 374 ms                                                                   | 391 ms: 1.05x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.47 ms: 1.05x slower                                                       |
| comprehensions          | 15.4 us                                                                  | 16.3 us: 1.06x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 790 ms: 1.06x slower                                                        |
| regex_v8                | 13.5 ms                                                                  | 14.4 ms: 1.07x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 723 ms: 1.07x slower                                                        |
| regex_dna               | 115 ms                                                                   | 124 ms: 1.08x slower                                                        |
| generators              | 33.5 ms                                                                  | 37.0 ms: 1.10x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, sympy_sum, docutils, unpickle
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
