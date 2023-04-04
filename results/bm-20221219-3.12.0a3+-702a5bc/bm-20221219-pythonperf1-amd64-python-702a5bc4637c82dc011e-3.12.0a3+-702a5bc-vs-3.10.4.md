
# Results vs. 3.10.4

- fork: python
- ref: 702a5bc4637c82dc011e
- machine: windows-amd64
- commit hash: 702a5bc
- commit date: 2022-12-19
- overall geometric mean: 1.17x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 204 ms: 1.12x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.63 ms: 1.25x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.6 ms: 1.33x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.21x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 50.3 ms: 1.18x faster                                                       |
| nbody          | 71.5 ms                                                                  | 63.8 ms: 1.12x faster                                                       |
| pidigits       | 145 ms                                                                   | 146 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 85.6 ms: 1.21x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.1 ms: 1.16x faster                                                       |
| regex_dna      | 131 ms                                                                   | 115 ms: 1.13x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.52 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.48 ms: 1.64x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 183 us: 1.44x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 128 us: 1.40x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.5 ms: 1.21x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.02 us: 1.11x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 50.0 ms: 1.08x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.4 us: 1.06x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 90.6 ms: 1.05x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.62 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 64.5 ms: 1.03x slower                                                       |
| pickle               | 6.67 us                                                                  | 6.99 us: 1.05x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.31 ms: 1.38x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.8 ms: 1.34x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.3 ms: 1.29x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 34.2 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.28x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3+-702a5bc |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.18 ms: 1.90x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.48 ms: 1.64x faster                                                       |
| go                      | 143 ms                                                                   | 88.8 ms: 1.61x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 59.1 ns: 1.60x faster                                                       |
| richards                | 41.0 ms                                                                  | 26.4 ms: 1.55x faster                                                       |
| mypy2                   | 337 ms                                                                   | 223 ms: 1.51x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 69.9 ms: 1.48x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 57.7 ms: 1.45x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 183 us: 1.44x faster                                                        |
| raytrace                | 267 ms                                                                   | 190 ms: 1.40x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 128 us: 1.40x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 40.1 ms: 1.40x faster                                                       |
| pyflate                 | 388 ms                                                                   | 281 ms: 1.38x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.31 ms: 1.38x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 486 ms: 1.37x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 900 us: 1.35x faster                                                        |
| django_template         | 29.2 ms                                                                  | 21.8 ms: 1.34x faster                                                       |
| thrift                  | 632 us                                                                   | 473 us: 1.34x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 29.5 ns: 1.33x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.10 ms: 1.33x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.6 ms: 1.33x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.13 ms: 1.32x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 46.8 ms: 1.31x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 21.7 us: 1.31x faster                                                       |
| pycparser               | 873 ms                                                                   | 675 ms: 1.29x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 14.3 ms: 1.29x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 953 ms: 1.29x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 807 ms: 1.27x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 469 ms: 1.27x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 46.5 ms: 1.26x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 386 ms: 1.26x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.63 ms: 1.25x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 334 ms: 1.24x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 35.5 ms: 1.21x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 499 ms: 1.21x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 61.3 ms: 1.21x faster                                                       |
| regex_compile           | 103 ms                                                                   | 85.6 ms: 1.21x faster                                                       |
| deepcopy                | 256 us                                                                   | 215 us: 1.19x faster                                                        |
| dask                    | 310 ms                                                                   | 261 ms: 1.19x faster                                                        |
| float                   | 59.5 ms                                                                  | 50.3 ms: 1.18x faster                                                       |
| async_generators        | 214 ms                                                                   | 181 ms: 1.18x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.1 ms: 1.16x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 33.5 ms: 1.15x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.92 us: 1.14x faster                                                       |
| regex_dna               | 131 ms                                                                   | 115 ms: 1.13x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.80 ms: 1.13x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 34.2 ms: 1.13x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.37 ms: 1.13x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 677 us: 1.13x faster                                                        |
| 2to3                    | 229 ms                                                                   | 204 ms: 1.12x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 63.8 ms: 1.12x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 42.0 ms: 1.12x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 855 us: 1.11x faster                                                        |
| unpickle                | 8.88 us                                                                  | 8.02 us: 1.11x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 182 ms: 1.11x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.3 ms: 1.10x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 286 ms: 1.09x faster                                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.52 ms: 1.08x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 60.1 ms: 1.08x faster                                                       |
| fannkuch                | 252 ms                                                                   | 233 ms: 1.08x faster                                                        |
| xml_etree_generate      | 53.8 ms                                                                  | 50.0 ms: 1.08x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.4 us: 1.06x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 90.6 ms: 1.05x faster                                                       |
| sympy_str               | 189 ms                                                                   | 179 ms: 1.05x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 179 ms: 1.04x faster                                                        |
| unpickle_list           | 2.71 us                                                                  | 2.62 us: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.04x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.55 sec: 1.04x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 15.1 ms: 1.03x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 99.7 ms: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 73.1 ms: 1.02x faster                                                       |
| pidigits                | 145 ms                                                                   | 146 ms: 1.01x slower                                                        |
| logging_simple          | 6.12 us                                                                  | 6.23 us: 1.02x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.86 ms: 1.02x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.5 ms: 1.03x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.82 us: 1.04x slower                                                       |
| pickle                  | 6.67 us                                                                  | 6.99 us: 1.05x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.2 ms: 1.07x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.48 ms: 1.11x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| generators              | 31.4 ms                                                                  | 38.7 ms: 1.23x slower                                                       |
| coverage                | 37.5 ms                                                                  | 54.0 ms: 1.44x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.17x faster                                                                |

Benchmark hidden because not significant (2): comprehensions, pathlib
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
