
# Results vs. 3.10.4

- fork: python
- ref: b6bd7ffcbc1ffaa68e34
- machine: windows-amd64
- commit hash: b6bd7ff
- commit date: 2022-12-06
- overall geometric mean: 1.24x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 186 ms: 1.24x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 4.22 ms: 1.37x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.50 sec: 1.22x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 34.8 ms: 1.36x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.29x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 47.7 ms: 1.25x faster                                                      |
| nbody          | 71.5 ms                                                                  | 57.5 ms: 1.24x faster                                                      |
| pidigits       | 145 ms                                                                   | 147 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.15x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 77.2 ms: 1.34x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.7 ms: 1.11x faster                                                      |
| regex_dna      | 131 ms                                                                   | 119 ms: 1.10x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.69 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.31 ms: 1.70x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 166 us: 1.59x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 116 us: 1.54x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 32.7 ms: 1.32x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 47.9 ms: 1.12x faster                                                      |
| unpickle             | 8.88 us                                                                  | 8.03 us: 1.11x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 89.1 ms: 1.07x faster                                                      |
| json_loads           | 14.2 us                                                                  | 13.3 us: 1.06x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.67 us: 1.01x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.87 us: 1.03x slower                                                      |
| pickle_list          | 2.57 us                                                                  | 2.73 us: 1.06x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.16x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.1 ms: 1.06x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.00 ms: 1.45x faster                                                      |
| django_template | 29.2 ms                                                                  | 20.3 ms: 1.44x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 13.7 ms: 1.36x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 31.5 ms: 1.23x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.37x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221206-pythonperf1-amd64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.97 ms: 2.10x faster                                                      |
| go                      | 143 ms                                                                   | 78.0 ms: 1.84x faster                                                      |
| richards                | 41.0 ms                                                                  | 23.4 ms: 1.76x faster                                                      |
| logging_silent          | 94.6 ns                                                                  | 55.4 ns: 1.71x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 5.31 ms: 1.70x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 61.1 ms: 1.69x faster                                                      |
| mypy2                   | 337 ms                                                                   | 206 ms: 1.64x faster                                                       |
| pickle_pure_python      | 264 us                                                                   | 166 us: 1.59x faster                                                       |
| raytrace                | 267 ms                                                                   | 169 ms: 1.58x faster                                                       |
| scimark_lu              | 83.9 ms                                                                  | 53.2 ms: 1.58x faster                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 25.3 ns: 1.56x faster                                                      |
| scimark_monte_carlo     | 56.0 ms                                                                  | 36.3 ms: 1.54x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 116 us: 1.54x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 804 us: 1.52x faster                                                       |
| pyflate                 | 388 ms                                                                   | 259 ms: 1.50x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.65 ms: 1.49x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 994 us: 1.48x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 19.3 us: 1.47x faster                                                      |
| mako                    | 8.69 ms                                                                  | 6.00 ms: 1.45x faster                                                      |
| django_template         | 29.2 ms                                                                  | 20.3 ms: 1.44x faster                                                      |
| crypto_pyaes            | 61.4 ms                                                                  | 43.2 ms: 1.42x faster                                                      |
| chaos                   | 58.4 ms                                                                  | 41.3 ms: 1.42x faster                                                      |
| thrift                  | 632 us                                                                   | 455 us: 1.39x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 888 ms: 1.38x faster                                                       |
| chameleon               | 5.77 ms                                                                  | 4.22 ms: 1.37x faster                                                      |
| html5lib                | 47.3 ms                                                                  | 34.8 ms: 1.36x faster                                                      |
| async_tree_io           | 1.02 sec                                                                 | 753 ms: 1.36x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 13.7 ms: 1.36x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 440 ms: 1.35x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 308 ms: 1.35x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 362 ms: 1.34x faster                                                       |
| regex_compile           | 103 ms                                                                   | 77.2 ms: 1.34x faster                                                      |
| xml_etree_process       | 43.0 ms                                                                  | 32.7 ms: 1.32x faster                                                      |
| async_generators        | 214 ms                                                                   | 163 ms: 1.31x faster                                                       |
| pycparser               | 873 ms                                                                   | 667 ms: 1.31x faster                                                       |
| deepcopy                | 256 us                                                                   | 197 us: 1.30x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 30.4 ms: 1.27x faster                                                      |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.11 ms: 1.27x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.74 us: 1.25x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 483 ms: 1.25x faster                                                       |
| float                   | 59.5 ms                                                                  | 47.7 ms: 1.25x faster                                                      |
| nbody                   | 71.5 ms                                                                  | 57.5 ms: 1.24x faster                                                      |
| 2to3                    | 229 ms                                                                   | 186 ms: 1.24x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 31.5 ms: 1.23x faster                                                      |
| dask                    | 310 ms                                                                   | 254 ms: 1.22x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 164 ms: 1.22x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 60.9 ms: 1.22x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.50 sec: 1.22x faster                                                     |
| fannkuch                | 252 ms                                                                   | 210 ms: 1.20x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.67 ms: 1.19x faster                                                      |
| nqueens                 | 64.8 ms                                                                  | 55.3 ms: 1.17x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 815 us: 1.17x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 660 us: 1.16x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 273 ms: 1.14x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.8 ms: 1.14x faster                                                      |
| scimark_fft             | 187 ms                                                                   | 164 ms: 1.14x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 47.9 ms: 1.12x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 42.1 ms: 1.12x faster                                                      |
| unpickle                | 8.88 us                                                                  | 8.03 us: 1.11x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.7 ms: 1.11x faster                                                      |
| regex_dna               | 131 ms                                                                   | 119 ms: 1.10x faster                                                       |
| meteor_contest          | 74.3 ms                                                                  | 67.8 ms: 1.10x faster                                                      |
| sympy_str               | 189 ms                                                                   | 173 ms: 1.09x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.4 ms: 1.09x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 14.7 us: 1.09x faster                                                      |
| xml_etree_parse         | 95.6 ms                                                                  | 89.1 ms: 1.07x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.72 us: 1.07x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 95.7 ms: 1.07x faster                                                      |
| json_loads              | 14.2 us                                                                  | 13.3 us: 1.06x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.1 ms: 1.06x faster                                                      |
| mdp                     | 1.60 sec                                                                 | 1.51 sec: 1.06x faster                                                     |
| logging_format          | 6.53 us                                                                  | 6.24 us: 1.05x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 72.3 ms: 1.04x faster                                                      |
| logging_simple          | 6.12 us                                                                  | 5.91 us: 1.04x faster                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.67 us: 1.01x faster                                                      |
| pidigits                | 145 ms                                                                   | 147 ms: 1.02x slower                                                       |
| telco                   | 3.77 ms                                                                  | 3.86 ms: 1.02x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.69 ms: 1.03x slower                                                      |
| pickle                  | 6.67 us                                                                  | 6.87 us: 1.03x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.3 ms: 1.03x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 61.1 ms: 1.03x slower                                                      |
| gc_traversal            | 1.33 ms                                                                  | 1.40 ms: 1.05x slower                                                      |
| generators              | 31.4 ms                                                                  | 33.1 ms: 1.05x slower                                                      |
| pickle_list             | 2.57 us                                                                  | 2.73 us: 1.06x slower                                                      |
| asyncio_tcp             | 664 ms                                                                   | 711 ms: 1.07x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 18.4 us: 1.10x slower                                                      |
| coverage                | 37.5 ms                                                                  | 50.1 ms: 1.34x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.24x faster                                                               |
Ignored benchmarks (6) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
