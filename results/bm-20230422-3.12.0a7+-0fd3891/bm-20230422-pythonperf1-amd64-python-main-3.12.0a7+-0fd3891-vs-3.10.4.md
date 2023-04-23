
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: windows-amd64
- commit hash: 0fd3891
- commit date: 2023-04-22
- overall geometric mean: 1.17x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 207 ms: 1.11x faster                                        |
| chameleon      | 5.77 ms                                                                  | 4.93 ms: 1.17x faster                                       |
| docutils       | 1.83 sec                                                                 | 1.54 sec: 1.19x faster                                      |
| html5lib       | 47.3 ms                                                                  | 36.6 ms: 1.29x faster                                       |
| tornado_http   | 106 ms                                                                   | 90.0 ms: 1.18x faster                                       |
| Geometric mean | (ref)                                                                    | 1.19x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 51.4 ms: 1.16x faster                                       |
| pidigits       | 145 ms                                                                   | 148 ms: 1.02x slower                                        |
| nbody          | 71.5 ms                                                                  | 73.1 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 83.8 ms: 1.23x faster                                       |
| regex_v8       | 15.1 ms                                                                  | 13.0 ms: 1.16x faster                                       |
| regex_dna      | 131 ms                                                                   | 115 ms: 1.14x faster                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.51 ms: 1.09x faster                                       |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.41 ms: 1.66x faster                                       |
| pickle_pure_python   | 264 us                                                                   | 189 us: 1.40x faster                                        |
| unpickle_pure_python | 179 us                                                                   | 135 us: 1.33x faster                                        |
| xml_etree_process    | 43.0 ms                                                                  | 37.4 ms: 1.15x faster                                       |
| json_loads           | 14.2 us                                                                  | 12.8 us: 1.11x faster                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 87.5 ms: 1.09x faster                                       |
| unpickle             | 8.88 us                                                                  | 8.46 us: 1.05x faster                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 60.0 ms: 1.04x faster                                       |
| unpickle_list        | 2.71 us                                                                  | 2.63 us: 1.03x faster                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 54.4 ms: 1.01x slower                                       |
| pickle               | 6.67 us                                                                  | 6.77 us: 1.02x slower                                       |
| pickle_dict          | 16.7 us                                                                  | 18.2 us: 1.09x slower                                       |
| pickle_list          | 2.57 us                                                                  | 2.81 us: 1.09x slower                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                       |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 21.8 ms: 1.34x faster                                       |
| mako            | 8.69 ms                                                                  | 6.66 ms: 1.31x faster                                       |
| genshi_text     | 18.5 ms                                                                  | 15.1 ms: 1.23x faster                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.5 ms: 1.19x faster                                       |
| Geometric mean  | (ref)                                                                    | 1.26x faster                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230422-pythonperf1-amd64-python-main-3.12.0a7+-0fd3891 |
|-------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.16 ms: 1.92x faster                                       |
| json_dumps              | 9.00 ms                                                                  | 5.41 ms: 1.66x faster                                       |
| go                      | 143 ms                                                                   | 87.4 ms: 1.64x faster                                       |
| logging_silent          | 94.6 ns                                                                  | 59.5 ns: 1.59x faster                                       |
| mypy2                   | 337 ms                                                                   | 215 ms: 1.57x faster                                        |
| scimark_lu              | 83.9 ms                                                                  | 54.2 ms: 1.55x faster                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 789 us: 1.54x faster                                        |
| richards                | 41.0 ms                                                                  | 27.1 ms: 1.51x faster                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 991 us: 1.48x faster                                        |
| generators              | 31.4 ms                                                                  | 21.7 ms: 1.45x faster                                       |
| raytrace                | 267 ms                                                                   | 185 ms: 1.44x faster                                        |
| asyncio_tcp             | 664 ms                                                                   | 470 ms: 1.41x faster                                        |
| pickle_pure_python      | 264 us                                                                   | 189 us: 1.40x faster                                        |
| async_tree_none         | 414 ms                                                                   | 298 ms: 1.39x faster                                        |
| async_tree_io           | 1.02 sec                                                                 | 748 ms: 1.37x faster                                        |
| pyflate                 | 388 ms                                                                   | 286 ms: 1.36x faster                                        |
| async_tree_memoization  | 485 ms                                                                   | 357 ms: 1.36x faster                                        |
| chaos                   | 58.4 ms                                                                  | 43.3 ms: 1.35x faster                                       |
| django_template         | 29.2 ms                                                                  | 21.8 ms: 1.34x faster                                       |
| thrift                  | 632 us                                                                   | 474 us: 1.33x faster                                        |
| unpickle_pure_python    | 179 us                                                                   | 135 us: 1.33x faster                                        |
| hexiom                  | 5.45 ms                                                                  | 4.10 ms: 1.33x faster                                       |
| pycparser               | 873 ms                                                                   | 658 ms: 1.33x faster                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 46.4 ms: 1.32x faster                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 42.7 ms: 1.31x faster                                       |
| mako                    | 8.69 ms                                                                  | 6.66 ms: 1.31x faster                                       |
| html5lib                | 47.3 ms                                                                  | 36.6 ms: 1.29x faster                                       |
| scimark_sor             | 104 ms                                                                   | 80.8 ms: 1.28x faster                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 474 ms: 1.27x faster                                        |
| deepcopy_memo           | 28.4 us                                                                  | 23.0 us: 1.24x faster                                       |
| regex_compile           | 103 ms                                                                   | 83.8 ms: 1.23x faster                                       |
| pprint_pformat          | 1.23 sec                                                                 | 995 ms: 1.23x faster                                        |
| genshi_text             | 18.5 ms                                                                  | 15.1 ms: 1.23x faster                                       |
| pylint                  | 337 ms                                                                   | 276 ms: 1.22x faster                                        |
| pprint_safe_repr        | 593 ms                                                                   | 491 ms: 1.21x faster                                        |
| spectral_norm           | 74.3 ms                                                                  | 61.6 ms: 1.21x faster                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.5 ms: 1.19x faster                                       |
| docutils                | 1.83 sec                                                                 | 1.54 sec: 1.19x faster                                      |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.6 ms: 1.19x faster                                       |
| tornado_http            | 106 ms                                                                   | 90.0 ms: 1.18x faster                                       |
| bench_thread_pool       | 953 us                                                                   | 813 us: 1.17x faster                                        |
| chameleon               | 5.77 ms                                                                  | 4.93 ms: 1.17x faster                                       |
| float                   | 59.5 ms                                                                  | 51.4 ms: 1.16x faster                                       |
| regex_v8                | 15.1 ms                                                                  | 13.0 ms: 1.16x faster                                       |
| xml_etree_process       | 43.0 ms                                                                  | 37.4 ms: 1.15x faster                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.33 ms: 1.15x faster                                       |
| sqlglot_normalize       | 201 ms                                                                   | 176 ms: 1.14x faster                                        |
| regex_dna               | 131 ms                                                                   | 115 ms: 1.14x faster                                        |
| dulwich_log             | 47.0 ms                                                                  | 41.3 ms: 1.14x faster                                       |
| coroutines              | 15.6 ms                                                                  | 13.8 ms: 1.14x faster                                       |
| nqueens                 | 64.8 ms                                                                  | 57.3 ms: 1.13x faster                                       |
| create_gc_cycles        | 764 us                                                                   | 677 us: 1.13x faster                                        |
| json                    | 3.18 ms                                                                  | 2.82 ms: 1.13x faster                                       |
| deepcopy                | 256 us                                                                   | 227 us: 1.13x faster                                        |
| sympy_expand            | 313 ms                                                                   | 278 ms: 1.12x faster                                        |
| json_loads              | 14.2 us                                                                  | 12.8 us: 1.11x faster                                       |
| mdp                     | 1.60 sec                                                                 | 1.44 sec: 1.11x faster                                      |
| sympy_integrate         | 14.7 ms                                                                  | 13.2 ms: 1.11x faster                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.97 us: 1.11x faster                                       |
| 2to3                    | 229 ms                                                                   | 207 ms: 1.11x faster                                        |
| sympy_str               | 189 ms                                                                   | 171 ms: 1.10x faster                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 87.5 ms: 1.09x faster                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.51 ms: 1.09x faster                                       |
| scimark_fft             | 187 ms                                                                   | 172 ms: 1.08x faster                                        |
| comprehensions          | 16.0 us                                                                  | 15.0 us: 1.07x faster                                       |
| sympy_sum               | 102 ms                                                                   | 96.1 ms: 1.06x faster                                       |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                       |
| unpack_sequence         | 39.4 ns                                                                  | 37.4 ns: 1.05x faster                                       |
| unpickle                | 8.88 us                                                                  | 8.46 us: 1.05x faster                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 60.0 ms: 1.04x faster                                       |
| fannkuch                | 252 ms                                                                   | 243 ms: 1.04x faster                                        |
| unpickle_list           | 2.71 us                                                                  | 2.63 us: 1.03x faster                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.81 us: 1.02x faster                                       |
| async_generators        | 214 ms                                                                   | 216 ms: 1.01x slower                                        |
| telco                   | 3.77 ms                                                                  | 3.80 ms: 1.01x slower                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 54.4 ms: 1.01x slower                                       |
| pickle                  | 6.67 us                                                                  | 6.77 us: 1.02x slower                                       |
| logging_simple          | 6.12 us                                                                  | 6.25 us: 1.02x slower                                       |
| pidigits                | 145 ms                                                                   | 148 ms: 1.02x slower                                        |
| logging_format          | 6.53 us                                                                  | 6.67 us: 1.02x slower                                       |
| nbody                   | 71.5 ms                                                                  | 73.1 ms: 1.02x slower                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                       |
| meteor_contest          | 74.3 ms                                                                  | 77.8 ms: 1.05x slower                                       |
| pickle_dict             | 16.7 us                                                                  | 18.2 us: 1.09x slower                                       |
| pickle_list             | 2.57 us                                                                  | 2.81 us: 1.09x slower                                       |
| pathlib                 | 75.2 ms                                                                  | 82.4 ms: 1.10x slower                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.47 ms: 1.10x slower                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 66.7 ms: 1.13x slower                                       |
| dask                    | 310 ms                                                                   | 357 ms: 1.15x slower                                        |
| coverage                | 37.5 ms                                                                  | 50.5 ms: 1.35x slower                                       |
| Geometric mean          | (ref)                                                                    | 1.17x faster                                                |
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
