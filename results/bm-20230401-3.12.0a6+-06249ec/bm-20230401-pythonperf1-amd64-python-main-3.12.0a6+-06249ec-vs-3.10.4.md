
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 06249ec
- commit date: 2023-04-01
- overall geometric mean: 1.19x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 208 ms: 1.11x faster                                        |
| chameleon      | 5.77 ms                                                                  | 4.75 ms: 1.22x faster                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.19x faster                                      |
| html5lib       | 47.3 ms                                                                  | 36.4 ms: 1.30x faster                                       |
| tornado_http   | 106 ms                                                                   | 88.0 ms: 1.21x faster                                       |
| Geometric mean | (ref)                                                                    | 1.20x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 50.0 ms: 1.19x faster                                       |
| nbody          | 71.5 ms                                                                  | 61.6 ms: 1.16x faster                                       |
| pidigits       | 145 ms                                                                   | 146 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 84.0 ms: 1.23x faster                                       |
| regex_v8       | 15.1 ms                                                                  | 13.2 ms: 1.14x faster                                       |
| regex_dna      | 131 ms                                                                   | 118 ms: 1.11x faster                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.52 ms: 1.08x faster                                       |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.27 ms: 1.71x faster                                       |
| pickle_pure_python   | 264 us                                                                   | 185 us: 1.43x faster                                        |
| unpickle_pure_python | 179 us                                                                   | 126 us: 1.42x faster                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.9 ms: 1.20x faster                                       |
| unpickle             | 8.88 us                                                                  | 8.01 us: 1.11x faster                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 91.4 ms: 1.05x faster                                       |
| json_loads           | 14.2 us                                                                  | 13.7 us: 1.04x faster                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 52.7 ms: 1.02x faster                                       |
| unpickle_list        | 2.71 us                                                                  | 2.82 us: 1.04x slower                                       |
| pickle               | 6.67 us                                                                  | 7.08 us: 1.06x slower                                       |
| pickle_list          | 2.57 us                                                                  | 2.89 us: 1.13x slower                                       |
| pickle_dict          | 16.7 us                                                                  | 19.1 us: 1.14x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.19 ms: 1.40x faster                                       |
| django_template | 29.2 ms                                                                  | 21.4 ms: 1.37x faster                                       |
| genshi_text     | 18.5 ms                                                                  | 14.0 ms: 1.33x faster                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.7 ms: 1.26x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.34x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230401-pythonperf1-amd64-python-main-3.12.0a6+-06249ec |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.95 ms: 2.13x faster                                       |
| go                      | 143 ms                                                                   | 81.9 ms: 1.75x faster                                       |
| logging_silent          | 94.6 ns                                                                  | 54.3 ns: 1.74x faster                                       |
| json_dumps              | 9.00 ms                                                                  | 5.27 ms: 1.71x faster                                       |
| richards                | 41.0 ms                                                                  | 25.5 ms: 1.61x faster                                       |
| scimark_lu              | 83.9 ms                                                                  | 52.6 ms: 1.60x faster                                       |
| mypy2                   | 337 ms                                                                   | 220 ms: 1.53x faster                                        |
| raytrace                | 267 ms                                                                   | 174 ms: 1.53x faster                                        |
| generators              | 31.4 ms                                                                  | 21.2 ms: 1.48x faster                                       |
| pickle_pure_python      | 264 us                                                                   | 185 us: 1.43x faster                                        |
| unpickle_pure_python    | 179 us                                                                   | 126 us: 1.42x faster                                        |
| chaos                   | 58.4 ms                                                                  | 41.5 ms: 1.41x faster                                       |
| mako                    | 8.69 ms                                                                  | 6.19 ms: 1.40x faster                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.9 ms: 1.40x faster                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 869 us: 1.40x faster                                        |
| hexiom                  | 5.45 ms                                                                  | 3.90 ms: 1.40x faster                                       |
| unpack_sequence         | 39.4 ns                                                                  | 28.1 ns: 1.40x faster                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.07 ms: 1.37x faster                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 44.9 ms: 1.37x faster                                       |
| django_template         | 29.2 ms                                                                  | 21.4 ms: 1.37x faster                                       |
| pyflate                 | 388 ms                                                                   | 286 ms: 1.36x faster                                        |
| scimark_sor             | 104 ms                                                                   | 76.7 ms: 1.35x faster                                       |
| asyncio_tcp             | 664 ms                                                                   | 495 ms: 1.34x faster                                        |
| genshi_text             | 18.5 ms                                                                  | 14.0 ms: 1.33x faster                                       |
| async_tree_io           | 1.02 sec                                                                 | 773 ms: 1.32x faster                                        |
| deepcopy_memo           | 28.4 us                                                                  | 21.6 us: 1.32x faster                                       |
| async_tree_memoization  | 485 ms                                                                   | 369 ms: 1.32x faster                                        |
| async_tree_none         | 414 ms                                                                   | 318 ms: 1.30x faster                                        |
| html5lib                | 47.3 ms                                                                  | 36.4 ms: 1.30x faster                                       |
| pycparser               | 873 ms                                                                   | 672 ms: 1.30x faster                                        |
| spectral_norm           | 74.3 ms                                                                  | 57.2 ms: 1.30x faster                                       |
| thrift                  | 632 us                                                                   | 487 us: 1.30x faster                                        |
| pprint_pformat          | 1.23 sec                                                                 | 966 ms: 1.27x faster                                        |
| genshi_xml              | 38.8 ms                                                                  | 30.7 ms: 1.26x faster                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 480 ms: 1.26x faster                                        |
| pprint_safe_repr        | 593 ms                                                                   | 477 ms: 1.25x faster                                        |
| regex_compile           | 103 ms                                                                   | 84.0 ms: 1.23x faster                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.7 ms: 1.22x faster                                       |
| chameleon               | 5.77 ms                                                                  | 4.75 ms: 1.22x faster                                       |
| tornado_http            | 106 ms                                                                   | 88.0 ms: 1.21x faster                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.9 ms: 1.20x faster                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.24 ms: 1.19x faster                                       |
| float                   | 59.5 ms                                                                  | 50.0 ms: 1.19x faster                                       |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.19x faster                                      |
| deepcopy                | 256 us                                                                   | 218 us: 1.17x faster                                        |
| sqlglot_normalize       | 201 ms                                                                   | 173 ms: 1.16x faster                                        |
| nbody                   | 71.5 ms                                                                  | 61.6 ms: 1.16x faster                                       |
| json                    | 3.18 ms                                                                  | 2.77 ms: 1.15x faster                                       |
| regex_v8                | 15.1 ms                                                                  | 13.2 ms: 1.14x faster                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.91 us: 1.14x faster                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.9 ms: 1.14x faster                                       |
| coroutines              | 15.6 ms                                                                  | 13.8 ms: 1.14x faster                                       |
| scimark_fft             | 187 ms                                                                   | 165 ms: 1.13x faster                                        |
| nqueens                 | 64.8 ms                                                                  | 57.4 ms: 1.13x faster                                       |
| bench_thread_pool       | 953 us                                                                   | 845 us: 1.13x faster                                        |
| sympy_expand            | 313 ms                                                                   | 278 ms: 1.13x faster                                        |
| mdp                     | 1.60 sec                                                                 | 1.43 sec: 1.12x faster                                      |
| dulwich_log             | 47.0 ms                                                                  | 42.3 ms: 1.11x faster                                       |
| unpickle                | 8.88 us                                                                  | 8.01 us: 1.11x faster                                       |
| regex_dna               | 131 ms                                                                   | 118 ms: 1.11x faster                                        |
| 2to3                    | 229 ms                                                                   | 208 ms: 1.11x faster                                        |
| create_gc_cycles        | 764 us                                                                   | 695 us: 1.10x faster                                        |
| fannkuch                | 252 ms                                                                   | 232 ms: 1.08x faster                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.52 ms: 1.08x faster                                       |
| sympy_str               | 189 ms                                                                   | 177 ms: 1.06x faster                                        |
| comprehensions          | 16.0 us                                                                  | 15.2 us: 1.05x faster                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 91.4 ms: 1.05x faster                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.4 ms: 1.04x faster                                       |
| json_loads              | 14.2 us                                                                  | 13.7 us: 1.04x faster                                       |
| sympy_sum               | 102 ms                                                                   | 99.7 ms: 1.03x faster                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 52.7 ms: 1.02x faster                                       |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                       |
| pidigits                | 145 ms                                                                   | 146 ms: 1.01x slower                                        |
| sqlite_synth            | 1.85 us                                                                  | 1.87 us: 1.01x slower                                       |
| logging_format          | 6.53 us                                                                  | 6.68 us: 1.02x slower                                       |
| telco                   | 3.77 ms                                                                  | 3.91 ms: 1.04x slower                                       |
| unpickle_list           | 2.71 us                                                                  | 2.82 us: 1.04x slower                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                       |
| pickle                  | 6.67 us                                                                  | 7.08 us: 1.06x slower                                       |
| pickle_list             | 2.57 us                                                                  | 2.89 us: 1.13x slower                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 67.0 ms: 1.13x slower                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.51 ms: 1.14x slower                                       |
| pickle_dict             | 16.7 us                                                                  | 19.1 us: 1.14x slower                                       |
| pathlib                 | 75.2 ms                                                                  | 86.3 ms: 1.15x slower                                       |
| dask                    | 310 ms                                                                   | 362 ms: 1.17x slower                                        |
| coverage                | 37.5 ms                                                                  | 52.8 ms: 1.41x slower                                       |
| Geometric mean          | (ref)                                                                    | 1.19x faster                                                |

Benchmark hidden because not significant (2): logging_simple, async_generators
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
