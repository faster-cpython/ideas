
# Results vs. 3.10.4

- fork: python
- ref: 41cb07120b7792eac641
- machine: windows-amd64
- commit hash: 41cb071
- commit date: 2022-08-05
- overall geometric mean: 1.11x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.13x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 5.05 ms: 1.14x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 38.4 ms: 1.23x faster                                                       |
| tornado_http   | 106 ms                                                                   | 90.9 ms: 1.17x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.17x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 52.9 ms: 1.13x faster                                                       |
| nbody          | 71.5 ms                                                                  | 68.3 ms: 1.05x faster                                                       |
| pidigits       | 145 ms                                                                   | 146 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 89.4 ms: 1.16x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 14.1 ms: 1.07x faster                                                       |
| regex_dna      | 131 ms                                                                   | 123 ms: 1.06x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.66 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 202 us: 1.31x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 150 us: 1.19x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 36.7 ms: 1.17x faster                                                       |
| json_dumps           | 9.00 ms                                                                  | 7.73 ms: 1.16x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.11 us: 1.10x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.44 us: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.64 us: 1.03x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 52.6 ms: 1.02x faster                                                       |
| json_loads           | 14.2 us                                                                  | 14.0 us: 1.01x faster                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.2 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 23.7 ms: 1.23x faster                                                       |
| mako            | 8.69 ms                                                                  | 7.26 ms: 1.20x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 16.7 ms: 1.11x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 37.7 ms: 1.03x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.14x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.63 ms: 1.58x faster                                                       |
| go                      | 143 ms                                                                   | 101 ms: 1.42x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 739 ms: 1.38x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 77.3 ms: 1.34x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 310 ms: 1.34x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 368 ms: 1.32x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 925 us: 1.32x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 63.7 ms: 1.32x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 71.9 ns: 1.32x faster                                                       |
| richards                | 41.0 ms                                                                  | 31.3 ms: 1.31x faster                                                       |
| raytrace                | 267 ms                                                                   | 204 ms: 1.31x faster                                                        |
| thrift                  | 632 us                                                                   | 482 us: 1.31x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 202 us: 1.31x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.13 ms: 1.30x faster                                                       |
| pyflate                 | 388 ms                                                                   | 303 ms: 1.28x faster                                                        |
| pycparser               | 873 ms                                                                   | 689 ms: 1.27x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 44.4 ms: 1.26x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 48.7 ms: 1.26x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 38.4 ms: 1.23x faster                                                       |
| django_template         | 29.2 ms                                                                  | 23.7 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 491 ms: 1.23x faster                                                        |
| mypy2                   | 337 ms                                                                   | 275 ms: 1.23x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.46 ms: 1.22x faster                                                       |
| async_generators        | 214 ms                                                                   | 176 ms: 1.22x faster                                                        |
| mako                    | 8.69 ms                                                                  | 7.26 ms: 1.20x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 150 us: 1.19x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 49.6 ms: 1.18x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 1.04 sec: 1.17x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 36.7 ms: 1.17x faster                                                       |
| tornado_http            | 106 ms                                                                   | 90.9 ms: 1.17x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 7.73 ms: 1.16x faster                                                       |
| dask                    | 310 ms                                                                   | 267 ms: 1.16x faster                                                        |
| regex_compile           | 103 ms                                                                   | 89.4 ms: 1.16x faster                                                       |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 83.4 ms: 1.16x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 513 ms: 1.16x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                      |
| create_gc_cycles        | 764 us                                                                   | 665 us: 1.15x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 5.05 ms: 1.14x faster                                                       |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.13x faster                                                        |
| float                   | 59.5 ms                                                                  | 52.9 ms: 1.13x faster                                                       |
| aiohttp                 | 968 us                                                                   | 861 us: 1.12x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 25.3 us: 1.12x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 34.5 ms: 1.12x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 856 us: 1.11x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 16.7 ms: 1.11x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.68 us: 1.10x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.11 us: 1.10x faster                                                       |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.4 ms: 1.09x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.5 ms: 1.09x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 43.3 ms: 1.09x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.94 ms: 1.08x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 290 ms: 1.08x faster                                                        |
| deepcopy                | 256 us                                                                   | 238 us: 1.07x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 14.1 ms: 1.07x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 2.05 us: 1.07x faster                                                       |
| regex_dna               | 131 ms                                                                   | 123 ms: 1.06x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 189 ms: 1.06x faster                                                        |
| pylint                  | 337 ms                                                                   | 318 ms: 1.06x faster                                                        |
| coroutines              | 15.6 ms                                                                  | 14.8 ms: 1.06x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 97.0 ms: 1.05x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.2 us: 1.05x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                       |
| sympy_str               | 189 ms                                                                   | 180 ms: 1.05x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 68.3 ms: 1.05x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.44 us: 1.04x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 72.6 ms: 1.04x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 71.8 ms: 1.03x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 37.7 ms: 1.03x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.64 us: 1.03x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 182 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.61 ms: 1.02x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 52.6 ms: 1.02x faster                                                       |
| fannkuch                | 252 ms                                                                   | 247 ms: 1.02x faster                                                        |
| meteor_contest          | 74.3 ms                                                                  | 73.3 ms: 1.01x faster                                                       |
| json_loads              | 14.2 us                                                                  | 14.0 us: 1.01x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 64.2 ms: 1.01x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.60 sec: 1.00x faster                                                      |
| pidigits                | 145 ms                                                                   | 146 ms: 1.01x slower                                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.66 ms: 1.01x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.87 ms: 1.03x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.2 ms: 1.03x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 61.4 ms: 1.04x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.37 us: 1.04x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.40 ms: 1.06x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.90 us: 1.06x slower                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 41.9 ns: 1.06x slower                                                       |
| generators              | 31.4 ms                                                                  | 33.8 ms: 1.08x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.6 ms: 1.43x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (5): xml_etree_parse, asyncio_tcp, flaskblogging, pickle_list, xml_etree_iterparse
