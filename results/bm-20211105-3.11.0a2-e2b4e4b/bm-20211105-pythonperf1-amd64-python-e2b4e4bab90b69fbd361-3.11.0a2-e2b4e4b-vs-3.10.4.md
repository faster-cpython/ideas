
# Results vs. 3.10.4

- fork: python
- ref: e2b4e4bab90b69fbd361
- machine: windows-amd64
- commit hash: e2b4e4b
- commit date: 2021-11-05
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 210 ms: 1.09x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 5.53 ms: 1.04x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.67 sec: 1.10x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 41.4 ms: 1.14x faster                                                      |
| tornado_http   | 106 ms                                                                   | 98.3 ms: 1.08x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 56.1 ms: 1.06x faster                                                      |
| pidigits       | 145 ms                                                                   | 148 ms: 1.02x slower                                                       |
| nbody          | 71.5 ms                                                                  | 90.3 ms: 1.26x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.07x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 90.4 ms: 1.14x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 16.6 ms: 1.10x slower                                                      |
| regex_effbot   | 1.64 ms                                                                  | 1.82 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 228 us: 1.16x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.81 us: 1.14x faster                                                      |
| json_dumps           | 9.00 ms                                                                  | 7.94 ms: 1.13x faster                                                      |
| xml_etree_process    | 43.0 ms                                                                  | 39.7 ms: 1.08x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.54 us: 1.07x faster                                                      |
| unpickle_pure_python | 179 us                                                                   | 168 us: 1.07x faster                                                       |
| pickle_list          | 2.57 us                                                                  | 2.49 us: 1.03x faster                                                      |
| pickle_dict          | 16.7 us                                                                  | 16.2 us: 1.03x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 93.8 ms: 1.02x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.61 us: 1.01x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 54.7 ms: 1.02x slower                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 65.2 ms: 1.04x slower                                                      |
| json_loads           | 14.2 us                                                                  | 14.9 us: 1.05x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.8 ms: 1.02x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.1 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 26.0 ms: 1.12x faster                                                      |
| mako            | 8.69 ms                                                                  | 8.07 ms: 1.08x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 17.5 ms: 1.06x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.07x faster                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.86 ms: 1.45x faster                                                      |
| go                      | 143 ms                                                                   | 106 ms: 1.35x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 307 ms: 1.35x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 72.1 ns: 1.31x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 793 ms: 1.29x faster                                                       |
| raytrace                | 267 ms                                                                   | 214 ms: 1.25x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 395 ms: 1.23x faster                                                       |
| richards                | 41.0 ms                                                                  | 34.0 ms: 1.21x faster                                                      |
| thrift                  | 632 us                                                                   | 528 us: 1.20x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 228 us: 1.16x faster                                                       |
| regex_compile           | 103 ms                                                                   | 90.4 ms: 1.14x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 41.4 ms: 1.14x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 530 ms: 1.14x faster                                                       |
| unpickle                | 8.88 us                                                                  | 7.81 us: 1.14x faster                                                      |
| pycparser               | 873 ms                                                                   | 769 ms: 1.14x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 7.94 ms: 1.13x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 5.45 us: 1.12x faster                                                      |
| django_template         | 29.2 ms                                                                  | 26.0 ms: 1.12x faster                                                      |
| async_generators        | 214 ms                                                                   | 192 ms: 1.12x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 686 us: 1.11x faster                                                       |
| logging_format          | 6.53 us                                                                  | 5.92 us: 1.10x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.67 sec: 1.10x faster                                                     |
| pprint_pformat          | 1.23 sec                                                                 | 1.13 sec: 1.09x faster                                                     |
| 2to3                    | 229 ms                                                                   | 210 ms: 1.09x faster                                                       |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 88.5 ms: 1.09x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 547 ms: 1.08x faster                                                       |
| pyflate                 | 388 ms                                                                   | 358 ms: 1.08x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 53.9 ms: 1.08x faster                                                      |
| scimark_monte_carlo     | 56.0 ms                                                                  | 51.7 ms: 1.08x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 39.7 ms: 1.08x faster                                                      |
| tornado_http            | 106 ms                                                                   | 98.3 ms: 1.08x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 5.06 ms: 1.08x faster                                                      |
| mako                    | 8.69 ms                                                                  | 8.07 ms: 1.08x faster                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.54 us: 1.07x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 168 us: 1.07x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 44.1 ms: 1.07x faster                                                      |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.6 ms: 1.06x faster                                                      |
| float                   | 59.5 ms                                                                  | 56.1 ms: 1.06x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 17.5 ms: 1.06x faster                                                      |
| dask                    | 310 ms                                                                   | 295 ms: 1.05x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 906 us: 1.05x faster                                                       |
| pylint                  | 337 ms                                                                   | 321 ms: 1.05x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 58.9 ms: 1.04x faster                                                      |
| chameleon               | 5.77 ms                                                                  | 5.53 ms: 1.04x faster                                                      |
| json                    | 3.18 ms                                                                  | 3.06 ms: 1.04x faster                                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 37.5 ms: 1.03x faster                                                      |
| pickle_list             | 2.57 us                                                                  | 2.49 us: 1.03x faster                                                      |
| scimark_lu              | 83.9 ms                                                                  | 81.5 ms: 1.03x faster                                                      |
| pickle_dict             | 16.7 us                                                                  | 16.2 us: 1.03x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.03x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 73.4 ms: 1.02x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 196 ms: 1.02x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.8 ms: 1.02x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 101 ms: 1.02x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 14.4 ms: 1.02x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 93.8 ms: 1.02x faster                                                      |
| generators              | 31.4 ms                                                                  | 31.0 ms: 1.01x faster                                                      |
| deepcopy_memo           | 28.4 us                                                                  | 28.1 us: 1.01x faster                                                      |
| pickle                  | 6.67 us                                                                  | 6.61 us: 1.01x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 311 ms: 1.01x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.61 sec: 1.01x slower                                                     |
| sympy_str               | 189 ms                                                                   | 191 ms: 1.01x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.1 ms: 1.01x slower                                                      |
| pidigits                | 145 ms                                                                   | 148 ms: 1.02x slower                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 54.7 ms: 1.02x slower                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.50 ms: 1.02x slower                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 2.23 us: 1.02x slower                                                      |
| meteor_contest          | 74.3 ms                                                                  | 76.2 ms: 1.03x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.37 ms: 1.03x slower                                                      |
| telco                   | 3.77 ms                                                                  | 3.91 ms: 1.04x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 61.4 ms: 1.04x slower                                                      |
| nqueens                 | 64.8 ms                                                                  | 67.3 ms: 1.04x slower                                                      |
| deepcopy                | 256 us                                                                   | 266 us: 1.04x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 65.2 ms: 1.04x slower                                                      |
| asyncio_tcp             | 664 ms                                                                   | 695 ms: 1.05x slower                                                       |
| json_loads              | 14.2 us                                                                  | 14.9 us: 1.05x slower                                                      |
| sqlglot_parse           | 1.22 ms                                                                  | 1.29 ms: 1.06x slower                                                      |
| fannkuch                | 252 ms                                                                   | 275 ms: 1.09x slower                                                       |
| regex_v8                | 15.1 ms                                                                  | 16.6 ms: 1.10x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.82 ms: 1.11x slower                                                      |
| spectral_norm           | 74.3 ms                                                                  | 82.7 ms: 1.11x slower                                                      |
| scimark_fft             | 187 ms                                                                   | 212 ms: 1.14x slower                                                       |
| coroutines              | 15.6 ms                                                                  | 18.1 ms: 1.16x slower                                                      |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 3.18 ms: 1.19x slower                                                      |
| comprehensions          | 16.0 us                                                                  | 19.1 us: 1.19x slower                                                      |
| nbody                   | 71.5 ms                                                                  | 90.3 ms: 1.26x slower                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 51.9 ns: 1.32x slower                                                      |
| coverage                | 37.5 ms                                                                  | 262 ms: 6.99x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.02x faster                                                               |

Benchmark hidden because not significant (4): genshi_xml, sympy_sum, flaskblogging, regex_dna
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, mypy2
