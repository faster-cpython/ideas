
# Results vs. 3.10.4

- fork: python
- ref: 594de165bf2f21d6b28e
- machine: windows-amd64
- commit hash: 594de16
- commit date: 2022-11-28
- overall geometric mean: 1.21x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 193 ms: 1.19x faster                                                        |
| chameleon      | 5.77 ms                                                                  | 4.45 ms: 1.30x faster                                                       |
| docutils       | 1.83 sec                                                                 | 1.56 sec: 1.17x faster                                                      |
| html5lib       | 47.3 ms                                                                  | 35.7 ms: 1.33x faster                                                       |
| tornado_http   | 106 ms                                                                   | 92.1 ms: 1.16x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.5 ms                                                                  | 57.1 ms: 1.25x faster                                                       |
| float          | 59.5 ms                                                                  | 48.3 ms: 1.23x faster                                                       |
| pidigits       | 145 ms                                                                   | 150 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 79.4 ms: 1.30x faster                                                       |
| regex_dna      | 131 ms                                                                   | 121 ms: 1.08x faster                                                        |
| regex_v8       | 15.1 ms                                                                  | 14.1 ms: 1.07x faster                                                       |
| regex_effbot   | 1.64 ms                                                                  | 1.57 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.36 ms: 1.68x faster                                                       |
| pickle_pure_python   | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| unpickle_pure_python | 179 us                                                                   | 121 us: 1.48x faster                                                        |
| xml_etree_process    | 43.0 ms                                                                  | 33.7 ms: 1.28x faster                                                       |
| unpickle             | 8.88 us                                                                  | 7.78 us: 1.14x faster                                                       |
| xml_etree_generate   | 53.8 ms                                                                  | 49.2 ms: 1.09x faster                                                       |
| xml_etree_parse      | 95.6 ms                                                                  | 88.8 ms: 1.08x faster                                                       |
| json_loads           | 14.2 us                                                                  | 13.2 us: 1.07x faster                                                       |
| unpickle_list        | 2.71 us                                                                  | 2.61 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 62.5 ms                                                                  | 60.8 ms: 1.03x faster                                                       |
| pickle               | 6.67 us                                                                  | 6.81 us: 1.02x slower                                                       |
| pickle_list          | 2.57 us                                                                  | 2.85 us: 1.11x slower                                                       |
| pickle_dict          | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.6 ms: 1.03x faster                                                       |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 20.5 ms: 1.42x faster                                                       |
| mako            | 8.69 ms                                                                  | 6.14 ms: 1.42x faster                                                       |
| genshi_text     | 18.5 ms                                                                  | 13.9 ms: 1.33x faster                                                       |
| genshi_xml      | 38.8 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.34x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2+-594de16 |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 1.97 ms: 2.10x faster                                                       |
| richards                | 41.0 ms                                                                  | 23.8 ms: 1.72x faster                                                       |
| go                      | 143 ms                                                                   | 84.3 ms: 1.70x faster                                                       |
| json_dumps              | 9.00 ms                                                                  | 5.36 ms: 1.68x faster                                                       |
| logging_silent          | 94.6 ns                                                                  | 56.7 ns: 1.67x faster                                                       |
| scimark_sor             | 104 ms                                                                   | 64.4 ms: 1.61x faster                                                       |
| mypy2                   | 337 ms                                                                   | 215 ms: 1.57x faster                                                        |
| scimark_lu              | 83.9 ms                                                                  | 55.0 ms: 1.52x faster                                                       |
| scimark_monte_carlo     | 56.0 ms                                                                  | 36.9 ms: 1.52x faster                                                       |
| raytrace                | 267 ms                                                                   | 177 ms: 1.51x faster                                                        |
| pickle_pure_python      | 264 us                                                                   | 176 us: 1.50x faster                                                        |
| unpack_sequence         | 39.4 ns                                                                  | 26.4 ns: 1.49x faster                                                       |
| unpickle_pure_python    | 179 us                                                                   | 121 us: 1.48x faster                                                        |
| pyflate                 | 388 ms                                                                   | 266 ms: 1.46x faster                                                        |
| sqlglot_parse           | 1.22 ms                                                                  | 838 us: 1.45x faster                                                        |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.03 ms: 1.43x faster                                                       |
| django_template         | 29.2 ms                                                                  | 20.5 ms: 1.42x faster                                                       |
| hexiom                  | 5.45 ms                                                                  | 3.85 ms: 1.42x faster                                                       |
| crypto_pyaes            | 61.4 ms                                                                  | 43.4 ms: 1.42x faster                                                       |
| mako                    | 8.69 ms                                                                  | 6.14 ms: 1.42x faster                                                       |
| deepcopy_memo           | 28.4 us                                                                  | 20.3 us: 1.40x faster                                                       |
| chaos                   | 58.4 ms                                                                  | 42.5 ms: 1.38x faster                                                       |
| pycparser               | 873 ms                                                                   | 638 ms: 1.37x faster                                                        |
| pprint_pformat          | 1.23 sec                                                                 | 900 ms: 1.36x faster                                                        |
| thrift                  | 632 us                                                                   | 466 us: 1.36x faster                                                        |
| pprint_safe_repr        | 593 ms                                                                   | 443 ms: 1.34x faster                                                        |
| async_tree_io           | 1.02 sec                                                                 | 767 ms: 1.33x faster                                                        |
| genshi_text             | 18.5 ms                                                                  | 13.9 ms: 1.33x faster                                                       |
| html5lib                | 47.3 ms                                                                  | 35.7 ms: 1.33x faster                                                       |
| async_tree_none         | 414 ms                                                                   | 315 ms: 1.32x faster                                                        |
| regex_compile           | 103 ms                                                                   | 79.4 ms: 1.30x faster                                                       |
| async_tree_memoization  | 485 ms                                                                   | 373 ms: 1.30x faster                                                        |
| chameleon               | 5.77 ms                                                                  | 4.45 ms: 1.30x faster                                                       |
| xml_etree_process       | 43.0 ms                                                                  | 33.7 ms: 1.28x faster                                                       |
| async_generators        | 214 ms                                                                   | 168 ms: 1.27x faster                                                        |
| nbody                   | 71.5 ms                                                                  | 57.1 ms: 1.25x faster                                                       |
| float                   | 59.5 ms                                                                  | 48.3 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 493 ms: 1.23x faster                                                        |
| sqlglot_optimize        | 38.7 ms                                                                  | 31.8 ms: 1.22x faster                                                       |
| spectral_norm           | 74.3 ms                                                                  | 61.0 ms: 1.22x faster                                                       |
| genshi_xml              | 38.8 ms                                                                  | 32.0 ms: 1.21x faster                                                       |
| json                    | 3.18 ms                                                                  | 2.65 ms: 1.20x faster                                                       |
| deepcopy                | 256 us                                                                   | 214 us: 1.20x faster                                                        |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.24 ms: 1.19x faster                                                       |
| sqlglot_normalize       | 201 ms                                                                   | 168 ms: 1.19x faster                                                        |
| dask                    | 310 ms                                                                   | 261 ms: 1.19x faster                                                        |
| 2to3                    | 229 ms                                                                   | 193 ms: 1.19x faster                                                        |
| deepcopy_reduce         | 2.18 us                                                                  | 1.84 us: 1.19x faster                                                       |
| fannkuch                | 252 ms                                                                   | 215 ms: 1.17x faster                                                        |
| docutils                | 1.83 sec                                                                 | 1.56 sec: 1.17x faster                                                      |
| dulwich_log             | 47.0 ms                                                                  | 40.5 ms: 1.16x faster                                                       |
| tornado_http            | 106 ms                                                                   | 92.1 ms: 1.16x faster                                                       |
| bench_thread_pool       | 953 us                                                                   | 830 us: 1.15x faster                                                        |
| scimark_fft             | 187 ms                                                                   | 163 ms: 1.14x faster                                                        |
| unpickle                | 8.88 us                                                                  | 7.78 us: 1.14x faster                                                       |
| nqueens                 | 64.8 ms                                                                  | 57.1 ms: 1.14x faster                                                       |
| sympy_integrate         | 14.7 ms                                                                  | 13.0 ms: 1.13x faster                                                       |
| sympy_expand            | 313 ms                                                                   | 278 ms: 1.12x faster                                                        |
| meteor_contest          | 74.3 ms                                                                  | 66.7 ms: 1.11x faster                                                       |
| xml_etree_generate      | 53.8 ms                                                                  | 49.2 ms: 1.09x faster                                                       |
| create_gc_cycles        | 764 us                                                                   | 700 us: 1.09x faster                                                        |
| sympy_str               | 189 ms                                                                   | 174 ms: 1.08x faster                                                        |
| regex_dna               | 131 ms                                                                   | 121 ms: 1.08x faster                                                        |
| xml_etree_parse         | 95.6 ms                                                                  | 88.8 ms: 1.08x faster                                                       |
| json_loads              | 14.2 us                                                                  | 13.2 us: 1.07x faster                                                       |
| regex_v8                | 15.1 ms                                                                  | 14.1 ms: 1.07x faster                                                       |
| coroutines              | 15.6 ms                                                                  | 14.6 ms: 1.07x faster                                                       |
| sqlite_synth            | 1.85 us                                                                  | 1.74 us: 1.06x faster                                                       |
| comprehensions          | 16.0 us                                                                  | 15.1 us: 1.06x faster                                                       |
| mdp                     | 1.60 sec                                                                 | 1.52 sec: 1.05x faster                                                      |
| sympy_sum               | 102 ms                                                                   | 97.4 ms: 1.05x faster                                                       |
| regex_effbot            | 1.64 ms                                                                  | 1.57 ms: 1.05x faster                                                       |
| unpickle_list           | 2.71 us                                                                  | 2.61 us: 1.04x faster                                                       |
| python_startup          | 19.3 ms                                                                  | 18.6 ms: 1.03x faster                                                       |
| xml_etree_iterparse     | 62.5 ms                                                                  | 60.8 ms: 1.03x faster                                                       |
| pathlib                 | 75.2 ms                                                                  | 73.7 ms: 1.02x faster                                                       |
| telco                   | 3.77 ms                                                                  | 3.73 ms: 1.01x faster                                                       |
| pickle                  | 6.67 us                                                                  | 6.81 us: 1.02x slower                                                       |
| logging_simple          | 6.12 us                                                                  | 6.27 us: 1.02x slower                                                       |
| logging_format          | 6.53 us                                                                  | 6.73 us: 1.03x slower                                                       |
| pidigits                | 145 ms                                                                   | 150 ms: 1.04x slower                                                        |
| bench_mp_pool           | 59.2 ms                                                                  | 62.9 ms: 1.06x slower                                                       |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.07x slower                                                       |
| gc_traversal            | 1.33 ms                                                                  | 1.47 ms: 1.10x slower                                                       |
| asyncio_tcp             | 664 ms                                                                   | 731 ms: 1.10x slower                                                        |
| generators              | 31.4 ms                                                                  | 34.8 ms: 1.11x slower                                                       |
| pickle_list             | 2.57 us                                                                  | 2.85 us: 1.11x slower                                                       |
| pickle_dict             | 16.7 us                                                                  | 19.0 us: 1.14x slower                                                       |
| coverage                | 37.5 ms                                                                  | 52.5 ms: 1.40x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.21x faster                                                                |
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
