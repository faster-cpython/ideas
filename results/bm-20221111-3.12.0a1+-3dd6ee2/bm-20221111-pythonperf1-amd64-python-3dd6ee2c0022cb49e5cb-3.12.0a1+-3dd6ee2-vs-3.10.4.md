
# Results vs. 3.10.4

- fork: python
- ref: 3dd6ee2c0022cb49e5cb
- machine: windows-amd64
- commit hash: 3dd6ee2
- commit date: 2022-11-11
- overall geometric mean: 1.16x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.13x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.68 ms: 1.23x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 36.8 ms: 1.29x faster                                                       |
| tornado_http   | 106 ms                                                                   | 92.6 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.19x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 50.8 ms: 1.17x faster                                                       |
| nbody          | 71.5 ms                                                                  | 64.7 ms: 1.11x faster                                                       |
| pidigits       | 145 ms                                                                   | 150 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 84.4 ms: 1.23x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 13.9 ms: 1.09x faster                                                       |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.09x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.19 ms: 1.73x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 189 us: 1.40x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 131 us: 1.37x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.7 ms: 1.20x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.01 us: 1.11x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 88.9 ms: 1.07x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.90 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 64.8 ms: 1.04x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.4 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.11x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.5 ms: 1.04x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.37 ms: 1.36x faster                                                       |
| django_template | 29.2 ms                                                                  | 22.4 ms: 1.30x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 14.8 ms: 1.25x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 33.2 ms: 1.17x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.27x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1+-3dd6ee2 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.29 ms: 1.81x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.19 ms: 1.73x faster                                                       |
| go                      | 143 ms                                                                   | 88.3 ms: 1.62x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 60.7 ns: 1.56x faster                                                       |
| richards                | 41.0 ms                                                                  | 26.8 ms: 1.53x faster                                                       |
| mypy2                   | 337 ms                                                                   | 221 ms: 1.53x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 69.9 ms: 1.48x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 57.6 ms: 1.46x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.6 ms: 1.41x faster                                                       |
| raytrace                | 267 ms                                                                   | 190 ms: 1.41x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 189 us: 1.40x faster                                                        |
| pyflate                 | 388 ms                                                                   | 280 ms: 1.39x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 131 us: 1.37x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.37 ms: 1.36x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.4 ms: 1.35x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 908 us: 1.34x faster                                                        |
| pycparser               | 873 ms                                                                   | 653 ms: 1.34x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.10 ms: 1.33x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.15 ms: 1.31x faster                                                       |
| thrift                  | 632 us                                                                   | 486 us: 1.30x faster                                                        |
| django_template         | 29.2 ms                                                                  | 22.4 ms: 1.30x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 45.1 ms: 1.30x faster                                                       |
| unpack_sequence         | 39.4 ns                                                                  | 30.6 ns: 1.29x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 36.8 ms: 1.29x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 804 ms: 1.27x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 382 ms: 1.27x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 22.6 us: 1.26x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 14.8 ms: 1.25x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 985 ms: 1.25x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 478 ms: 1.24x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 334 ms: 1.24x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.68 ms: 1.23x faster                                                       |
| regex_compile           | 103 ms                                                                   | 84.4 ms: 1.23x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.7 ms: 1.20x faster                                                       |
| dask                    | 310 ms                                                                   | 261 ms: 1.19x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.70 ms: 1.18x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.18x faster                                                      |
| async_generators        | 214 ms                                                                   | 183 ms: 1.17x faster                                                        |
| float                   | 59.5 ms                                                                  | 50.8 ms: 1.17x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 33.0 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 517 ms: 1.17x faster                                                        |
| genshi_xml              | 38.8 ms                                                                  | 33.2 ms: 1.17x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 63.6 ms: 1.17x faster                                                       |
| deepcopy                | 256 us                                                                   | 223 us: 1.15x faster                                                        |
| tornado_http            | 106 ms                                                                   | 92.6 ms: 1.15x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.2 ms: 1.14x faster                                                       |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.13x faster                                                        |
| sqlglot_normalize       | 201 ms                                                                   | 178 ms: 1.13x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.93 us: 1.13x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 852 us: 1.12x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.40 ms: 1.11x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 689 us: 1.11x faster                                                        |
| unpickle                | 8.88 us                                                                  | 8.01 us: 1.11x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 169 ms: 1.11x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 64.7 ms: 1.11x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 286 ms: 1.09x faster                                                        |
| json_loads              | 14.2 us                                                                  | 13.0 us: 1.09x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 13.9 ms: 1.09x faster                                                       |
| sympy_str               | 189 ms                                                                   | 174 ms: 1.09x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.5 ms: 1.09x faster                                                       |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.09x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 88.9 ms: 1.07x faster                                                       |
| fannkuch                | 252 ms                                                                   | 235 ms: 1.07x faster                                                        |
| coroutines              | 15.6 ms                                                                  | 14.9 ms: 1.05x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.76 us: 1.05x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 62.1 ms: 1.04x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.57 ms: 1.04x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 51.7 ms: 1.04x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.5 ms: 1.04x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 71.5 ms: 1.04x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 98.8 ms: 1.03x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 73.8 ms: 1.02x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.58 sec: 1.02x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 15.8 us: 1.01x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.83 ms: 1.01x slower                                                       |
| pidigits                | 145 ms                                                                   | 150 ms: 1.03x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.90 us: 1.03x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.8 ms: 1.04x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.40 us: 1.04x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.85 us: 1.05x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.0 ms: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.79 us: 1.09x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.48 ms: 1.11x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 765 ms: 1.15x slower                                                        |
| pickle_dict             | 16.7 us                                                                  | 19.4 us: 1.16x slower                                                       |
| generators              | 31.4 ms                                                                  | 37.3 ms: 1.19x slower                                                       |
| coverage                | 37.5 ms                                                                  | 55.5 ms: 1.48x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.16x faster                                                                |
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
