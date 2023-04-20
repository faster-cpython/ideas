
# Results vs. 3.10.4

- fork: python
- ref: 7d4cc5aa854fdea4d01a
- machine: windows-amd64
- commit hash: 7d4cc5a
- commit date: 2023-04-04
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 233 ms: 1.02x slower                                                      |
| chameleon      | 5.77 ms                                                                  | 5.67 ms: 1.02x faster                                                     |
| docutils       | 1.83 sec                                                                 | 1.82 sec: 1.00x faster                                                    |
| html5lib       | 47.3 ms                                                                  | 45.8 ms: 1.03x faster                                                     |
| tornado_http   | 106 ms                                                                   | 108 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                      |
| float          | 59.5 ms                                                                  | 60.7 ms: 1.02x slower                                                     |
| nbody          | 71.5 ms                                                                  | 75.5 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                                  | 14.6 ms: 1.03x faster                                                     |
| regex_effbot   | 1.64 ms                                                                  | 1.60 ms: 1.02x faster                                                     |
| regex_dna      | 131 ms                                                                   | 129 ms: 1.01x faster                                                      |
| regex_compile  | 103 ms                                                                   | 102 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                                  | 13.7 us: 1.03x faster                                                     |
| unpickle_list        | 2.71 us                                                                  | 2.66 us: 1.02x faster                                                     |
| unpickle_pure_python | 179 us                                                                   | 177 us: 1.01x faster                                                      |
| json_dumps           | 9.00 ms                                                                  | 8.90 ms: 1.01x faster                                                     |
| pickle_pure_python   | 264 us                                                                   | 266 us: 1.01x slower                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 96.4 ms: 1.01x slower                                                     |
| xml_etree_generate   | 53.8 ms                                                                  | 54.3 ms: 1.01x slower                                                     |
| xml_etree_process    | 43.0 ms                                                                  | 43.5 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.4 ms: 1.01x slower                                                     |
| unpickle             | 8.88 us                                                                  | 9.30 us: 1.05x slower                                                     |
| pickle               | 6.67 us                                                                  | 7.34 us: 1.10x slower                                                     |
| pickle_list          | 2.57 us                                                                  | 2.86 us: 1.11x slower                                                     |
| pickle_dict          | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                                    | 1.03x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 14.8 ms                                                                  | 15.6 ms: 1.05x slower                                                     |
| python_startup         | 19.3 ms                                                                  | 21.1 ms: 1.09x slower                                                     |
| Geometric mean         | (ref)                                                                    | 1.07x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 28.9 ms: 1.01x faster                                                     |
| mako            | 8.69 ms                                                                  | 8.76 ms: 1.01x slower                                                     |
| genshi_xml      | 38.8 ms                                                                  | 39.1 ms: 1.01x slower                                                     |
| genshi_text     | 18.5 ms                                                                  | 18.8 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json                    | 3.18 ms                                                                  | 3.02 ms: 1.05x faster                                                     |
| go                      | 143 ms                                                                   | 137 ms: 1.05x faster                                                      |
| pycparser               | 873 ms                                                                   | 839 ms: 1.04x faster                                                      |
| json_loads              | 14.2 us                                                                  | 13.7 us: 1.03x faster                                                     |
| html5lib                | 47.3 ms                                                                  | 45.8 ms: 1.03x faster                                                     |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.42 ms: 1.03x faster                                                     |
| regex_v8                | 15.1 ms                                                                  | 14.6 ms: 1.03x faster                                                     |
| meteor_contest          | 74.3 ms                                                                  | 72.1 ms: 1.03x faster                                                     |
| sqlglot_parse           | 1.22 ms                                                                  | 1.19 ms: 1.03x faster                                                     |
| pprint_pformat          | 1.23 sec                                                                 | 1.19 sec: 1.03x faster                                                    |
| bench_thread_pool       | 953 us                                                                   | 928 us: 1.03x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 15.6 us: 1.03x faster                                                     |
| dask                    | 310 ms                                                                   | 303 ms: 1.02x faster                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.60 ms: 1.02x faster                                                     |
| deepcopy_reduce         | 2.18 us                                                                  | 2.13 us: 1.02x faster                                                     |
| unpickle_list           | 2.71 us                                                                  | 2.66 us: 1.02x faster                                                     |
| chameleon               | 5.77 ms                                                                  | 5.67 ms: 1.02x faster                                                     |
| pprint_safe_repr        | 593 ms                                                                   | 584 ms: 1.02x faster                                                      |
| regex_dna               | 131 ms                                                                   | 129 ms: 1.01x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 177 us: 1.01x faster                                                      |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 11.1 ms: 1.01x faster                                                     |
| regex_compile           | 103 ms                                                                   | 102 ms: 1.01x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 8.90 ms: 1.01x faster                                                     |
| deltablue               | 4.15 ms                                                                  | 4.11 ms: 1.01x faster                                                     |
| pathlib                 | 75.2 ms                                                                  | 74.4 ms: 1.01x faster                                                     |
| hexiom                  | 5.45 ms                                                                  | 5.40 ms: 1.01x faster                                                     |
| django_template         | 29.2 ms                                                                  | 28.9 ms: 1.01x faster                                                     |
| aiohttp                 | 968 us                                                                   | 962 us: 1.01x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.82 sec: 1.00x faster                                                    |
| sqlglot_optimize        | 38.7 ms                                                                  | 38.5 ms: 1.00x faster                                                     |
| deepcopy_memo           | 28.4 us                                                                  | 28.6 us: 1.01x slower                                                     |
| pyflate                 | 388 ms                                                                   | 391 ms: 1.01x slower                                                      |
| scimark_lu              | 83.9 ms                                                                  | 84.5 ms: 1.01x slower                                                     |
| mako                    | 8.69 ms                                                                  | 8.76 ms: 1.01x slower                                                     |
| sympy_integrate         | 14.7 ms                                                                  | 14.8 ms: 1.01x slower                                                     |
| pickle_pure_python      | 264 us                                                                   | 266 us: 1.01x slower                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 96.4 ms: 1.01x slower                                                     |
| xml_etree_generate      | 53.8 ms                                                                  | 54.3 ms: 1.01x slower                                                     |
| genshi_xml              | 38.8 ms                                                                  | 39.1 ms: 1.01x slower                                                     |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                      |
| pylint                  | 337 ms                                                                   | 341 ms: 1.01x slower                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 43.5 ms: 1.01x slower                                                     |
| dulwich_log             | 47.0 ms                                                                  | 47.6 ms: 1.01x slower                                                     |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.4 ms: 1.01x slower                                                     |
| chaos                   | 58.4 ms                                                                  | 59.2 ms: 1.01x slower                                                     |
| raytrace                | 267 ms                                                                   | 271 ms: 1.01x slower                                                      |
| genshi_text             | 18.5 ms                                                                  | 18.8 ms: 1.02x slower                                                     |
| tornado_http            | 106 ms                                                                   | 108 ms: 1.02x slower                                                      |
| 2to3                    | 229 ms                                                                   | 233 ms: 1.02x slower                                                      |
| deepcopy                | 256 us                                                                   | 260 us: 1.02x slower                                                      |
| create_gc_cycles        | 764 us                                                                   | 777 us: 1.02x slower                                                      |
| async_generators        | 214 ms                                                                   | 218 ms: 1.02x slower                                                      |
| float                   | 59.5 ms                                                                  | 60.7 ms: 1.02x slower                                                     |
| bench_mp_pool           | 59.2 ms                                                                  | 60.4 ms: 1.02x slower                                                     |
| generators              | 31.4 ms                                                                  | 32.1 ms: 1.02x slower                                                     |
| sympy_sum               | 102 ms                                                                   | 105 ms: 1.02x slower                                                      |
| logging_simple          | 6.12 us                                                                  | 6.28 us: 1.03x slower                                                     |
| logging_silent          | 94.6 ns                                                                  | 97.2 ns: 1.03x slower                                                     |
| crypto_pyaes            | 61.4 ms                                                                  | 63.2 ms: 1.03x slower                                                     |
| logging_format          | 6.53 us                                                                  | 6.76 us: 1.03x slower                                                     |
| scimark_sor             | 104 ms                                                                   | 107 ms: 1.04x slower                                                      |
| nqueens                 | 64.8 ms                                                                  | 67.5 ms: 1.04x slower                                                     |
| telco                   | 3.77 ms                                                                  | 3.93 ms: 1.04x slower                                                     |
| coverage                | 37.5 ms                                                                  | 39.2 ms: 1.05x slower                                                     |
| unpickle                | 8.88 us                                                                  | 9.30 us: 1.05x slower                                                     |
| scimark_monte_carlo     | 56.0 ms                                                                  | 58.9 ms: 1.05x slower                                                     |
| python_startup_no_site  | 14.8 ms                                                                  | 15.6 ms: 1.05x slower                                                     |
| nbody                   | 71.5 ms                                                                  | 75.5 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.83 ms: 1.06x slower                                                     |
| gc_traversal            | 1.33 ms                                                                  | 1.42 ms: 1.06x slower                                                     |
| mdp                     | 1.60 sec                                                                 | 1.71 sec: 1.07x slower                                                    |
| unpack_sequence         | 39.4 ns                                                                  | 42.1 ns: 1.07x slower                                                     |
| scimark_fft             | 187 ms                                                                   | 203 ms: 1.08x slower                                                      |
| python_startup          | 19.3 ms                                                                  | 21.1 ms: 1.09x slower                                                     |
| spectral_norm           | 74.3 ms                                                                  | 81.4 ms: 1.10x slower                                                     |
| fannkuch                | 252 ms                                                                   | 276 ms: 1.10x slower                                                      |
| pickle                  | 6.67 us                                                                  | 7.34 us: 1.10x slower                                                     |
| pickle_list             | 2.57 us                                                                  | 2.86 us: 1.11x slower                                                     |
| pickle_dict             | 16.7 us                                                                  | 18.7 us: 1.12x slower                                                     |
| asyncio_tcp             | 664 ms                                                                   | 755 ms: 1.14x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.01x slower                                                              |

Benchmark hidden because not significant (14): async_tree_cpu_io_mixed, async_tree_memoization, sqlalchemy_declarative, thrift, richards, sympy_str, sympy_expand, sqlite_synth, flaskblogging, async_tree_none, sqlglot_normalize, coroutines, async_tree_io, mypy2
