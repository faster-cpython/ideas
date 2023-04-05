
# Results vs. 3.10.4

- fork: python
- ref: d717be04dc7876696cb2
- machine: windows-amd64
- commit hash: d717be0
- commit date: 2023-01-22
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 202 ms: 1.14x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.37 ms: 1.32x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.7 ms: 1.32x faster                                                       |
| tornado_http   | 106 ms                                                                   | 88.8 ms: 1.20x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 47.2 ms: 1.26x faster                                                       |
| nbody          | 71.5 ms                                                                  | 59.7 ms: 1.20x faster                                                       |
| pidigits       | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.13x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 78.1 ms: 1.32x faster                                                       |
| regex_dna      | 131 ms                                                                   | 117 ms: 1.12x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 13.6 ms: 1.11x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.43 ms: 1.66x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 171 us: 1.54x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 121 us: 1.48x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 35.0 ms: 1.23x faster                                                       |
| json_loads           | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 49.7 ms: 1.08x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 94.7 ms: 1.01x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.76 us: 1.02x slower                                                       |
| unpickle             | 8.88 us                                                                  | 9.15 us: 1.03x slower                                                       |
| pickle               | 6.67 us                                                                  | 6.94 us: 1.04x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.72 us: 1.06x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 14.8 ms                                                                  | 16.5 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.05x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.4 ms: 1.43x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.21 ms: 1.40x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.4 ms: 1.38x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 33.0 ms: 1.18x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.34x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4+-d717be0 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.02 ms: 2.06x faster                                                       |
| go                      | 143 ms                                                                   | 83.7 ms: 1.71x faster                                                       |
| richards                | 41.0 ms                                                                  | 24.2 ms: 1.69x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 56.5 ns: 1.67x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.43 ms: 1.66x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 64.2 ms: 1.61x faster                                                       |
| mypy2                   | 337 ms                                                                   | 216 ms: 1.56x faster                                                        |
| raytrace                | 267 ms                                                                   | 173 ms: 1.55x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 171 us: 1.54x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 25.7 ns: 1.53x faster                                                       |
| pyflate                 | 388 ms                                                                   | 258 ms: 1.51x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 121 us: 1.48x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 3.73 ms: 1.46x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 57.6 ms: 1.46x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 40.1 ms: 1.46x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.4 ms: 1.43x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 863 us: 1.41x faster                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 20.2 us: 1.40x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.21 ms: 1.40x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 40.2 ms: 1.39x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.06 ms: 1.39x faster                                                       |
| thrift                  | 632 us                                                                   | 456 us: 1.39x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.4 ms: 1.38x faster                                                       |
| asyncio_tcp             | 664 ms                                                                   | 483 ms: 1.37x faster                                                        |
| crypto_pyaes            | 61.4 ms                                                                  | 45.2 ms: 1.36x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 308 ms: 1.35x faster                                                        |
| pycparser               | 873 ms                                                                   | 653 ms: 1.34x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 770 ms: 1.33x faster                                                        |
| html5lib                | 47.3 ms                                                                  | 35.7 ms: 1.32x faster                                                       |
| regex_compile           | 103 ms                                                                   | 78.1 ms: 1.32x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.37 ms: 1.32x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 945 ms: 1.30x faster                                                        |
| async_tree_memoization  | 485 ms                                                                   | 374 ms: 1.30x faster                                                        |
| deepcopy                | 256 us                                                                   | 201 us: 1.27x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 469 ms: 1.27x faster                                                        |
| float                   | 59.5 ms                                                                  | 47.2 ms: 1.26x faster                                                       |
| async_generators        | 214 ms                                                                   | 171 ms: 1.25x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.16 ms: 1.23x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 35.0 ms: 1.23x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 60.5 ms: 1.23x faster                                                       |
| deepcopy_reduce         | 2.18 us                                                                  | 1.80 us: 1.22x faster                                                       |
| dask                    | 310 ms                                                                   | 257 ms: 1.21x faster                                                        |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 502 ms: 1.20x faster                                                        |
| tornado_http            | 106 ms                                                                   | 88.8 ms: 1.20x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 59.7 ms: 1.20x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.5 ms: 1.19x faster                                                       |
| docutils                | 1.83 sec                                                                 | 1.55 sec: 1.18x faster                                                      |
| genshi_xml              | 38.8 ms                                                                  | 33.0 ms: 1.18x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 55.9 ms: 1.16x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.75 ms: 1.16x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 174 ms: 1.16x faster                                                        |
| sympy_expand            | 313 ms                                                                   | 271 ms: 1.16x faster                                                        |
| fannkuch                | 252 ms                                                                   | 218 ms: 1.15x faster                                                        |
| sympy_integrate         | 14.7 ms                                                                  | 12.8 ms: 1.15x faster                                                       |
| 2to3                    | 229 ms                                                                   | 202 ms: 1.14x faster                                                        |
| bench_thread_pool       | 953 us                                                                   | 846 us: 1.13x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 167 ms: 1.12x faster                                                        |
| sympy_str               | 189 ms                                                                   | 169 ms: 1.12x faster                                                        |
| regex_dna               | 131 ms                                                                   | 117 ms: 1.12x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.6 ms: 1.11x faster                                                       |
| json_loads              | 14.2 us                                                                  | 12.8 us: 1.11x faster                                                       |
| dulwich_log             | 47.0 ms                                                                  | 42.5 ms: 1.11x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 702 us: 1.09x faster                                                        |
| xml_etree_generate      | 53.8 ms                                                                  | 49.7 ms: 1.08x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.6 ms: 1.07x faster                                                       |
| sympy_sum               | 102 ms                                                                   | 95.6 ms: 1.07x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.0 us: 1.07x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.54 ms: 1.06x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.74 us: 1.06x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 70.3 ms: 1.06x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.61 ms: 1.04x faster                                                       |
| logging_format          | 6.53 us                                                                  | 6.38 us: 1.02x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.57 sec: 1.02x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 94.7 ms: 1.01x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 63.3 ms: 1.01x slower                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.76 us: 1.02x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.23 us: 1.02x slower                                                       |
| unpickle                | 8.88 us                                                                  | 9.15 us: 1.03x slower                                                       |
| pidigits                | 145 ms                                                                   | 151 ms: 1.04x slower                                                        |
| pickle                  | 6.67 us                                                                  | 6.94 us: 1.04x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.72 us: 1.06x slower                                                       |
| bench_mp_pool           | 59.2 ms                                                                  | 63.3 ms: 1.07x slower                                                       |
| generators              | 31.4 ms                                                                  | 33.9 ms: 1.08x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 16.5 ms: 1.11x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.51 ms: 1.14x slower                                                       |
| coverage                | 37.5 ms                                                                  | 52.6 ms: 1.40x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |

Benchmark hidden because not significant (2): pathlib, python_startup
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
