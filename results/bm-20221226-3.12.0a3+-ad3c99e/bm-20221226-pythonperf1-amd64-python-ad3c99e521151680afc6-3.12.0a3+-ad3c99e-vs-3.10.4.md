
# Results vs. 3.10.4

- fork: python
- ref: ad3c99e521151680afc6
- machine: windows-amd64
- commit hash: ad3c99e
- commit date: 2022-12-26
- overall geometric mean: 1.16x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 203 ms: 1.13x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.75 ms: 1.22x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.17x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 34.7 ms: 1.36x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 51.1 ms: 1.16x faster                                                       |
| nbody          | 71.5 ms                                                                  | 66.0 ms: 1.08x faster                                                       |
| pidigits       | 145 ms                                                                   | 153 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 83.8 ms: 1.23x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                                       |
| regex_dna      | 131 ms                                                                   | 125 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.43 ms: 1.66x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 186 us: 1.42x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 127 us: 1.41x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.7 ms: 1.21x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.20 us: 1.08x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 90.4 ms: 1.06x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.62 us: 1.03x faster                                                       |
| pickle               | 6.67 us                                                                  | 7.29 us: 1.09x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.83 us: 1.10x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.35 ms: 1.37x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.9 ms: 1.33x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.6 ms: 1.27x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 33.9 ms: 1.14x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.28x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3+-ad3c99e |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.25 ms: 1.85x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.43 ms: 1.66x faster                                                       |
| richards                | 41.0 ms                                                                  | 25.6 ms: 1.60x faster                                                       |
| go                      | 143 ms                                                                   | 91.7 ms: 1.56x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 60.9 ns: 1.55x faster                                                       |
| mypy2                   | 337 ms                                                                   | 228 ms: 1.48x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 70.3 ms: 1.47x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 59.0 ms: 1.42x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 186 us: 1.42x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 127 us: 1.41x faster                                                        |
| raytrace                | 267 ms                                                                   | 190 ms: 1.41x faster                                                        |
| pyflate                 | 388 ms                                                                   | 279 ms: 1.39x faster                                                        |
| asyncio_tcp             | 664 ms                                                                   | 482 ms: 1.38x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 40.7 ms: 1.38x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.35 ms: 1.37x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 34.7 ms: 1.36x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.09 ms: 1.35x faster                                                       |
| thrift                  | 632 us                                                                   | 470 us: 1.34x faster                                                        |
| django_template         | 29.2 ms                                                                  | 21.9 ms: 1.33x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.12 ms: 1.32x faster                                                       |
| pycparser               | 873 ms                                                                   | 661 ms: 1.32x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 29.9 ns: 1.32x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 46.7 ms: 1.32x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 932 us: 1.31x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 788 ms: 1.30x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 322 ms: 1.29x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 45.6 ms: 1.28x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 381 ms: 1.27x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 14.6 ms: 1.27x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 22.6 us: 1.26x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 987 ms: 1.24x faster                                                        |
| regex_compile           | 103 ms                                                                   | 83.8 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 492 ms: 1.23x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 484 ms: 1.23x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.75 ms: 1.22x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.7 ms: 1.21x faster                                                       |
| async_generators        | 214 ms                                                                   | 180 ms: 1.19x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 62.4 ms: 1.19x faster                                                       |
| dask                    | 310 ms                                                                   | 262 ms: 1.19x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.69 ms: 1.18x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.17x faster                                                      |
| float                   | 59.5 ms                                                                  | 51.1 ms: 1.16x faster                                                       |
| deepcopy                | 256 us                                                                   | 223 us: 1.15x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 33.9 ms: 1.14x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 56.9 ms: 1.14x faster                                                       |
| 2to3                    | 229 ms                                                                   | 203 ms: 1.13x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 845 us: 1.13x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 681 us: 1.12x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 181 ms: 1.11x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.97 us: 1.11x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 42.6 ms: 1.10x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 284 ms: 1.10x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.4 ms: 1.10x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.45 ms: 1.09x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.20 us: 1.08x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 66.0 ms: 1.08x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 14.0 ms: 1.08x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 176 ms: 1.06x faster                                                        |
| fannkuch                | 252 ms                                                                   | 238 ms: 1.06x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 90.4 ms: 1.06x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.9 ms: 1.05x faster                                                       |
| sympy_str               | 189 ms                                                                   | 180 ms: 1.05x faster                                                        |
| sympy_sum               | 102 ms                                                                   | 97.7 ms: 1.05x faster                                                       |
| regex_dna               | 131 ms                                                                   | 125 ms: 1.04x faster                                                        |
| xml_etree_generate      | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.04x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.62 us: 1.03x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.8 ms: 1.03x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.80 ms: 1.01x slower                                                       |
| pathlib                 | 75.2 ms                                                                  | 76.4 ms: 1.02x slower                                                       |
| mdp                     | 1.60 sec                                                                 | 1.63 sec: 1.02x slower                                                      |
| logging_format          | 6.53 us                                                                  | 6.84 us: 1.05x slower                                                       |
| pidigits                | 145 ms                                                                   | 153 ms: 1.05x slower                                                        |
| bench_mp_pool           | 59.2 ms                                                                  | 62.6 ms: 1.06x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.51 us: 1.06x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.29 us: 1.09x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.83 us: 1.10x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.49 ms: 1.12x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| generators              | 31.4 ms                                                                  | 37.8 ms: 1.20x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.4 ms: 1.43x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.16x faster                                                                |

Benchmark hidden because not significant (3): regex_effbot, comprehensions, xml_etree_iterparse
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
