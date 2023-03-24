
# Results vs. 3.10.4

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: windows-amd64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.18x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 193 ms: 1.19x faster                                                       |
| chameleon      | 5.77 ms                                                                  | 4.59 ms: 1.26x faster                                                      |
| docutils       | 1.83 sec                                                                 | 1.52 sec: 1.21x faster                                                     |
| html5lib       | 47.3 ms                                                                  | 36.4 ms: 1.30x faster                                                      |
| tornado_http   | 106 ms                                                                   | 89.5 ms: 1.19x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 48.7 ms: 1.22x faster                                                      |
| nbody          | 71.5 ms                                                                  | 62.3 ms: 1.15x faster                                                      |
| pidigits       | 145 ms                                                                   | 146 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 82.3 ms: 1.26x faster                                                      |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.10x faster                                                      |
| regex_dna      | 131 ms                                                                   | 120 ms: 1.09x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.12 ms: 1.76x faster                                                      |
| pickle_pure_python   | 264 us                                                                   | 180 us: 1.47x faster                                                       |
| unpickle_pure_python | 179 us                                                                   | 130 us: 1.37x faster                                                       |
| xml_etree_process    | 43.0 ms                                                                  | 33.9 ms: 1.27x faster                                                      |
| xml_etree_generate   | 53.8 ms                                                                  | 49.0 ms: 1.10x faster                                                      |
| xml_etree_parse      | 95.6 ms                                                                  | 87.6 ms: 1.09x faster                                                      |
| unpickle             | 8.88 us                                                                  | 8.25 us: 1.08x faster                                                      |
| json_loads           | 14.2 us                                                                  | 13.3 us: 1.07x faster                                                      |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                                      |
| pickle               | 6.67 us                                                                  | 6.57 us: 1.01x faster                                                      |
| pickle_list          | 2.57 us                                                                  | 2.62 us: 1.02x slower                                                      |
| unpickle_list        | 2.71 us                                                                  | 2.79 us: 1.03x slower                                                      |
| pickle_dict          | 16.7 us                                                                  | 18.3 us: 1.10x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.14x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 8.69 ms                                                                  | 6.25 ms: 1.39x faster                                                      |
| django_template | 29.2 ms                                                                  | 21.6 ms: 1.35x faster                                                      |
| genshi_text     | 18.5 ms                                                                  | 14.4 ms: 1.29x faster                                                      |
| genshi_xml      | 38.8 ms                                                                  | 32.2 ms: 1.20x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.31x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-pythonperf1-amd64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.24 ms: 1.85x faster                                                      |
| json_dumps              | 9.00 ms                                                                  | 5.12 ms: 1.76x faster                                                      |
| go                      | 143 ms                                                                   | 84.0 ms: 1.71x faster                                                      |
| mypy2                   | 337 ms                                                                   | 212 ms: 1.60x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 59.9 ns: 1.58x faster                                                      |
| richards                | 41.0 ms                                                                  | 26.7 ms: 1.53x faster                                                      |
| scimark_sor             | 104 ms                                                                   | 69.2 ms: 1.50x faster                                                      |
| scimark_lu              | 83.9 ms                                                                  | 56.9 ms: 1.47x faster                                                      |
| pickle_pure_python      | 264 us                                                                   | 180 us: 1.47x faster                                                       |
| raytrace                | 267 ms                                                                   | 184 ms: 1.45x faster                                                       |
| pyflate                 | 388 ms                                                                   | 272 ms: 1.43x faster                                                       |
| sqlglot_parse           | 1.22 ms                                                                  | 865 us: 1.41x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 39.8 ms: 1.41x faster                                                      |
| mako                    | 8.69 ms                                                                  | 6.25 ms: 1.39x faster                                                      |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.06 ms: 1.38x faster                                                      |
| unpickle_pure_python    | 179 us                                                                   | 130 us: 1.37x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 4.00 ms: 1.36x faster                                                      |
| chaos                   | 58.4 ms                                                                  | 43.1 ms: 1.35x faster                                                      |
| crypto_pyaes            | 61.4 ms                                                                  | 45.4 ms: 1.35x faster                                                      |
| django_template         | 29.2 ms                                                                  | 21.6 ms: 1.35x faster                                                      |
| pycparser               | 873 ms                                                                   | 650 ms: 1.34x faster                                                       |
| pprint_pformat          | 1.23 sec                                                                 | 934 ms: 1.31x faster                                                       |
| async_tree_io           | 1.02 sec                                                                 | 783 ms: 1.31x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 36.4 ms: 1.30x faster                                                      |
| pprint_safe_repr        | 593 ms                                                                   | 458 ms: 1.30x faster                                                       |
| genshi_text             | 18.5 ms                                                                  | 14.4 ms: 1.29x faster                                                      |
| deepcopy_memo           | 28.4 us                                                                  | 22.2 us: 1.28x faster                                                      |
| unpack_sequence         | 39.4 ns                                                                  | 30.8 ns: 1.28x faster                                                      |
| async_tree_none         | 414 ms                                                                   | 325 ms: 1.27x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 33.9 ms: 1.27x faster                                                      |
| chameleon               | 5.77 ms                                                                  | 4.59 ms: 1.26x faster                                                      |
| async_tree_memoization  | 485 ms                                                                   | 386 ms: 1.26x faster                                                       |
| regex_compile           | 103 ms                                                                   | 82.3 ms: 1.26x faster                                                      |
| async_generators        | 214 ms                                                                   | 173 ms: 1.24x faster                                                       |
| float                   | 59.5 ms                                                                  | 48.7 ms: 1.22x faster                                                      |
| docutils                | 1.83 sec                                                                 | 1.52 sec: 1.21x faster                                                     |
| genshi_xml              | 38.8 ms                                                                  | 32.2 ms: 1.20x faster                                                      |
| dask                    | 310 ms                                                                   | 258 ms: 1.20x faster                                                       |
| sqlglot_optimize        | 38.7 ms                                                                  | 32.1 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 507 ms: 1.19x faster                                                       |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.25 ms: 1.19x faster                                                      |
| tornado_http            | 106 ms                                                                   | 89.5 ms: 1.19x faster                                                      |
| 2to3                    | 229 ms                                                                   | 193 ms: 1.19x faster                                                       |
| deepcopy                | 256 us                                                                   | 217 us: 1.18x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 63.1 ms: 1.18x faster                                                      |
| deepcopy_reduce         | 2.18 us                                                                  | 1.87 us: 1.17x faster                                                      |
| json                    | 3.18 ms                                                                  | 2.75 ms: 1.16x faster                                                      |
| sqlglot_normalize       | 201 ms                                                                   | 174 ms: 1.15x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 665 us: 1.15x faster                                                       |
| nbody                   | 71.5 ms                                                                  | 62.3 ms: 1.15x faster                                                      |
| bench_thread_pool       | 953 us                                                                   | 835 us: 1.14x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 12.9 ms: 1.14x faster                                                      |
| thrift                  | 632 us                                                                   | 558 us: 1.13x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 57.5 ms: 1.13x faster                                                      |
| fannkuch                | 252 ms                                                                   | 227 ms: 1.11x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 282 ms: 1.11x faster                                                       |
| scimark_fft             | 187 ms                                                                   | 170 ms: 1.10x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 49.0 ms: 1.10x faster                                                      |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.10x faster                                                      |
| regex_dna               | 131 ms                                                                   | 120 ms: 1.09x faster                                                       |
| xml_etree_parse         | 95.6 ms                                                                  | 87.6 ms: 1.09x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 43.1 ms: 1.09x faster                                                      |
| sympy_str               | 189 ms                                                                   | 175 ms: 1.08x faster                                                       |
| unpickle                | 8.88 us                                                                  | 8.25 us: 1.08x faster                                                      |
| sqlite_synth            | 1.85 us                                                                  | 1.71 us: 1.08x faster                                                      |
| meteor_contest          | 74.3 ms                                                                  | 69.3 ms: 1.07x faster                                                      |
| json_loads              | 14.2 us                                                                  | 13.3 us: 1.07x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 96.1 ms: 1.06x faster                                                      |
| python_startup          | 19.3 ms                                                                  | 18.2 ms: 1.06x faster                                                      |
| mdp                     | 1.60 sec                                                                 | 1.53 sec: 1.05x faster                                                     |
| coroutines              | 15.6 ms                                                                  | 15.0 ms: 1.04x faster                                                      |
| comprehensions          | 16.0 us                                                                  | 15.4 us: 1.04x faster                                                      |
| pathlib                 | 75.2 ms                                                                  | 72.6 ms: 1.04x faster                                                      |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.3 ms: 1.02x faster                                                      |
| pickle                  | 6.67 us                                                                  | 6.57 us: 1.01x faster                                                      |
| logging_format          | 6.53 us                                                                  | 6.56 us: 1.00x slower                                                      |
| pidigits                | 145 ms                                                                   | 146 ms: 1.01x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.62 us: 1.02x slower                                                      |
| unpickle_list           | 2.71 us                                                                  | 2.79 us: 1.03x slower                                                      |
| logging_simple          | 6.12 us                                                                  | 6.31 us: 1.03x slower                                                      |
| bench_mp_pool           | 59.2 ms                                                                  | 61.2 ms: 1.03x slower                                                      |
| regex_effbot            | 1.64 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.04x slower                                                      |
| telco                   | 3.77 ms                                                                  | 3.95 ms: 1.05x slower                                                      |
| asyncio_tcp             | 664 ms                                                                   | 708 ms: 1.07x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.44 ms: 1.08x slower                                                      |
| pickle_dict             | 16.7 us                                                                  | 18.3 us: 1.10x slower                                                      |
| generators              | 31.4 ms                                                                  | 35.7 ms: 1.14x slower                                                      |
| coverage                | 37.5 ms                                                                  | 52.0 ms: 1.39x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.18x faster                                                               |
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
