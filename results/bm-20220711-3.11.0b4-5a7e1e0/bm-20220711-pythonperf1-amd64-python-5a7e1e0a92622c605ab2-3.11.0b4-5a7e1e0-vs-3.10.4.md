
# Results vs. 3.10.4

- fork: python
- ref: 5a7e1e0a92622c605ab2
- machine: windows-amd64
- commit hash: 5a7e1e0
- commit date: 2022-07-11
- overall geometric mean: 1.10x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 206 ms: 1.11x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 5.14 ms: 1.12x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 38.9 ms: 1.22x faster                                                      |
| tornado_http   | 106 ms                                                                   | 91.9 ms: 1.16x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 53.9 ms: 1.10x faster                                                      |
| nbody          | 71.5 ms                                                                  | 68.7 ms: 1.04x faster                                                      |
| pidigits       | 145 ms                                                                   | 146 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                                   | 114 ms: 1.14x faster                                                       |
| regex_compile  | 103 ms                                                                   | 90.8 ms: 1.14x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                      |
| regex_effbot   | 1.64 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.09x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 204 us: 1.30x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 152 us: 1.18x faster                                                       |
| json_dumps           | 9.00 ms                                                                  | 7.78 ms: 1.16x faster                                                      |
| xml_etree_process    | 43.0 ms                                                                  | 37.8 ms: 1.14x faster                                                      |
| unpickle             | 8.88 us                                                                  | 8.32 us: 1.07x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.48 us: 1.03x faster                                                      |
| json_loads           | 14.2 us                                                                  | 14.1 us: 1.01x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 53.4 ms: 1.01x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.80 us: 1.03x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.65 us: 1.03x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                               |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 7.23 ms: 1.20x faster                                                      |
| django_template | 29.2 ms                                                                  | 25.0 ms: 1.17x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 17.6 ms: 1.06x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.11x faster                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.66 ms: 1.56x faster                                                      |
| go                      | 143 ms                                                                   | 99.5 ms: 1.44x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 753 ms: 1.36x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 62.7 ms: 1.34x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 78.5 ms: 1.32x faster                                                      |
| raytrace                | 267 ms                                                                   | 204 ms: 1.31x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 72.4 ns: 1.31x faster                                                      |
| async_tree_none         | 414 ms                                                                   | 317 ms: 1.31x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 936 us: 1.30x faster                                                       |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.13 ms: 1.30x faster                                                      |
| pickle_pure_python      | 264 us                                                                   | 204 us: 1.30x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 375 ms: 1.29x faster                                                       |
| richards                | 41.0 ms                                                                  | 31.7 ms: 1.29x faster                                                      |
| pyflate                 | 388 ms                                                                   | 306 ms: 1.27x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 44.3 ms: 1.27x faster                                                      |
| pycparser               | 873 ms                                                                   | 706 ms: 1.24x faster                                                       |
| thrift                  | 632 us                                                                   | 518 us: 1.22x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 38.9 ms: 1.22x faster                                                      |
| mypy2                   | 337 ms                                                                   | 278 ms: 1.21x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 50.6 ms: 1.21x faster                                                      |
| async_generators        | 214 ms                                                                   | 178 ms: 1.21x faster                                                       |
| mako                    | 8.69 ms                                                                  | 7.23 ms: 1.20x faster                                                      |
| chaos                   | 58.4 ms                                                                  | 48.7 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 508 ms: 1.19x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.61 ms: 1.18x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 152 us: 1.18x faster                                                       |
| django_template         | 29.2 ms                                                                  | 25.0 ms: 1.17x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.58 sec: 1.16x faster                                                     |
| tornado_http            | 106 ms                                                                   | 91.9 ms: 1.16x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 7.78 ms: 1.16x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 515 ms: 1.15x faster                                                       |
| dask                    | 310 ms                                                                   | 270 ms: 1.15x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 664 us: 1.15x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 1.07 sec: 1.15x faster                                                     |
| regex_dna               | 131 ms                                                                   | 114 ms: 1.14x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 37.8 ms: 1.14x faster                                                      |
| regex_compile           | 103 ms                                                                   | 90.8 ms: 1.14x faster                                                      |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 84.7 ms: 1.14x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.4 ms: 1.13x faster                                                      |
| aiohttp                 | 968 us                                                                   | 860 us: 1.13x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 5.14 ms: 1.12x faster                                                      |
| deepcopy_memo           | 28.4 us                                                                  | 25.3 us: 1.12x faster                                                      |
| 2to3                    | 229 ms                                                                   | 206 ms: 1.11x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 34.8 ms: 1.11x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 858 us: 1.11x faster                                                       |
| float                   | 59.5 ms                                                                  | 53.9 ms: 1.10x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.70 us: 1.09x faster                                                      |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.4 ms: 1.08x faster                                                      |
| sympy_expand            | 313 ms                                                                   | 291 ms: 1.07x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.7 ms: 1.07x faster                                                      |
| unpickle                | 8.88 us                                                                  | 8.32 us: 1.07x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 95.8 ms: 1.07x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 44.2 ms: 1.06x faster                                                      |
| pylint                  | 337 ms                                                                   | 318 ms: 1.06x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.8 ms: 1.06x faster                                                      |
| genshi_text             | 18.5 ms                                                                  | 17.6 ms: 1.06x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 192 ms: 1.05x faster                                                       |
| deepcopy                | 256 us                                                                   | 246 us: 1.04x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 68.7 ms: 1.04x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 72.4 ms: 1.04x faster                                                      |
| sympy_str               | 189 ms                                                                   | 182 ms: 1.04x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.48 us: 1.03x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 2.14 us: 1.02x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 15.7 us: 1.01x faster                                                      |
| json_loads              | 14.2 us                                                                  | 14.1 us: 1.01x faster                                                      |
| xml_etree_generate      | 53.8 ms                                                                  | 53.4 ms: 1.01x faster                                                      |
| spectral_norm           | 74.3 ms                                                                  | 73.7 ms: 1.01x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 74.8 ms: 1.01x slower                                                      |
| pidigits                | 145 ms                                                                   | 146 ms: 1.01x slower                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.80 us: 1.03x slower                                                      |
| pickle_list             | 2.57 us                                                                  | 2.65 us: 1.03x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 61.4 ms: 1.04x slower                                                      |
| mdp                     | 1.60 sec                                                                 | 1.67 sec: 1.04x slower                                                     |
| nqueens                 | 64.8 ms                                                                  | 67.6 ms: 1.04x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.41 ms: 1.06x slower                                                      |
| telco                   | 3.77 ms                                                                  | 4.02 ms: 1.07x slower                                                      |
| generators              | 31.4 ms                                                                  | 33.9 ms: 1.08x slower                                                      |
| logging_simple          | 6.12 us                                                                  | 6.68 us: 1.09x slower                                                      |
| logging_format          | 6.53 us                                                                  | 7.19 us: 1.10x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 45.4 ns: 1.15x slower                                                      |
| coverage                | 37.5 ms                                                                  | 54.1 ms: 1.44x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.10x faster                                                               |

Benchmark hidden because not significant (9): genshi_xml, xml_etree_parse, scimark_fft, fannkuch, flaskblogging, xml_etree_iterparse, scimark_sparse_mat_mult, asyncio_tcp, json
