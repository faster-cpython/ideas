
# Results vs. 3.10.4

- fork: python
- ref: aad5f6a89125ad4529ab
- machine: windows-amd64
- commit hash: aad5f6a
- commit date: 2023-02-07
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 231 ms: 1.01x slower                                                      |
| chameleon      | 5.77 ms                                                                  | 5.49 ms: 1.05x faster                                                     |
| docutils       | 1.83 sec                                                                 | 1.84 sec: 1.01x slower                                                    |
| html5lib       | 47.3 ms                                                                  | 48.2 ms: 1.02x slower                                                     |
| tornado_http   | 106 ms                                                                   | 109 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 60.6 ms: 1.02x slower                                                     |
| pidigits       | 145 ms                                                                   | 148 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                              |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                                  | 15.0 ms: 1.01x faster                                                     |
| regex_dna      | 131 ms                                                                   | 132 ms: 1.01x slower                                                      |
| regex_effbot   | 1.64 ms                                                                  | 1.81 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|---------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_generate  | 53.8 ms                                                                  | 53.3 ms: 1.01x faster                                                     |
| json_dumps          | 9.00 ms                                                                  | 8.93 ms: 1.01x faster                                                     |
| xml_etree_process   | 43.0 ms                                                                  | 42.7 ms: 1.01x faster                                                     |
| xml_etree_parse     | 95.6 ms                                                                  | 96.6 ms: 1.01x slower                                                     |
| pickle_pure_python  | 264 us                                                                   | 267 us: 1.01x slower                                                      |
| xml_etree_iterparse | 62.5 ms                                                                  | 64.4 ms: 1.03x slower                                                     |
| pickle              | 6.67 us                                                                  | 7.00 us: 1.05x slower                                                     |
| pickle_list         | 2.57 us                                                                  | 2.91 us: 1.13x slower                                                     |
| pickle_dict         | 16.7 us                                                                  | 19.1 us: 1.15x slower                                                     |
| Geometric mean      | (ref)                                                                    | 1.03x slower                                                              |

