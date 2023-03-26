
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 30a306c
- commit date: 2023-03-25
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 198 ms: 1.16x faster                                        |
| chameleon      | 5.77 ms                                                                  | 4.57 ms: 1.26x faster                                       |
| docutils       | 1.83 sec                                                                 | 1.52 sec: 1.21x faster                                      |
| html5lib       | 47.3 ms                                                                  | 35.5 ms: 1.33x faster                                       |
| tornado_http   | 106 ms                                                                   | 87.7 ms: 1.21x faster                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 56.6 ms: 1.26x faster                                       |
| float          | 59.5 ms                                                                  | 48.6 ms: 1.22x faster                                       |
| pidigits       | 145 ms                                                                   | 145 ms: 1.00x faster                                        |
| Geometric mean | (ref)                                                                    | 1.16x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 82.3 ms: 1.26x faster                                       |
| regex_v8       | 15.1 ms                                                                  | 13.6 ms: 1.11x faster                                       |
| regex_dna      | 131 ms                                                                   | 119 ms: 1.10x faster                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.77 ms: 1.08x slower                                       |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.58 ms: 1.61x faster                                       |
| pickle_pure_python   | 264 us                                                                   | 176 us: 1.50x faster                                        |
| unpickle_pure_python | 179 us                                                                   | 122 us: 1.47x faster                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.3 ms: 1.22x faster                                       |
| unpickle             | 8.88 us                                                                  | 7.97 us: 1.11x faster                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 89.5 ms: 1.07x faster                                       |
| json_loads           | 14.2 us                                                                  | 13.4 us: 1.06x faster                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 60.4 ms: 1.04x faster                                       |
| unpickle_list        | 2.71 us                                                                  | 2.66 us: 1.02x faster                                       |
| pickle               | 6.67 us                                                                  | 7.04 us: 1.06x slower                                       |
| pickle_dict          | 16.7 us                                                                  | 18.7 us: 1.12x slower                                       |
| pickle_list          | 2.57 us                                                                  | 2.91 us: 1.14x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.6 ms: 1.04x faster                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.6 ms: 1.42x faster                                       |
| mako            | 8.69 ms                                                                  | 6.32 ms: 1.38x faster                                       |
| genshi_text     | 18.5 ms                                                                  | 13.6 ms: 1.36x faster                                       |
| genshi_xml      | 38.8 ms                                                                  | 30.3 ms: 1.28x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.36x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-pythonperf1-amd64-python-main-3.12.0a6+-30a306c |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.94 ms: 2.14x faster                                       |
| logging_silent          | 94.6 ns                                                                  | 54.4 ns: 1.74x faster                                       |
| go                      | 143 ms                                                                   | 82.6 ms: 1.73x faster                                       |
| richards                | 41.0 ms                                                                  | 25.1 ms: 1.64x faster                                       |
| json_dumps              | 9.00 ms                                                                  | 5.58 ms: 1.61x faster                                       |
| scimark_lu              | 83.9 ms                                                                  | 52.6 ms: 1.60x faster                                       |
| mypy2                   | 337 ms                                                                   | 212 ms: 1.59x faster                                        |
| raytrace                | 267 ms                                                                   | 171 ms: 1.57x faster                                        |
| pickle_pure_python      | 264 us                                                                   | 176 us: 1.50x faster                                        |
| generators              | 31.4 ms                                                                  | 21.0 ms: 1.50x faster                                       |
| unpickle_pure_python    | 179 us                                                                   | 122 us: 1.47x faster                                        |
| chaos                   | 58.4 ms                                                                  | 40.2 ms: 1.45x faster                                       |
| unpack_sequence         | 39.4 ns                                                                  | 27.2 ns: 1.45x faster                                       |
| hexiom                  | 5.45 ms                                                                  | 3.80 ms: 1.43x faster                                       |
| asyncio_tcp             | 664 ms                                                                   | 467 ms: 1.42x faster                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.5 ms: 1.42x faster                                       |
| django_template         | 29.2 ms                                                                  | 20.6 ms: 1.42x faster                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 864 us: 1.41x faster                                        |
| async_tree_none         | 414 ms                                                                   | 295 ms: 1.40x faster                                        |
| async_tree_io           | 1.02 sec                                                                 | 731 ms: 1.40x faster                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.05 ms: 1.40x faster                                       |
| pyflate                 | 388 ms                                                                   | 281 ms: 1.38x faster                                        |
| mako                    | 8.69 ms                                                                  | 6.32 ms: 1.38x faster                                       |
| thrift                  | 632 us                                                                   | 461 us: 1.37x faster                                        |
| async_tree_memoization  | 485 ms                                                                   | 355 ms: 1.37x faster                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 45.0 ms: 1.37x faster                                       |
| pycparser               | 873 ms                                                                   | 641 ms: 1.36x faster                                        |
| genshi_text             | 18.5 ms                                                                  | 13.6 ms: 1.36x faster                                       |
| scimark_sor             | 104 ms                                                                   | 76.4 ms: 1.35x faster                                       |
| html5lib                | 47.3 ms                                                                  | 35.5 ms: 1.33x faster                                       |
| deepcopy_memo           | 28.4 us                                                                  | 21.5 us: 1.32x faster                                       |
| pprint_pformat          | 1.23 sec                                                                 | 941 ms: 1.30x faster                                        |
| pprint_safe_repr        | 593 ms                                                                   | 458 ms: 1.30x faster                                        |
| genshi_xml              | 38.8 ms                                                                  | 30.3 ms: 1.28x faster                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 475 ms: 1.27x faster                                        |
| chameleon               | 5.77 ms                                                                  | 4.57 ms: 1.26x faster                                       |
| nbody                   | 71.5 ms                                                                  | 56.6 ms: 1.26x faster                                       |
| regex_compile           | 103 ms                                                                   | 82.3 ms: 1.26x faster                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.5 ms: 1.23x faster                                       |
| float                   | 59.5 ms                                                                  | 48.6 ms: 1.22x faster                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.3 ms: 1.22x faster                                       |
| tornado_http            | 106 ms                                                                   | 87.7 ms: 1.21x faster                                       |
| docutils                | 1.83 sec                                                                 | 1.52 sec: 1.21x faster                                      |
| deepcopy                | 256 us                                                                   | 212 us: 1.21x faster                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.83 us: 1.19x faster                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.25 ms: 1.18x faster                                       |
| sqlglot_normalize       | 201 ms                                                                   | 171 ms: 1.18x faster                                        |
| mdp                     | 1.60 sec                                                                 | 1.37 sec: 1.17x faster                                      |
| json                    | 3.18 ms                                                                  | 2.75 ms: 1.16x faster                                       |
| 2to3                    | 229 ms                                                                   | 198 ms: 1.16x faster                                        |
| nqueens                 | 64.8 ms                                                                  | 56.7 ms: 1.14x faster                                       |
| bench_thread_pool       | 953 us                                                                   | 833 us: 1.14x faster                                        |
| sympy_integrate         | 14.7 ms                                                                  | 12.8 ms: 1.14x faster                                       |
| create_gc_cycles        | 764 us                                                                   | 671 us: 1.14x faster                                        |
| spectral_norm           | 74.3 ms                                                                  | 65.4 ms: 1.14x faster                                       |
| scimark_fft             | 187 ms                                                                   | 165 ms: 1.13x faster                                        |
| sympy_expand            | 313 ms                                                                   | 278 ms: 1.12x faster                                        |
| unpickle                | 8.88 us                                                                  | 7.97 us: 1.11x faster                                       |
| fannkuch                | 252 ms                                                                   | 227 ms: 1.11x faster                                        |
| regex_v8                | 15.1 ms                                                                  | 13.6 ms: 1.11x faster                                       |
| regex_dna               | 131 ms                                                                   | 119 ms: 1.10x faster                                        |
| dulwich_log             | 47.0 ms                                                                  | 43.0 ms: 1.09x faster                                       |
| coroutines              | 15.6 ms                                                                  | 14.4 ms: 1.09x faster                                       |
| sympy_str               | 189 ms                                                                   | 174 ms: 1.08x faster                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 89.5 ms: 1.07x faster                                       |
| comprehensions          | 16.0 us                                                                  | 15.0 us: 1.06x faster                                       |
| json_loads              | 14.2 us                                                                  | 13.4 us: 1.06x faster                                       |
| sympy_sum               | 102 ms                                                                   | 96.8 ms: 1.06x faster                                       |
| meteor_contest          | 74.3 ms                                                                  | 70.9 ms: 1.05x faster                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 60.4 ms: 1.04x faster                                       |
| python_startup          | 19.3 ms                                                                  | 18.6 ms: 1.04x faster                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.78 us: 1.03x faster                                       |
| logging_format          | 6.53 us                                                                  | 6.35 us: 1.03x faster                                       |
| logging_simple          | 6.12 us                                                                  | 5.99 us: 1.02x faster                                       |
| unpickle_list           | 2.71 us                                                                  | 2.66 us: 1.02x faster                                       |
| async_generators        | 214 ms                                                                   | 213 ms: 1.01x faster                                        |
| pidigits                | 145 ms                                                                   | 145 ms: 1.00x faster                                        |
| telco                   | 3.77 ms                                                                  | 3.83 ms: 1.01x slower                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.7 ms: 1.06x slower                                       |
| pickle                  | 6.67 us                                                                  | 7.04 us: 1.06x slower                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.77 ms: 1.08x slower                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.45 ms: 1.09x slower                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 64.8 ms: 1.09x slower                                       |
| pathlib                 | 75.2 ms                                                                  | 84.2 ms: 1.12x slower                                       |
| pickle_dict             | 16.7 us                                                                  | 18.7 us: 1.12x slower                                       |
| pickle_list             | 2.57 us                                                                  | 2.91 us: 1.14x slower                                       |
| dask                    | 310 ms                                                                   | 354 ms: 1.14x slower                                        |
| coverage                | 37.5 ms                                                                  | 51.5 ms: 1.38x slower                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                |
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
