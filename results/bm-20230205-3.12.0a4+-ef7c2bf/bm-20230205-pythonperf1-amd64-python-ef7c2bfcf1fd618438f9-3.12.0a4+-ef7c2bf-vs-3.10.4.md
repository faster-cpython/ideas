
# Results vs. 3.10.4

- fork: python
- ref: ef7c2bfcf1fd618438f9
- machine: windows-amd64
- commit hash: ef7c2bf
- commit date: 2023-02-05
- overall geometric mean: 1.20x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 200 ms: 1.15x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.59 ms: 1.26x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.19x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 34.6 ms: 1.37x faster                                                       |
| tornado_http   | 106 ms                                                                   | 92.2 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 50.4 ms: 1.18x faster                                                       |
| nbody          | 71.5 ms                                                                  | 61.4 ms: 1.16x faster                                                       |
| pidigits       | 145 ms                                                                   | 152 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 77.6 ms: 1.33x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.3 ms: 1.14x faster                                                       |
| regex_dna      | 131 ms                                                                   | 119 ms: 1.10x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.54 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.16x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.14 ms: 1.75x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 175 us: 1.51x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 34.5 ms: 1.25x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 87.7 ms: 1.09x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 49.9 ms: 1.08x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| pickle               | 6.67 us                                                                  | 6.79 us: 1.02x slower                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.79 us: 1.03x slower                                                       |
| unpickle             | 8.88 us                                                                  | 9.39 us: 1.06x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.8 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.14 ms: 1.42x faster                                                       |
| django_template | 29.2 ms                                                                  | 21.1 ms: 1.39x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.8 ms: 1.26x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.5 ms: 1.19x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.31x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230205-pythonperf1-amd64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.02 ms: 2.05x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.14 ms: 1.75x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.5 ms: 1.67x faster                                                       |
| go                      | 143 ms                                                                   | 85.9 ms: 1.67x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 57.2 ns: 1.66x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 65.4 ms: 1.58x faster                                                       |
| mypy2                   | 337 ms                                                                   | 217 ms: 1.56x faster                                                        |
| raytrace                | 267 ms                                                                   | 174 ms: 1.53x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 175 us: 1.51x faster                                                        |
| pyflate                 | 388 ms                                                                   | 259 ms: 1.50x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 26.8 ns: 1.47x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 122 us: 1.47x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 57.5 ms: 1.46x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 38.4 ms: 1.46x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 40.9 ms: 1.43x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.14 ms: 1.42x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.86 ms: 1.41x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.1 ms: 1.39x faster                                                       |
| thrift                  | 632 us                                                                   | 457 us: 1.38x faster                                                        |
| asyncio_tcp             | 664 ms                                                                   | 481 ms: 1.38x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 44.5 ms: 1.38x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 34.6 ms: 1.37x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 891 us: 1.37x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.08 ms: 1.36x faster                                                       |
| pycparser               | 873 ms                                                                   | 648 ms: 1.35x faster                                                        |
| regex_compile           | 103 ms                                                                   | 77.6 ms: 1.33x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 312 ms: 1.33x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 21.5 us: 1.32x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 929 ms: 1.32x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 779 ms: 1.31x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 371 ms: 1.31x faster                                                        |
| comprehensions          | 16.0 us                                                                  | 12.3 us: 1.30x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 462 ms: 1.29x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.59 ms: 1.26x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 14.8 ms: 1.26x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 34.5 ms: 1.25x faster                                                       |
| async_generators        | 214 ms                                                                   | 173 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 490 ms: 1.23x faster                                                        |
| spectral_norm           | 74.3 ms                                                                  | 60.8 ms: 1.22x faster                                                       |
| deepcopy                | 256 us                                                                   | 214 us: 1.20x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.24 ms: 1.19x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.5 ms: 1.19x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.5 ms: 1.19x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.19x faster                                                      |
| fannkuch                | 252 ms                                                                   | 212 ms: 1.18x faster                                                        |
| float                   | 59.5 ms                                                                  | 50.4 ms: 1.18x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.5 ms: 1.17x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 61.4 ms: 1.16x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 40.6 ms: 1.16x faster                                                       |
| tornado_http            | 106 ms                                                                   | 92.2 ms: 1.15x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.89 us: 1.15x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.76 ms: 1.15x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 56.3 ms: 1.15x faster                                                       |
| sympy_str               | 189 ms                                                                   | 164 ms: 1.15x faster                                                        |
| 2to3                    | 229 ms                                                                   | 200 ms: 1.15x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 175 ms: 1.15x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 836 us: 1.14x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.3 ms: 1.14x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 276 ms: 1.13x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 166 ms: 1.13x faster                                                        |
| regex_dna               | 131 ms                                                                   | 119 ms: 1.10x faster                                                        |
| sympy_sum               | 102 ms                                                                   | 92.8 ms: 1.10x faster                                                       |
| json_loads              | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 87.7 ms: 1.09x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 49.9 ms: 1.08x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.54 ms: 1.07x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 718 us: 1.07x faster                                                        |
| coroutines              | 15.6 ms                                                                  | 14.7 ms: 1.06x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.51 sec: 1.06x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 71.1 ms: 1.04x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.04x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.8 ms: 1.03x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.58 us: 1.01x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.19 us: 1.01x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| pickle                  | 6.67 us                                                                  | 6.79 us: 1.02x slower                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.79 us: 1.03x slower                                                       |
| pidigits                | 145 ms                                                                   | 152 ms: 1.05x slower                                                        |
| unpickle                | 8.88 us                                                                  | 9.39 us: 1.06x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.9 ms: 1.08x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                                       |
| generators              | 31.4 ms                                                                  | 34.2 ms: 1.09x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                       |
| dask                    | 310 ms                                                                   | 353 ms: 1.14x slower                                                        |
| coverage                | 37.5 ms                                                                  | 53.9 ms: 1.44x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (2): pathlib, telco
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