Benchmark hidden because not significant (4): json_loads, unpickle_list, unpickle_pure_python, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 14.8 ms                                                                  | 15.0 ms: 1.01x slower                                                     |
| python_startup         | 19.3 ms                                                                  | 19.8 ms: 1.03x slower                                                     |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text    | 18.5 ms                                                                  | 18.3 ms: 1.01x faster                                                     |
| mako           | 8.69 ms                                                                  | 8.84 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                              |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-------------------------|:------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| chameleon               | 5.77 ms                                                                  | 5.49 ms: 1.05x faster                                                     |
| thrift                  | 632 us                                                                   | 605 us: 1.04x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 1.18 sec: 1.04x faster                                                    |
| json                    | 3.18 ms                                                                  | 3.06 ms: 1.04x faster                                                     |
| go                      | 143 ms                                                                   | 138 ms: 1.04x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 576 ms: 1.03x faster                                                      |
| pycparser               | 873 ms                                                                   | 855 ms: 1.02x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 15.7 us: 1.02x faster                                                     |
| meteor_contest          | 74.3 ms                                                                  | 72.9 ms: 1.02x faster                                                     |
| deepcopy_reduce         | 2.18 us                                                                  | 2.14 us: 1.02x faster                                                     |
| scimark_monte_carlo     | 56.0 ms                                                                  | 55.2 ms: 1.02x faster                                                     |
| genshi_text             | 18.5 ms                                                                  | 18.3 ms: 1.01x faster                                                     |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.45 ms: 1.01x faster                                                     |
| hexiom                  | 5.45 ms                                                                  | 5.38 ms: 1.01x faster                                                     |
| xml_etree_generate      | 53.8 ms                                                                  | 53.3 ms: 1.01x faster                                                     |
| bench_thread_pool       | 953 us                                                                   | 944 us: 1.01x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 8.93 ms: 1.01x faster                                                     |
| scimark_lu              | 83.9 ms                                                                  | 83.2 ms: 1.01x faster                                                     |
| xml_etree_process       | 43.0 ms                                                                  | 42.7 ms: 1.01x faster                                                     |
| regex_v8                | 15.1 ms                                                                  | 15.0 ms: 1.01x faster                                                     |
| sqlglot_optimize        | 38.7 ms                                                                  | 38.5 ms: 1.01x faster                                                     |
| raytrace                | 267 ms                                                                   | 266 ms: 1.00x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.84 sec: 1.01x slower                                                    |
| sqlglot_normalize       | 201 ms                                                                   | 202 ms: 1.01x slower                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.86 us: 1.01x slower                                                     |
| regex_dna               | 131 ms                                                                   | 132 ms: 1.01x slower                                                      |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 97.2 ms: 1.01x slower                                                     |
| deepcopy                | 256 us                                                                   | 258 us: 1.01x slower                                                      |
| 2to3                    | 229 ms                                                                   | 231 ms: 1.01x slower                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 1.23 ms: 1.01x slower                                                     |
| pylint                  | 337 ms                                                                   | 340 ms: 1.01x slower                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 96.6 ms: 1.01x slower                                                     |
| sympy_str               | 189 ms                                                                   | 191 ms: 1.01x slower                                                      |
| aiohttp                 | 968 us                                                                   | 980 us: 1.01x slower                                                      |
| pickle_pure_python      | 264 us                                                                   | 267 us: 1.01x slower                                                      |
| pyflate                 | 388 ms                                                                   | 393 ms: 1.01x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.0 ms: 1.01x slower                                                     |
| bench_mp_pool           | 59.2 ms                                                                  | 60.0 ms: 1.01x slower                                                     |
| create_gc_cycles        | 764 us                                                                   | 776 us: 1.02x slower                                                      |
| coroutines              | 15.6 ms                                                                  | 15.9 ms: 1.02x slower                                                     |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 11.5 ms: 1.02x slower                                                     |
| html5lib                | 47.3 ms                                                                  | 48.2 ms: 1.02x slower                                                     |
| mako                    | 8.69 ms                                                                  | 8.84 ms: 1.02x slower                                                     |
| float                   | 59.5 ms                                                                  | 60.6 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 615 ms: 1.02x slower                                                      |
| pidigits                | 145 ms                                                                   | 148 ms: 1.02x slower                                                      |
| async_tree_io           | 1.02 sec                                                                 | 1.05 sec: 1.02x slower                                                    |
| deepcopy_memo           | 28.4 us                                                                  | 29.1 us: 1.02x slower                                                     |
| python_startup          | 19.3 ms                                                                  | 19.8 ms: 1.03x slower                                                     |
| crypto_pyaes            | 61.4 ms                                                                  | 63.1 ms: 1.03x slower                                                     |
| tornado_http            | 106 ms                                                                   | 109 ms: 1.03x slower                                                      |
| telco                   | 3.77 ms                                                                  | 3.88 ms: 1.03x slower                                                     |
| fannkuch                | 252 ms                                                                   | 259 ms: 1.03x slower                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.4 ms: 1.03x slower                                                     |
| richards                | 41.0 ms                                                                  | 42.3 ms: 1.03x slower                                                     |
| generators              | 31.4 ms                                                                  | 32.5 ms: 1.04x slower                                                     |
| unpack_sequence         | 39.4 ns                                                                  | 40.8 ns: 1.04x slower                                                     |
| scimark_fft             | 187 ms                                                                   | 194 ms: 1.04x slower                                                      |
| sympy_sum               | 102 ms                                                                   | 106 ms: 1.04x slower                                                      |
| logging_format          | 6.53 us                                                                  | 6.81 us: 1.04x slower                                                     |
| dulwich_log             | 47.0 ms                                                                  | 49.0 ms: 1.04x slower                                                     |
| logging_silent          | 94.6 ns                                                                  | 99.1 ns: 1.05x slower                                                     |
| gc_traversal            | 1.33 ms                                                                  | 1.40 ms: 1.05x slower                                                     |
| pickle                  | 6.67 us                                                                  | 7.00 us: 1.05x slower                                                     |
| logging_simple          | 6.12 us                                                                  | 6.45 us: 1.05x slower                                                     |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.82 ms: 1.06x slower                                                     |
| async_generators        | 214 ms                                                                   | 227 ms: 1.06x slower                                                      |
| mdp                     | 1.60 sec                                                                 | 1.71 sec: 1.07x slower                                                    |
| coverage                | 37.5 ms                                                                  | 40.0 ms: 1.07x slower                                                     |
| regex_effbot            | 1.64 ms                                                                  | 1.81 ms: 1.11x slower                                                     |
| spectral_norm           | 74.3 ms                                                                  | 82.5 ms: 1.11x slower                                                     |
| pickle_list             | 2.57 us                                                                  | 2.91 us: 1.13x slower                                                     |
| pickle_dict             | 16.7 us                                                                  | 19.1 us: 1.15x slower                                                     |
| Geometric mean          | (ref)                                                                    | 1.01x slower                                                              |

Benchmark hidden because not significant (21): chaos, pathlib, flaskblogging, regex_compile, sympy_integrate, json_loads, django_template, mypy2, deltablue, sympy_expand, unpickle_list, scimark_sor, unpickle_pure_python, genshi_xml, nbody, async_tree_none, nqueens, async_tree_memoization, dask, unpickle, asyncio_tcp
