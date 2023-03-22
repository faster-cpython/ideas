
# Results vs. 3.10.4

- fork: python
- ref: 72f00f420afaba3bc873
- machine: windows-amd64
- commit hash: 72f00f4
- commit date: 2022-05-30
- overall geometric mean: 1.09x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 205 ms: 1.12x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 5.35 ms: 1.08x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 39.6 ms: 1.19x faster                                                      |
| tornado_http   | 106 ms                                                                   | 91.0 ms: 1.17x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 53.5 ms: 1.11x faster                                                      |
| nbody          | 71.5 ms                                                                  | 68.5 ms: 1.04x faster                                                      |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 92.2 ms: 1.12x faster                                                      |
| regex_effbot   | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                      |
| regex_dna      | 131 ms                                                                   | 123 ms: 1.07x faster                                                       |
| regex_v8       | 15.1 ms                                                                  | 14.7 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 202 us: 1.31x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 155 us: 1.16x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 37.5 ms: 1.15x faster                                                      |
| json_dumps           | 9.00 ms                                                                  | 7.87 ms: 1.14x faster                                                      |
| unpickle             | 8.88 us                                                                  | 7.81 us: 1.14x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.44 us: 1.03x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 93.2 ms: 1.03x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 52.9 ms: 1.02x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.6 ms: 1.01x faster                                                      |
| json_loads           | 14.2 us                                                                  | 14.3 us: 1.01x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.60 us: 1.01x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 17.0 us: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.3 ms: 1.05x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 7.10 ms: 1.22x faster                                                      |
| django_template | 29.2 ms                                                                  | 23.9 ms: 1.22x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 17.2 ms: 1.08x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 38.4 ms: 1.01x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.13x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.68 ms: 1.55x faster                                                      |
| go                      | 143 ms                                                                   | 98.5 ms: 1.45x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 744 ms: 1.37x faster                                                       |
| richards                | 41.0 ms                                                                  | 30.5 ms: 1.34x faster                                                      |
| async_tree_none         | 414 ms                                                                   | 310 ms: 1.33x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 78.3 ms: 1.32x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 71.8 ns: 1.32x faster                                                      |
| async_tree_memoization  | 485 ms                                                                   | 369 ms: 1.32x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 63.8 ms: 1.31x faster                                                      |
| pickle_pure_python      | 264 us                                                                   | 202 us: 1.31x faster                                                       |
| raytrace                | 267 ms                                                                   | 205 ms: 1.30x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 43.6 ms: 1.29x faster                                                      |
| pyflate                 | 388 ms                                                                   | 302 ms: 1.29x faster                                                       |
| thrift                  | 632 us                                                                   | 500 us: 1.26x faster                                                       |
| pycparser               | 873 ms                                                                   | 701 ms: 1.25x faster                                                       |
| mako                    | 8.69 ms                                                                  | 7.10 ms: 1.22x faster                                                      |
| django_template         | 29.2 ms                                                                  | 23.9 ms: 1.22x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 497 ms: 1.22x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 48.2 ms: 1.21x faster                                                      |
| mypy2                   | 337 ms                                                                   | 279 ms: 1.21x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 51.1 ms: 1.20x faster                                                      |
| hexiom                  | 5.45 ms                                                                  | 4.56 ms: 1.19x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 39.6 ms: 1.19x faster                                                      |
| async_generators        | 214 ms                                                                   | 182 ms: 1.18x faster                                                       |
| tornado_http            | 106 ms                                                                   | 91.0 ms: 1.17x faster                                                      |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 82.6 ms: 1.17x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                     |
| unpickle_pure_python    | 179 us                                                                   | 155 us: 1.16x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 662 us: 1.15x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 37.5 ms: 1.15x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 7.87 ms: 1.14x faster                                                      |
| pprint_pformat          | 1.23 sec                                                                 | 1.08 sec: 1.14x faster                                                     |
| unpickle                | 8.88 us                                                                  | 7.81 us: 1.14x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 523 ms: 1.14x faster                                                       |
| dask                    | 310 ms                                                                   | 274 ms: 1.13x faster                                                       |
| regex_compile           | 103 ms                                                                   | 92.2 ms: 1.12x faster                                                      |
| deepcopy_memo           | 28.4 us                                                                  | 25.4 us: 1.12x faster                                                      |
| aiohttp                 | 968 us                                                                   | 866 us: 1.12x faster                                                       |
| 2to3                    | 229 ms                                                                   | 205 ms: 1.12x faster                                                       |
| float                   | 59.5 ms                                                                  | 53.5 ms: 1.11x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 865 us: 1.10x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 35.2 ms: 1.10x faster                                                      |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.3 ms: 1.09x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.35 ms: 1.09x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.70 us: 1.09x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 5.65 us: 1.08x faster                                                      |
| chameleon               | 5.77 ms                                                                  | 5.35 ms: 1.08x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 17.2 ms: 1.08x faster                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                      |
| sympy_integrate         | 14.7 ms                                                                  | 13.7 ms: 1.07x faster                                                      |
| logging_format          | 6.53 us                                                                  | 6.10 us: 1.07x faster                                                      |
| regex_dna               | 131 ms                                                                   | 123 ms: 1.07x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 1.14 ms: 1.06x faster                                                      |
| pylint                  | 337 ms                                                                   | 318 ms: 1.06x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 191 ms: 1.05x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.3 ms: 1.05x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 44.9 ms: 1.05x faster                                                      |
| coroutines              | 15.6 ms                                                                  | 14.9 ms: 1.05x faster                                                      |
| nbody                   | 71.5 ms                                                                  | 68.5 ms: 1.04x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 72.2 ms: 1.04x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 98.2 ms: 1.04x faster                                                      |
| spectral_norm           | 74.3 ms                                                                  | 71.3 ms: 1.04x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 301 ms: 1.04x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.44 us: 1.03x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 2.12 us: 1.03x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 14.7 ms: 1.03x faster                                                      |
| fannkuch                | 252 ms                                                                   | 245 ms: 1.03x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 93.2 ms: 1.03x faster                                                      |
| scimark_fft             | 187 ms                                                                   | 182 ms: 1.02x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.65 us: 1.02x faster                                                      |
| sympy_str               | 189 ms                                                                   | 185 ms: 1.02x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 52.9 ms: 1.02x faster                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.6 ms: 1.01x faster                                                      |
| genshi_xml              | 38.8 ms                                                                  | 38.4 ms: 1.01x faster                                                      |
| deepcopy                | 256 us                                                                   | 254 us: 1.01x faster                                                       |
| json_loads              | 14.2 us                                                                  | 14.3 us: 1.01x slower                                                      |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.60 us: 1.01x slower                                                      |
| meteor_contest          | 74.3 ms                                                                  | 75.7 ms: 1.02x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 17.0 us: 1.02x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 61.2 ms: 1.03x slower                                                      |
| nqueens                 | 64.8 ms                                                                  | 67.6 ms: 1.04x slower                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 41.1 ns: 1.05x slower                                                      |
| asyncio_tcp             | 664 ms                                                                   | 699 ms: 1.05x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.42 ms: 1.07x slower                                                      |
| telco                   | 3.77 ms                                                                  | 4.03 ms: 1.07x slower                                                      |
| mdp                     | 1.60 sec                                                                 | 1.72 sec: 1.07x slower                                                     |
| comprehensions          | 16.0 us                                                                  | 17.4 us: 1.09x slower                                                      |
| generators              | 31.4 ms                                                                  | 34.3 ms: 1.09x slower                                                      |
| coverage                | 37.5 ms                                                                  | 98.8 ms: 2.64x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.09x faster                                                               |

Benchmark hidden because not significant (2): json, scimark_sparse_mat_mult
Ignored benchmarks (1) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging
