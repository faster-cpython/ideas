
# Results vs. 3.10.4

- fork: python
- ref: f3909b8bc83675b7ab09
- machine: windows-amd64
- commit hash: f3909b8
- commit date: 2023-04-04
- overall geometric mean: 1.11x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 206 ms: 1.11x faster                                                     |
| chameleon      | 5.77 ms                                                                  | 5.27 ms: 1.10x faster                                                    |
| docutils       | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                   |
| html5lib       | 47.3 ms                                                                  | 39.8 ms: 1.19x faster                                                    |
| tornado_http   | 106 ms                                                                   | 90.1 ms: 1.18x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 52.6 ms: 1.13x faster                                                    |
| nbody          | 71.5 ms                                                                  | 69.8 ms: 1.02x faster                                                    |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 89.7 ms: 1.15x faster                                                    |
| regex_dna      | 131 ms                                                                   | 120 ms: 1.09x faster                                                     |
| regex_v8       | 15.1 ms                                                                  | 14.3 ms: 1.06x faster                                                    |
| regex_effbot   | 1.64 ms                                                                  | 1.57 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 198 us: 1.34x faster                                                     |
| unpickle_pure_python | 179 us                                                                   | 150 us: 1.20x faster                                                     |
| xml_etree_process    | 43.0 ms                                                                  | 36.3 ms: 1.19x faster                                                    |
| json_dumps           | 9.00 ms                                                                  | 7.60 ms: 1.18x faster                                                    |
| unpickle             | 8.88 us                                                                  | 7.97 us: 1.11x faster                                                    |
| json_loads           | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                    |
| xml_etree_parse      | 95.6 ms                                                                  | 91.3 ms: 1.05x faster                                                    |
| xml_etree_generate   | 53.8 ms                                                                  | 51.8 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.4 ms: 1.02x faster                                                    |
| unpickle_list        | 2.71 us                                                                  | 2.68 us: 1.01x faster                                                    |
| pickle               | 6.67 us                                                                  | 6.73 us: 1.01x slower                                                    |
| pickle_list          | 2.57 us                                                                  | 2.78 us: 1.08x slower                                                    |
| pickle_dict          | 16.7 us                                                                  | 18.6 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                    |
| python_startup_no_site | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 23.8 ms: 1.23x faster                                                    |
| mako            | 8.69 ms                                                                  | 7.22 ms: 1.20x faster                                                    |
| genshi_text     | 18.5 ms                                                                  | 17.3 ms: 1.07x faster                                                    |
| genshi_xml      | 38.8 ms                                                                  | 37.6 ms: 1.03x faster                                                    |
| Geometric mean  | (ref)                                                                    | 1.13x faster                                                             |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230404-pythonperf1-amd64-python-f3909b8bc83675b7ab09-3.11.3-f3909b8 |
|-------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.65 ms: 1.56x faster                                                    |
| go                      | 143 ms                                                                   | 99.2 ms: 1.44x faster                                                    |
| async_tree_io           | 1.02 sec                                                                 | 739 ms: 1.38x faster                                                     |
| scimark_sor             | 104 ms                                                                   | 75.2 ms: 1.38x faster                                                    |
| richards                | 41.0 ms                                                                  | 30.4 ms: 1.35x faster                                                    |
| logging_silent          | 94.6 ns                                                                  | 70.1 ns: 1.35x faster                                                    |
| pickle_pure_python      | 264 us                                                                   | 198 us: 1.34x faster                                                     |
| scimark_lu              | 83.9 ms                                                                  | 63.3 ms: 1.32x faster                                                    |
| async_tree_memoization  | 485 ms                                                                   | 368 ms: 1.32x faster                                                     |
| async_tree_none         | 414 ms                                                                   | 314 ms: 1.32x faster                                                     |
| raytrace                | 267 ms                                                                   | 203 ms: 1.32x faster                                                     |
| thrift                  | 632 us                                                                   | 482 us: 1.31x faster                                                     |
| sqlglot_parse           | 1.22 ms                                                                  | 931 us: 1.31x faster                                                     |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.13 ms: 1.30x faster                                                    |
| pyflate                 | 388 ms                                                                   | 301 ms: 1.29x faster                                                     |
| crypto_pyaes            | 61.4 ms                                                                  | 48.2 ms: 1.27x faster                                                    |
| pycparser               | 873 ms                                                                   | 703 ms: 1.24x faster                                                     |
| scimark_monte_carlo     | 56.0 ms                                                                  | 45.1 ms: 1.24x faster                                                    |
| django_template         | 29.2 ms                                                                  | 23.8 ms: 1.23x faster                                                    |
| async_generators        | 214 ms                                                                   | 176 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 500 ms: 1.21x faster                                                     |
| mypy2                   | 337 ms                                                                   | 280 ms: 1.20x faster                                                     |
| mako                    | 8.69 ms                                                                  | 7.22 ms: 1.20x faster                                                    |
| unpickle_pure_python    | 179 us                                                                   | 150 us: 1.20x faster                                                     |
| hexiom                  | 5.45 ms                                                                  | 4.56 ms: 1.20x faster                                                    |
| chaos                   | 58.4 ms                                                                  | 48.9 ms: 1.20x faster                                                    |
| html5lib                | 47.3 ms                                                                  | 39.8 ms: 1.19x faster                                                    |
| dask                    | 310 ms                                                                   | 261 ms: 1.19x faster                                                     |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 81.1 ms: 1.19x faster                                                    |
| xml_etree_process       | 43.0 ms                                                                  | 36.3 ms: 1.19x faster                                                    |
| json_dumps              | 9.00 ms                                                                  | 7.60 ms: 1.18x faster                                                    |
| tornado_http            | 106 ms                                                                   | 90.1 ms: 1.18x faster                                                    |
| docutils                | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                   |
| pprint_pformat          | 1.23 sec                                                                 | 1.06 sec: 1.16x faster                                                   |
| regex_compile           | 103 ms                                                                   | 89.7 ms: 1.15x faster                                                    |
| create_gc_cycles        | 764 us                                                                   | 664 us: 1.15x faster                                                     |
| deepcopy_memo           | 28.4 us                                                                  | 24.8 us: 1.14x faster                                                    |
| float                   | 59.5 ms                                                                  | 52.6 ms: 1.13x faster                                                    |
| pprint_safe_repr        | 593 ms                                                                   | 526 ms: 1.13x faster                                                     |
| aiohttp                 | 968 us                                                                   | 857 us: 1.13x faster                                                     |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.0 ms: 1.13x faster                                                    |
| bench_thread_pool       | 953 us                                                                   | 848 us: 1.12x faster                                                     |
| sqlglot_optimize        | 38.7 ms                                                                  | 34.7 ms: 1.12x faster                                                    |
| unpickle                | 8.88 us                                                                  | 7.97 us: 1.11x faster                                                    |
| 2to3                    | 229 ms                                                                   | 206 ms: 1.11x faster                                                     |
| dulwich_log             | 47.0 ms                                                                  | 42.5 ms: 1.10x faster                                                    |
| spectral_norm           | 74.3 ms                                                                  | 67.6 ms: 1.10x faster                                                    |
| chameleon               | 5.77 ms                                                                  | 5.27 ms: 1.10x faster                                                    |
| json_loads              | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                    |
| sqlite_synth            | 1.85 us                                                                  | 1.69 us: 1.09x faster                                                    |
| regex_dna               | 131 ms                                                                   | 120 ms: 1.09x faster                                                     |
| sympy_expand            | 313 ms                                                                   | 290 ms: 1.08x faster                                                     |
| sympy_integrate         | 14.7 ms                                                                  | 13.6 ms: 1.08x faster                                                    |
| deepcopy_reduce         | 2.18 us                                                                  | 2.04 us: 1.07x faster                                                    |
| genshi_text             | 18.5 ms                                                                  | 17.3 ms: 1.07x faster                                                    |
| regex_v8                | 15.1 ms                                                                  | 14.3 ms: 1.06x faster                                                    |
| deepcopy                | 256 us                                                                   | 243 us: 1.05x faster                                                     |
| sqlglot_normalize       | 201 ms                                                                   | 191 ms: 1.05x faster                                                     |
| pylint                  | 337 ms                                                                   | 321 ms: 1.05x faster                                                     |
| xml_etree_parse         | 95.6 ms                                                                  | 91.3 ms: 1.05x faster                                                    |
| regex_effbot            | 1.64 ms                                                                  | 1.57 ms: 1.05x faster                                                    |
| python_startup          | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                    |
| comprehensions          | 16.0 us                                                                  | 15.4 us: 1.04x faster                                                    |
| xml_etree_generate      | 53.8 ms                                                                  | 51.8 ms: 1.04x faster                                                    |
| sympy_sum               | 102 ms                                                                   | 98.4 ms: 1.04x faster                                                    |
| sympy_str               | 189 ms                                                                   | 182 ms: 1.04x faster                                                     |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.58 ms: 1.04x faster                                                    |
| coroutines              | 15.6 ms                                                                  | 15.1 ms: 1.03x faster                                                    |
| genshi_xml              | 38.8 ms                                                                  | 37.6 ms: 1.03x faster                                                    |
| pathlib                 | 75.2 ms                                                                  | 73.2 ms: 1.03x faster                                                    |
| nbody                   | 71.5 ms                                                                  | 69.8 ms: 1.02x faster                                                    |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.4 ms: 1.02x faster                                                    |
| unpickle_list           | 2.71 us                                                                  | 2.68 us: 1.01x faster                                                    |
| scimark_fft             | 187 ms                                                                   | 185 ms: 1.01x faster                                                     |
| meteor_contest          | 74.3 ms                                                                  | 74.7 ms: 1.01x slower                                                    |
| pickle                  | 6.67 us                                                                  | 6.73 us: 1.01x slower                                                    |
| nqueens                 | 64.8 ms                                                                  | 65.6 ms: 1.01x slower                                                    |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                     |
| fannkuch                | 252 ms                                                                   | 256 ms: 1.02x slower                                                     |
| python_startup_no_site  | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                    |
| bench_mp_pool           | 59.2 ms                                                                  | 62.0 ms: 1.05x slower                                                    |
| telco                   | 3.77 ms                                                                  | 4.02 ms: 1.07x slower                                                    |
| logging_format          | 6.53 us                                                                  | 6.99 us: 1.07x slower                                                    |
| gc_traversal            | 1.33 ms                                                                  | 1.43 ms: 1.07x slower                                                    |
| asyncio_tcp             | 664 ms                                                                   | 718 ms: 1.08x slower                                                     |
| generators              | 31.4 ms                                                                  | 34.0 ms: 1.08x slower                                                    |
| pickle_list             | 2.57 us                                                                  | 2.78 us: 1.08x slower                                                    |
| mdp                     | 1.60 sec                                                                 | 1.74 sec: 1.09x slower                                                   |
| logging_simple          | 6.12 us                                                                  | 6.67 us: 1.09x slower                                                    |
| pickle_dict             | 16.7 us                                                                  | 18.6 us: 1.11x slower                                                    |
| unpack_sequence         | 39.4 ns                                                                  | 46.0 ns: 1.17x slower                                                    |
| coverage                | 37.5 ms                                                                  | 53.2 ms: 1.42x slower                                                    |
| Geometric mean          | (ref)                                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (2): flaskblogging, json
