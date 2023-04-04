
# Results vs. 3.10.4

- fork: python
- ref: cdde29dde90947df9bac
- machine: windows-amd64
- commit hash: cdde29d
- commit date: 2022-11-21
- overall geometric mean: 1.19x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 194 ms: 1.18x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.62 ms: 1.25x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 34.8 ms: 1.36x faster                                                       |
| tornado_http   | 106 ms                                                                   | 88.1 ms: 1.21x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 59.0 ms: 1.21x faster                                                       |
| float          | 59.5 ms                                                                  | 51.0 ms: 1.17x faster                                                       |
| pidigits       | 145 ms                                                                   | 148 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 81.1 ms: 1.28x faster                                                       |
| regex_dna      | 131 ms                                                                   | 118 ms: 1.11x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 13.9 ms: 1.09x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.35 ms: 1.68x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 177 us: 1.49x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 131 us: 1.37x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 33.6 ms: 1.28x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 48.4 ms: 1.11x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 91.0 ms: 1.05x faster                                                       |
| unpickle             | 8.88 us                                                                  | 8.52 us: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.64 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 64.0 ms: 1.02x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.73 us: 1.07x slower                                                       |
| pickle               | 6.67 us                                                                  | 7.13 us: 1.07x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.4 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 21.0 ms: 1.39x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.38 ms: 1.36x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.9 ms: 1.33x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.4 ms: 1.20x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.32x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.08 ms: 2.00x faster                                                       |
| go                      | 143 ms                                                                   | 82.9 ms: 1.73x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.35 ms: 1.68x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.8 ms: 1.66x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 57.8 ns: 1.64x faster                                                       |
| mypy2                   | 337 ms                                                                   | 216 ms: 1.56x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 26.3 ns: 1.50x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 177 us: 1.49x faster                                                        |
| scimark_sor             | 104 ms                                                                   | 69.5 ms: 1.49x faster                                                       |
| raytrace                | 267 ms                                                                   | 182 ms: 1.47x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 833 us: 1.46x faster                                                        |
| pyflate                 | 388 ms                                                                   | 267 ms: 1.46x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.01 ms: 1.45x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 58.9 ms: 1.43x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.87 ms: 1.41x faster                                                       |
| django_template         | 29.2 ms                                                                  | 21.0 ms: 1.39x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 42.2 ms: 1.38x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 131 us: 1.37x faster                                                        |
| mako                    | 8.69 ms                                                                  | 6.38 ms: 1.36x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 34.8 ms: 1.36x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 45.7 ms: 1.34x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 363 ms: 1.34x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.9 ms: 1.33x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 21.4 us: 1.33x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 42.3 ms: 1.33x faster                                                       |
| thrift                  | 632 us                                                                   | 478 us: 1.32x faster                                                        |
| async_tree_none         | 414 ms                                                                   | 314 ms: 1.32x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 934 ms: 1.31x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 783 ms: 1.31x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 458 ms: 1.30x faster                                                        |
| xml_etree_process       | 43.0 ms                                                                  | 33.6 ms: 1.28x faster                                                       |
| regex_compile           | 103 ms                                                                   | 81.1 ms: 1.28x faster                                                       |
| pycparser               | 873 ms                                                                   | 691 ms: 1.26x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.62 ms: 1.25x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.0 ms: 1.25x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 59.7 ms: 1.24x faster                                                       |
| async_generators        | 214 ms                                                                   | 176 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 496 ms: 1.22x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 59.0 ms: 1.21x faster                                                       |
| deepcopy                | 256 us                                                                   | 212 us: 1.21x faster                                                        |
| tornado_http            | 106 ms                                                                   | 88.1 ms: 1.21x faster                                                       |
| dask                    | 310 ms                                                                   | 257 ms: 1.21x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.82 us: 1.20x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.4 ms: 1.20x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.24 ms: 1.19x faster                                                       |
| 2to3                    | 229 ms                                                                   | 194 ms: 1.18x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| float                   | 59.5 ms                                                                  | 51.0 ms: 1.17x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 174 ms: 1.16x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.78 ms: 1.15x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 41.1 ms: 1.14x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 57.1 ms: 1.14x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 275 ms: 1.14x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 842 us: 1.13x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 13.0 ms: 1.12x faster                                                       |
| fannkuch                | 252 ms                                                                   | 225 ms: 1.12x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 685 us: 1.12x faster                                                        |
| xml_etree_generate      | 53.8 ms                                                                  | 48.4 ms: 1.11x faster                                                       |
| regex_dna               | 131 ms                                                                   | 118 ms: 1.11x faster                                                        |
| json_loads              | 14.2 us                                                                  | 12.9 us: 1.10x faster                                                       |
| sympy_str               | 189 ms                                                                   | 173 ms: 1.09x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.9 ms: 1.09x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.5 ms: 1.08x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 69.2 ms: 1.07x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 95.2 ms: 1.07x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 175 ms: 1.07x faster                                                        |
| comprehensions          | 16.0 us                                                                  | 15.1 us: 1.06x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 91.0 ms: 1.05x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.52 us: 1.04x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.54 sec: 1.04x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.7 ms: 1.03x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.64 us: 1.03x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.80 us: 1.03x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.39 us: 1.02x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 76.4 ms: 1.02x slower                                                       |
| pidigits                | 145 ms                                                                   | 148 ms: 1.02x slower                                                        |
| logging_simple          | 6.12 us                                                                  | 6.24 us: 1.02x slower                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 64.0 ms: 1.02x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.73 us: 1.07x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.3 ms: 1.07x slower                                                       |
| pickle                  | 6.67 us                                                                  | 7.13 us: 1.07x slower                                                       |
| generators              | 31.4 ms                                                                  | 34.4 ms: 1.09x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.48 ms: 1.12x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 747 ms: 1.13x slower                                                        |
| pickle_dict             | 16.7 us                                                                  | 19.4 us: 1.16x slower                                                       |
| coverage                | 37.5 ms                                                                  | 53.2 ms: 1.42x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.19x faster                                                                |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
