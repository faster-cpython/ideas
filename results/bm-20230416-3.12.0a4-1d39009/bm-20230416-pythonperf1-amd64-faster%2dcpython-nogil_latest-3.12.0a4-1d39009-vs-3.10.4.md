
# Results vs. 3.10.4

- fork: faster-cpython
- ref: nogil_latest
- machine: windows-amd64
- commit hash: 1d39009
- commit date: 2023-04-16
- overall geometric mean: 1.06x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 224 ms: 1.02x faster                                                         |
| chameleon      | 5.77 ms                                                                  | 5.66 ms: 1.02x faster                                                        |
| docutils       | 1.83 sec                                                                 | 1.89 sec: 1.03x slower                                                       |
| html5lib       | 47.3 ms                                                                  | 39.3 ms: 1.20x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 49.6 ms: 1.20x faster                                                        |
| pidigits       | 145 ms                                                                   | 141 ms: 1.03x faster                                                         |
| nbody          | 71.5 ms                                                                  | 89.9 ms: 1.26x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                                   | 110 ms: 1.19x faster                                                         |
| regex_v8       | 15.1 ms                                                                  | 13.2 ms: 1.14x faster                                                        |
| regex_compile  | 103 ms                                                                   | 96.4 ms: 1.07x faster                                                        |
| regex_effbot   | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 6.50 ms: 1.38x faster                                                        |
| pickle_pure_python   | 264 us                                                                   | 218 us: 1.21x faster                                                         |
| xml_etree_parse      | 95.6 ms                                                                  | 82.9 ms: 1.15x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 159 us: 1.13x faster                                                         |
| xml_etree_process    | 43.0 ms                                                                  | 41.7 ms: 1.03x faster                                                        |
| json_loads           | 14.2 us                                                                  | 14.6 us: 1.03x slower                                                        |
| unpickle             | 8.88 us                                                                  | 9.19 us: 1.03x slower                                                        |
| unpickle_list        | 2.71 us                                                                  | 2.86 us: 1.05x slower                                                        |
| xml_etree_generate   | 53.8 ms                                                                  | 57.5 ms: 1.07x slower                                                        |
| pickle               | 6.67 us                                                                  | 7.14 us: 1.07x slower                                                        |
| pickle_list          | 2.57 us                                                                  | 2.81 us: 1.09x slower                                                        |
| xml_etree_iterparse  | 62.5 ms                                                                  | 74.7 ms: 1.19x slower                                                        |
| pickle_dict          | 16.7 us                                                                  | 21.8 us: 1.30x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                        |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 25.5 ms: 1.14x faster                                                        |
| genshi_xml      | 38.8 ms                                                                  | 35.3 ms: 1.10x faster                                                        |
| genshi_text     | 18.5 ms                                                                  | 17.7 ms: 1.05x faster                                                        |
| mako            | 8.69 ms                                                                  | 8.95 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230416-pythonperf1-amd64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 1.02 sec                                                                 | 405 ms: 2.53x faster                                                         |
| async_tree_none         | 414 ms                                                                   | 189 ms: 2.19x faster                                                         |
| async_tree_memoization  | 485 ms                                                                   | 240 ms: 2.02x faster                                                         |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 371 ms: 1.63x faster                                                         |
| deltablue               | 4.15 ms                                                                  | 2.71 ms: 1.53x faster                                                        |
| go                      | 143 ms                                                                   | 103 ms: 1.39x faster                                                         |
| json_dumps              | 9.00 ms                                                                  | 6.50 ms: 1.38x faster                                                        |
| sqlite_synth            | 1.85 us                                                                  | 1.35 us: 1.36x faster                                                        |
| asyncio_tcp             | 664 ms                                                                   | 489 ms: 1.36x faster                                                         |
| pyflate                 | 388 ms                                                                   | 302 ms: 1.29x faster                                                         |
| richards                | 41.0 ms                                                                  | 32.3 ms: 1.27x faster                                                        |
| logging_silent          | 94.6 ns                                                                  | 75.0 ns: 1.26x faster                                                        |
| pycparser               | 873 ms                                                                   | 713 ms: 1.23x faster                                                         |
| pickle_pure_python      | 264 us                                                                   | 218 us: 1.21x faster                                                         |
| html5lib                | 47.3 ms                                                                  | 39.3 ms: 1.20x faster                                                        |
| float                   | 59.5 ms                                                                  | 49.6 ms: 1.20x faster                                                        |
| regex_dna               | 131 ms                                                                   | 110 ms: 1.19x faster                                                         |
| crypto_pyaes            | 61.4 ms                                                                  | 52.7 ms: 1.17x faster                                                        |
| thrift                  | 632 us                                                                   | 542 us: 1.17x faster                                                         |
| scimark_sor             | 104 ms                                                                   | 89.1 ms: 1.16x faster                                                        |
| mypy2                   | 337 ms                                                                   | 291 ms: 1.16x faster                                                         |
| xml_etree_parse         | 95.6 ms                                                                  | 82.9 ms: 1.15x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 73.1 ms: 1.15x faster                                                        |
| django_template         | 29.2 ms                                                                  | 25.5 ms: 1.14x faster                                                        |
| regex_v8                | 15.1 ms                                                                  | 13.2 ms: 1.14x faster                                                        |
| unpickle_pure_python    | 179 us                                                                   | 159 us: 1.13x faster                                                         |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.33 ms: 1.11x faster                                                        |
| raytrace                | 267 ms                                                                   | 241 ms: 1.11x faster                                                         |
| genshi_xml              | 38.8 ms                                                                  | 35.3 ms: 1.10x faster                                                        |
| hexiom                  | 5.45 ms                                                                  | 4.97 ms: 1.10x faster                                                        |
| scimark_monte_carlo     | 56.0 ms                                                                  | 51.2 ms: 1.09x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 1.12 ms: 1.09x faster                                                        |
| chaos                   | 58.4 ms                                                                  | 53.7 ms: 1.09x faster                                                        |
| json                    | 3.18 ms                                                                  | 2.94 ms: 1.08x faster                                                        |
| dulwich_log             | 47.0 ms                                                                  | 43.6 ms: 1.08x faster                                                        |
| regex_compile           | 103 ms                                                                   | 96.4 ms: 1.07x faster                                                        |
| regex_effbot            | 1.64 ms                                                                  | 1.53 ms: 1.07x faster                                                        |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 36.8 ms: 1.05x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 17.7 ms: 1.05x faster                                                        |
| async_generators        | 214 ms                                                                   | 205 ms: 1.05x faster                                                         |
| xml_etree_process       | 43.0 ms                                                                  | 41.7 ms: 1.03x faster                                                        |
| pidigits                | 145 ms                                                                   | 141 ms: 1.03x faster                                                         |
| 2to3                    | 229 ms                                                                   | 224 ms: 1.02x faster                                                         |
| pathlib                 | 75.2 ms                                                                  | 73.6 ms: 1.02x faster                                                        |
| create_gc_cycles        | 764 us                                                                   | 748 us: 1.02x faster                                                         |
| chameleon               | 5.77 ms                                                                  | 5.66 ms: 1.02x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 1.21 sec: 1.02x faster                                                       |
| pprint_safe_repr        | 593 ms                                                                   | 586 ms: 1.01x faster                                                         |
| sqlglot_normalize       | 201 ms                                                                   | 199 ms: 1.01x faster                                                         |
| sympy_integrate         | 14.7 ms                                                                  | 14.8 ms: 1.01x slower                                                        |
| nqueens                 | 64.8 ms                                                                  | 65.6 ms: 1.01x slower                                                        |
| mdp                     | 1.60 sec                                                                 | 1.63 sec: 1.02x slower                                                       |
| sympy_expand            | 313 ms                                                                   | 320 ms: 1.02x slower                                                         |
| docutils                | 1.83 sec                                                                 | 1.89 sec: 1.03x slower                                                       |
| json_loads              | 14.2 us                                                                  | 14.6 us: 1.03x slower                                                        |
| mako                    | 8.69 ms                                                                  | 8.95 ms: 1.03x slower                                                        |
| unpickle                | 8.88 us                                                                  | 9.19 us: 1.03x slower                                                        |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                        |
| deepcopy_memo           | 28.4 us                                                                  | 29.5 us: 1.04x slower                                                        |
| sympy_str               | 189 ms                                                                   | 198 ms: 1.05x slower                                                         |
| unpickle_list           | 2.71 us                                                                  | 2.86 us: 1.05x slower                                                        |
| deepcopy                | 256 us                                                                   | 272 us: 1.06x slower                                                         |
| spectral_norm           | 74.3 ms                                                                  | 78.8 ms: 1.06x slower                                                        |
| sympy_sum               | 102 ms                                                                   | 109 ms: 1.07x slower                                                         |
| xml_etree_generate      | 53.8 ms                                                                  | 57.5 ms: 1.07x slower                                                        |
| pickle                  | 6.67 us                                                                  | 7.14 us: 1.07x slower                                                        |
| coroutines              | 15.6 ms                                                                  | 16.8 ms: 1.07x slower                                                        |
| bench_mp_pool           | 59.2 ms                                                                  | 63.9 ms: 1.08x slower                                                        |
| bench_thread_pool       | 953 us                                                                   | 1.03 ms: 1.08x slower                                                        |
| pickle_list             | 2.57 us                                                                  | 2.81 us: 1.09x slower                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 2.40 us: 1.10x slower                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.98 ms: 1.12x slower                                                        |
| logging_simple          | 6.12 us                                                                  | 6.92 us: 1.13x slower                                                        |
| fannkuch                | 252 ms                                                                   | 285 ms: 1.13x slower                                                         |
| logging_format          | 6.53 us                                                                  | 7.40 us: 1.13x slower                                                        |
| meteor_contest          | 74.3 ms                                                                  | 86.5 ms: 1.16x slower                                                        |
| telco                   | 3.77 ms                                                                  | 4.41 ms: 1.17x slower                                                        |
| gc_traversal            | 1.33 ms                                                                  | 1.56 ms: 1.17x slower                                                        |
| scimark_fft             | 187 ms                                                                   | 220 ms: 1.18x slower                                                         |
| comprehensions          | 16.0 us                                                                  | 19.1 us: 1.19x slower                                                        |
| xml_etree_iterparse     | 62.5 ms                                                                  | 74.7 ms: 1.19x slower                                                        |
| generators              | 31.4 ms                                                                  | 37.5 ms: 1.19x slower                                                        |
| nbody                   | 71.5 ms                                                                  | 89.9 ms: 1.26x slower                                                        |
| pickle_dict             | 16.7 us                                                                  | 21.8 us: 1.30x slower                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 55.2 ns: 1.40x slower                                                        |
| coverage                | 37.5 ms                                                                  | 59.9 ms: 1.60x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.06x faster                                                                 |
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, dask, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
