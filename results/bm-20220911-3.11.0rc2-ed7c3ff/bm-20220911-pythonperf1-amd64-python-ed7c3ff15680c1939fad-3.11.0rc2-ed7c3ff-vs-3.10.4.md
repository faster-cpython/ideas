
# Results vs. 3.10.4

- fork: python
- ref: ed7c3ff15680c1939fad
- machine: windows-amd64
- commit hash: ed7c3ff
- commit date: 2022-09-11
- overall geometric mean: 1.11x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.13x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 5.09 ms: 1.13x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.57 sec: 1.16x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 37.2 ms: 1.27x faster                                                       |
| tornado_http   | 106 ms                                                                   | 92.1 ms: 1.16x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.17x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 53.9 ms: 1.10x faster                                                       |
| nbody          | 71.5 ms                                                                  | 68.6 ms: 1.04x faster                                                       |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 89.5 ms: 1.16x faster                                                       |
| regex_dna      | 131 ms                                                                   | 115 ms: 1.14x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.60 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 197 us: 1.34x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 149 us: 1.20x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.9 ms: 1.20x faster                                                       |
| json_dumps           | 9.00 ms                                                                  | 7.66 ms: 1.17x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.70 us: 1.15x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.55 us: 1.06x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.2 ms: 1.05x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 91.6 ms: 1.04x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.7 us: 1.04x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.60 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.9 ms: 1.01x faster                                                       |
| pickle_list          | 2.57 us                                                                  | 2.65 us: 1.03x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.2 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.5 ms: 1.04x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 23.8 ms: 1.22x faster                                                       |
| mako            | 8.69 ms                                                                  | 7.22 ms: 1.20x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 16.7 ms: 1.11x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.14x faster                                                                |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220911-pythonperf1-amd64-python-ed7c3ff15680c1939fad-3.11.0rc2-ed7c3ff |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.61 ms: 1.59x faster                                                       |
| go                      | 143 ms                                                                   | 97.5 ms: 1.47x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 740 ms: 1.38x faster                                                        |
| richards                | 41.0 ms                                                                  | 30.6 ms: 1.34x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 197 us: 1.34x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 77.3 ms: 1.34x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 310 ms: 1.33x faster                                                        |
| logging_silent          | 94.6 ns                                                                  | 70.9 ns: 1.33x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 920 us: 1.33x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 63.4 ms: 1.32x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 368 ms: 1.32x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.12 ms: 1.31x faster                                                       |
| thrift                  | 632 us                                                                   | 491 us: 1.29x faster                                                        |
| pyflate                 | 388 ms                                                                   | 303 ms: 1.28x faster                                                        |
| pycparser               | 873 ms                                                                   | 683 ms: 1.28x faster                                                        |
| html5lib                | 47.3 ms                                                                  | 37.2 ms: 1.27x faster                                                       |
| raytrace                | 267 ms                                                                   | 211 ms: 1.27x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 48.5 ms: 1.27x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 44.6 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 488 ms: 1.24x faster                                                        |
| django_template         | 29.2 ms                                                                  | 23.8 ms: 1.22x faster                                                       |
| mypy2                   | 337 ms                                                                   | 276 ms: 1.22x faster                                                        |
| async_generators        | 214 ms                                                                   | 176 ms: 1.22x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.48 ms: 1.22x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 48.0 ms: 1.22x faster                                                       |
| mako                    | 8.69 ms                                                                  | 7.22 ms: 1.20x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 149 us: 1.20x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 35.9 ms: 1.20x faster                                                       |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 81.7 ms: 1.18x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 7.66 ms: 1.17x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 1.05 sec: 1.17x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.57 sec: 1.16x faster                                                      |
| dask                    | 310 ms                                                                   | 267 ms: 1.16x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 512 ms: 1.16x faster                                                        |
| regex_compile           | 103 ms                                                                   | 89.5 ms: 1.16x faster                                                       |
| tornado_http            | 106 ms                                                                   | 92.1 ms: 1.16x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.70 us: 1.15x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 667 us: 1.15x faster                                                        |
| regex_dna               | 131 ms                                                                   | 115 ms: 1.14x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 34.0 ms: 1.14x faster                                                       |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.13x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 5.09 ms: 1.13x faster                                                       |
| aiohttp                 | 968 us                                                                   | 857 us: 1.13x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 849 us: 1.12x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 25.4 us: 1.12x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 16.7 ms: 1.11x faster                                                       |
| float                   | 59.5 ms                                                                  | 53.9 ms: 1.10x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.67 us: 1.10x faster                                                       |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.3 ms: 1.10x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 2.00 us: 1.09x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.5 ms: 1.08x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 186 ms: 1.08x faster                                                        |
| dulwich_log             | 47.0 ms                                                                  | 43.6 ms: 1.08x faster                                                       |
| deepcopy                | 256 us                                                                   | 239 us: 1.07x faster                                                        |
| pylint                  | 337 ms                                                                   | 316 ms: 1.07x faster                                                        |
| sympy_expand            | 313 ms                                                                   | 294 ms: 1.06x faster                                                        |
| unpickle_list           | 2.71 us                                                                  | 2.55 us: 1.06x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.2 us: 1.05x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.2 ms: 1.05x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.9 ms: 1.05x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 91.6 ms: 1.04x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 72.1 ms: 1.04x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.5 ms: 1.04x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 98.2 ms: 1.04x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 68.6 ms: 1.04x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.7 us: 1.04x faster                                                       |
| sympy_str               | 189 ms                                                                   | 182 ms: 1.04x faster                                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.60 ms: 1.03x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 73.2 ms: 1.01x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.60 us: 1.01x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.9 ms: 1.01x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.59 sec: 1.01x faster                                                      |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                        |
| scimark_fft             | 187 ms                                                                   | 189 ms: 1.01x slower                                                        |
| fannkuch                | 252 ms                                                                   | 256 ms: 1.02x slower                                                        |
| python_startup_no_site  | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.65 us: 1.03x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 61.2 ms: 1.03x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.91 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.81 ms: 1.05x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.41 ms: 1.06x slower                                                       |
| generators              | 31.4 ms                                                                  | 33.5 ms: 1.07x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.97 us: 1.07x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.57 us: 1.07x slower                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 42.7 ns: 1.08x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.2 us: 1.09x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.2 ms: 1.42x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (6): json, genshi_xml, nqueens, flaskblogging, meteor_contest, asyncio_tcp
