
# Results vs. 3.10.4

- fork: python
- ref: 2cd268a3a9340346dd86
- machine: windows-amd64
- commit hash: 2cd268a
- commit date: 2021-12-06
- overall geometric mean: 1.02x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 232 ms: 1.01x slower                                                     |
| chameleon      | 5.77 ms                                                                  | 5.89 ms: 1.02x slower                                                    |
| docutils       | 1.83 sec                                                                 | 1.88 sec: 1.02x slower                                                   |
| html5lib       | 47.3 ms                                                                  | 48.7 ms: 1.03x slower                                                    |
| tornado_http   | 106 ms                                                                   | 109 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 145 ms                                                                   | 149 ms: 1.03x slower                                                     |
| float          | 59.5 ms                                                                  | 61.8 ms: 1.04x slower                                                    |
| nbody          | 71.5 ms                                                                  | 77.2 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                                   | 129 ms: 1.01x faster                                                     |
| regex_v8       | 15.1 ms                                                                  | 15.0 ms: 1.01x faster                                                    |
| regex_compile  | 103 ms                                                                   | 103 ms: 1.00x faster                                                     |
| regex_effbot   | 1.64 ms                                                                  | 1.74 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle             | 8.88 us                                                                  | 8.17 us: 1.09x faster                                                    |
| json_dumps           | 9.00 ms                                                                  | 8.45 ms: 1.06x faster                                                    |
| unpickle_list        | 2.71 us                                                                  | 2.64 us: 1.03x faster                                                    |
| unpickle_pure_python | 179 us                                                                   | 177 us: 1.01x faster                                                     |
| pickle_pure_python   | 264 us                                                                   | 267 us: 1.01x slower                                                     |
| pickle_dict          | 16.7 us                                                                  | 17.0 us: 1.02x slower                                                    |
| xml_etree_generate   | 53.8 ms                                                                  | 55.0 ms: 1.02x slower                                                    |
| xml_etree_process    | 43.0 ms                                                                  | 44.0 ms: 1.02x slower                                                    |
| xml_etree_parse      | 95.6 ms                                                                  | 98.0 ms: 1.03x slower                                                    |
| pickle               | 6.67 us                                                                  | 6.84 us: 1.03x slower                                                    |
| xml_etree_iterparse  | 62.5 ms                                                                  | 64.6 ms: 1.03x slower                                                    |
| pickle_list          | 2.57 us                                                                  | 2.70 us: 1.05x slower                                                    |
| json_loads           | 14.2 us                                                                  | 15.0 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 14.8 ms                                                                  | 15.1 ms: 1.02x slower                                                    |
| python_startup         | 19.3 ms                                                                  | 19.7 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 8.69 ms                                                                  | 8.56 ms: 1.01x faster                                                    |
| genshi_xml     | 38.8 ms                                                                  | 40.9 ms: 1.05x slower                                                    |
| genshi_text    | 18.5 ms                                                                  | 19.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211206-pythonperf1-amd64-python-2cd268a3a9340346dd86-3.10.1-2cd268a |
|-------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle                | 8.88 us                                                                  | 8.17 us: 1.09x faster                                                    |
| json_dumps              | 9.00 ms                                                                  | 8.45 ms: 1.06x faster                                                    |
| go                      | 143 ms                                                                   | 137 ms: 1.04x faster                                                     |
| unpickle_list           | 2.71 us                                                                  | 2.64 us: 1.03x faster                                                    |
| generators              | 31.4 ms                                                                  | 30.7 ms: 1.02x faster                                                    |
| meteor_contest          | 74.3 ms                                                                  | 73.2 ms: 1.02x faster                                                    |
| mako                    | 8.69 ms                                                                  | 8.56 ms: 1.01x faster                                                    |
| pycparser               | 873 ms                                                                   | 861 ms: 1.01x faster                                                     |
| deepcopy_reduce         | 2.18 us                                                                  | 2.15 us: 1.01x faster                                                    |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.45 ms: 1.01x faster                                                    |
| unpickle_pure_python    | 179 us                                                                   | 177 us: 1.01x faster                                                     |
| regex_dna               | 131 ms                                                                   | 129 ms: 1.01x faster                                                     |
| thrift                  | 632 us                                                                   | 625 us: 1.01x faster                                                     |
| sqlglot_parse           | 1.22 ms                                                                  | 1.21 ms: 1.01x faster                                                    |
| comprehensions          | 16.0 us                                                                  | 15.8 us: 1.01x faster                                                    |
| regex_v8                | 15.1 ms                                                                  | 15.0 ms: 1.01x faster                                                    |
| deepcopy                | 256 us                                                                   | 254 us: 1.01x faster                                                     |
| scimark_lu              | 83.9 ms                                                                  | 83.4 ms: 1.01x faster                                                    |
| hexiom                  | 5.45 ms                                                                  | 5.42 ms: 1.01x faster                                                    |
| regex_compile           | 103 ms                                                                   | 103 ms: 1.00x faster                                                     |
| sqlite_synth            | 1.85 us                                                                  | 1.85 us: 1.00x slower                                                    |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 11.4 ms: 1.01x slower                                                    |
| create_gc_cycles        | 764 us                                                                   | 770 us: 1.01x slower                                                     |
| sympy_expand            | 313 ms                                                                   | 316 ms: 1.01x slower                                                     |
| sqlglot_normalize       | 201 ms                                                                   | 203 ms: 1.01x slower                                                     |
| nqueens                 | 64.8 ms                                                                  | 65.5 ms: 1.01x slower                                                    |
| pickle_pure_python      | 264 us                                                                   | 267 us: 1.01x slower                                                     |
| deepcopy_memo           | 28.4 us                                                                  | 28.7 us: 1.01x slower                                                    |
| pprint_safe_repr        | 593 ms                                                                   | 601 ms: 1.01x slower                                                     |
| bench_thread_pool       | 953 us                                                                   | 965 us: 1.01x slower                                                     |
| 2to3                    | 229 ms                                                                   | 232 ms: 1.01x slower                                                     |
| pprint_pformat          | 1.23 sec                                                                 | 1.24 sec: 1.01x slower                                                   |
| sqlglot_optimize        | 38.7 ms                                                                  | 39.2 ms: 1.01x slower                                                    |
| sympy_str               | 189 ms                                                                   | 191 ms: 1.01x slower                                                     |
| sympy_integrate         | 14.7 ms                                                                  | 14.9 ms: 1.01x slower                                                    |
| scimark_monte_carlo     | 56.0 ms                                                                  | 56.9 ms: 1.01x slower                                                    |
| chaos                   | 58.4 ms                                                                  | 59.4 ms: 1.02x slower                                                    |
| pyflate                 | 388 ms                                                                   | 394 ms: 1.02x slower                                                     |
| pickle_dict             | 16.7 us                                                                  | 17.0 us: 1.02x slower                                                    |
| coroutines              | 15.6 ms                                                                  | 15.9 ms: 1.02x slower                                                    |
| pylint                  | 337 ms                                                                   | 343 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 615 ms: 1.02x slower                                                     |
| python_startup_no_site  | 14.8 ms                                                                  | 15.1 ms: 1.02x slower                                                    |
| logging_simple          | 6.12 us                                                                  | 6.24 us: 1.02x slower                                                    |
| chameleon               | 5.77 ms                                                                  | 5.89 ms: 1.02x slower                                                    |
| sympy_sum               | 102 ms                                                                   | 104 ms: 1.02x slower                                                     |
| bench_mp_pool           | 59.2 ms                                                                  | 60.4 ms: 1.02x slower                                                    |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 98.4 ms: 1.02x slower                                                    |
| xml_etree_generate      | 53.8 ms                                                                  | 55.0 ms: 1.02x slower                                                    |
| python_startup          | 19.3 ms                                                                  | 19.7 ms: 1.02x slower                                                    |
| raytrace                | 267 ms                                                                   | 273 ms: 1.02x slower                                                     |
| xml_etree_process       | 43.0 ms                                                                  | 44.0 ms: 1.02x slower                                                    |
| aiohttp                 | 968 us                                                                   | 990 us: 1.02x slower                                                     |
| scimark_sor             | 104 ms                                                                   | 106 ms: 1.02x slower                                                     |
| telco                   | 3.77 ms                                                                  | 3.86 ms: 1.02x slower                                                    |
| docutils                | 1.83 sec                                                                 | 1.88 sec: 1.02x slower                                                   |
| xml_etree_parse         | 95.6 ms                                                                  | 98.0 ms: 1.03x slower                                                    |
| pickle                  | 6.67 us                                                                  | 6.84 us: 1.03x slower                                                    |
| dask                    | 310 ms                                                                   | 319 ms: 1.03x slower                                                     |
| tornado_http            | 106 ms                                                                   | 109 ms: 1.03x slower                                                     |
| pidigits                | 145 ms                                                                   | 149 ms: 1.03x slower                                                     |
| html5lib                | 47.3 ms                                                                  | 48.7 ms: 1.03x slower                                                    |
| logging_format          | 6.53 us                                                                  | 6.72 us: 1.03x slower                                                    |
| unpack_sequence         | 39.4 ns                                                                  | 40.5 ns: 1.03x slower                                                    |
| gc_traversal            | 1.33 ms                                                                  | 1.37 ms: 1.03x slower                                                    |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.6 ms: 1.03x slower                                                    |
| coverage                | 37.5 ms                                                                  | 38.8 ms: 1.04x slower                                                    |
| logging_silent          | 94.6 ns                                                                  | 98.0 ns: 1.04x slower                                                    |
| dulwich_log             | 47.0 ms                                                                  | 48.7 ms: 1.04x slower                                                    |
| float                   | 59.5 ms                                                                  | 61.8 ms: 1.04x slower                                                    |
| scimark_fft             | 187 ms                                                                   | 195 ms: 1.04x slower                                                     |
| async_generators        | 214 ms                                                                   | 224 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.80 ms: 1.05x slower                                                    |
| pickle_list             | 2.57 us                                                                  | 2.70 us: 1.05x slower                                                    |
| genshi_xml              | 38.8 ms                                                                  | 40.9 ms: 1.05x slower                                                    |
| genshi_text             | 18.5 ms                                                                  | 19.6 ms: 1.05x slower                                                    |
| fannkuch                | 252 ms                                                                   | 266 ms: 1.06x slower                                                     |
| json_loads              | 14.2 us                                                                  | 15.0 us: 1.06x slower                                                    |
| regex_effbot            | 1.64 ms                                                                  | 1.74 ms: 1.06x slower                                                    |
| crypto_pyaes            | 61.4 ms                                                                  | 65.5 ms: 1.07x slower                                                    |
| spectral_norm           | 74.3 ms                                                                  | 79.4 ms: 1.07x slower                                                    |
| mdp                     | 1.60 sec                                                                 | 1.72 sec: 1.07x slower                                                   |
| asyncio_tcp             | 664 ms                                                                   | 713 ms: 1.07x slower                                                     |
| nbody                   | 71.5 ms                                                                  | 77.2 ms: 1.08x slower                                                    |
| Geometric mean          | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (10): json, deltablue, richards, async_tree_memoization, flaskblogging, django_template, async_tree_io, mypy2, async_tree_none, pathlib
