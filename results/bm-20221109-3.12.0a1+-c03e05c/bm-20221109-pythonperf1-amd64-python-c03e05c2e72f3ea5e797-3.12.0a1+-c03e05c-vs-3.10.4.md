
# Results vs. 3.10.4

- fork: python
- ref: c03e05c2e72f3ea5e797
- machine: windows-amd64
- commit hash: c03e05c
- commit date: 2022-11-09
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 209 ms: 1.10x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 5.20 ms: 1.11x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.63 sec: 1.12x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 39.9 ms: 1.18x faster                                                       |
| tornado_http   | 106 ms                                                                   | 92.5 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 55.8 ms: 1.07x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                                  | 13.1 ms: 1.15x faster                                                       |
| regex_compile  | 103 ms                                                                   | 89.9 ms: 1.15x faster                                                       |
| regex_dna      | 131 ms                                                                   | 118 ms: 1.11x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.56 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.54 ms: 1.62x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 208 us: 1.27x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 154 us: 1.17x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 37.8 ms: 1.14x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.17 us: 1.09x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.7 ms: 1.07x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.78 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 65.2 ms: 1.04x slower                                                       |
| pickle               | 6.67 us                                                                  | 7.06 us: 1.06x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.76 us: 1.08x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.1 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 14.8 ms                                                                  | 16.4 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.05x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 7.18 ms: 1.21x faster                                                       |
| django_template | 29.2 ms                                                                  | 24.4 ms: 1.20x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 16.9 ms: 1.10x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.12x faster                                                                |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1+-c03e05c |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps              | 9.00 ms                                                                  | 5.54 ms: 1.62x faster                                                       |
| deltablue               | 4.15 ms                                                                  | 2.59 ms: 1.61x faster                                                       |
| mypy2                   | 337 ms                                                                   | 224 ms: 1.51x faster                                                        |
| go                      | 143 ms                                                                   | 105 ms: 1.37x faster                                                        |
| raytrace                | 267 ms                                                                   | 203 ms: 1.32x faster                                                        |
| logging_silent          | 94.6 ns                                                                  | 72.0 ns: 1.31x faster                                                       |
| richards                | 41.0 ms                                                                  | 31.5 ms: 1.30x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 80.1 ms: 1.29x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 956 us: 1.27x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.16 ms: 1.27x faster                                                       |
| thrift                  | 632 us                                                                   | 497 us: 1.27x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 208 us: 1.27x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 48.6 ms: 1.26x faster                                                       |
| pyflate                 | 388 ms                                                                   | 311 ms: 1.25x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 827 ms: 1.24x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 67.9 ms: 1.24x faster                                                       |
| pycparser               | 873 ms                                                                   | 711 ms: 1.23x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 338 ms: 1.22x faster                                                        |
| mako                    | 8.69 ms                                                                  | 7.18 ms: 1.21x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 402 ms: 1.21x faster                                                        |
| django_template         | 29.2 ms                                                                  | 24.4 ms: 1.20x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 49.1 ms: 1.19x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 39.9 ms: 1.18x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 47.5 ms: 1.18x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 506 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 517 ms: 1.17x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 154 us: 1.17x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 1.06 sec: 1.16x faster                                                      |
| json                    | 3.18 ms                                                                  | 2.74 ms: 1.16x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.1 ms: 1.15x faster                                                       |
| dask                    | 310 ms                                                                   | 270 ms: 1.15x faster                                                        |
| tornado_http            | 106 ms                                                                   | 92.5 ms: 1.15x faster                                                       |
| regex_compile           | 103 ms                                                                   | 89.9 ms: 1.15x faster                                                       |
| async_generators        | 214 ms                                                                   | 188 ms: 1.14x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 37.8 ms: 1.14x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 672 us: 1.14x faster                                                        |
| dulwich_log             | 47.0 ms                                                                  | 41.6 ms: 1.13x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.63 sec: 1.12x faster                                                      |
| regex_dna               | 131 ms                                                                   | 118 ms: 1.11x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 5.20 ms: 1.11x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 25.7 us: 1.11x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.95 ms: 1.10x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.43 ms: 1.10x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 868 us: 1.10x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 16.9 ms: 1.10x faster                                                       |
| 2to3                    | 229 ms                                                                   | 209 ms: 1.10x faster                                                        |
| json_loads              | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 35.4 ms: 1.09x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.17 us: 1.09x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.6 ms: 1.08x faster                                                       |
| float                   | 59.5 ms                                                                  | 55.8 ms: 1.07x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 89.7 ms: 1.07x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 297 ms: 1.05x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 70.5 ms: 1.05x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.56 ms: 1.05x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 15.1 ms: 1.04x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 2.11 us: 1.03x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 72.0 ms: 1.03x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 196 ms: 1.03x faster                                                        |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.02x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 74.2 ms: 1.01x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 101 ms: 1.01x faster                                                        |
| sympy_str               | 189 ms                                                                   | 188 ms: 1.01x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 189 ms: 1.01x slower                                                        |
| unpickle_list           | 2.71 us                                                                  | 2.78 us: 1.02x slower                                                       |
| nqueens                 | 64.8 ms                                                                  | 67.1 ms: 1.03x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| xml_etree_iterparse     | 62.5 ms                                                                  | 65.2 ms: 1.04x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.95 ms: 1.05x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.06 us: 1.06x slower                                                       |
| mdp                     | 1.60 sec                                                                 | 1.70 sec: 1.06x slower                                                      |
| fannkuch                | 252 ms                                                                   | 270 ms: 1.07x slower                                                        |
| comprehensions          | 16.0 us                                                                  | 17.1 us: 1.07x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.76 us: 1.08x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                                       |
| generators              | 31.4 ms                                                                  | 34.5 ms: 1.10x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 16.4 ms: 1.11x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 753 ms: 1.13x slower                                                        |
| logging_format          | 6.53 us                                                                  | 7.41 us: 1.14x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 67.3 ms: 1.14x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.1 us: 1.15x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 7.05 us: 1.15x slower                                                       |
| coverage                | 37.5 ms                                                                  | 55.0 ms: 1.47x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (6): unpack_sequence, deepcopy, nbody, genshi_xml, xml_etree_generate, python_startup
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
