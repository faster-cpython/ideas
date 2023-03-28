
# Results vs. 3.10.4

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: linux-x86_64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.30x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 245 ms: 1.37x faster                                                  |
| chameleon      | 9.13 ms                                                             | 6.30 ms: 1.45x faster                                                 |
| docutils       | 3.19 sec                                                            | 2.50 sec: 1.28x faster                                                |
| html5lib       | 86.4 ms                                                             | 58.9 ms: 1.46x faster                                                 |
| tornado_http   | 129 ms                                                              | 93.1 ms: 1.38x faster                                                 |
| Geometric mean | (ref)                                                               | 1.39x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 93.9 ms: 1.55x faster                                                 |
| float          | 110 ms                                                              | 72.0 ms: 1.52x faster                                                 |
| pidigits       | 190 ms                                                              | 189 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                               | 1.33x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 127 ms: 1.40x faster                                                  |
| regex_v8       | 24.9 ms                                                             | 21.1 ms: 1.18x faster                                                 |
| regex_dna      | 213 ms                                                              | 208 ms: 1.03x faster                                                  |
| regex_effbot   | 3.22 ms                                                             | 3.47 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                               | 1.12x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 283 us: 1.61x faster                                                  |
| unpickle_pure_python | 300 us                                                              | 200 us: 1.50x faster                                                  |
| json_dumps           | 13.7 ms                                                             | 9.66 ms: 1.42x faster                                                 |
| xml_etree_process    | 74.8 ms                                                             | 53.9 ms: 1.39x faster                                                 |
| xml_etree_generate   | 94.9 ms                                                             | 77.2 ms: 1.23x faster                                                 |
| json_loads           | 29.3 us                                                             | 23.9 us: 1.23x faster                                                 |
| pickle_list          | 4.73 us                                                             | 4.06 us: 1.16x faster                                                 |
| unpickle             | 15.0 us                                                             | 12.9 us: 1.16x faster                                                 |
| xml_etree_parse      | 164 ms                                                              | 149 ms: 1.10x faster                                                  |
| xml_etree_iterparse  | 111 ms                                                              | 103 ms: 1.08x faster                                                  |
| pickle               | 10.2 us                                                             | 9.88 us: 1.04x faster                                                 |
| unpickle_list        | 4.94 us                                                             | 4.98 us: 1.01x slower                                                 |
| pickle_dict          | 27.8 us                                                             | 30.8 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                               | 1.20x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.58 ms: 1.65x faster                                                 |
| python_startup_no_site | 5.80 ms                                                             | 6.12 ms: 1.06x slower                                                 |
| Geometric mean         | (ref)                                                               | 1.25x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.39 ms: 1.57x faster                                                 |
| genshi_text     | 30.4 ms                                                             | 20.2 ms: 1.51x faster                                                 |
| django_template | 45.8 ms                                                             | 32.8 ms: 1.40x faster                                                 |
| genshi_xml      | 64.3 ms                                                             | 47.0 ms: 1.37x faster                                                 |
| Geometric mean  | (ref)                                                               | 1.46x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 7.30 ms                                                             | 3.22 ms: 2.27x faster                                                 |
| scimark_sor             | 198 ms                                                              | 105 ms: 1.88x faster                                                  |
| logging_silent          | 169 ns                                                              | 93.4 ns: 1.81x faster                                                 |
| richards                | 74.2 ms                                                             | 41.8 ms: 1.77x faster                                                 |
| raytrace                | 470 ms                                                              | 277 ms: 1.70x faster                                                  |
| go                      | 226 ms                                                              | 135 ms: 1.68x faster                                                  |
| pyflate                 | 671 ms                                                              | 402 ms: 1.67x faster                                                  |
| python_startup          | 14.1 ms                                                             | 8.58 ms: 1.65x faster                                                 |
| pickle_pure_python      | 457 us                                                              | 283 us: 1.61x faster                                                  |
| chaos                   | 106 ms                                                              | 65.8 ms: 1.61x faster                                                 |
| scimark_monte_carlo     | 109 ms                                                              | 68.0 ms: 1.60x faster                                                 |
| spectral_norm           | 150 ms                                                              | 94.9 ms: 1.58x faster                                                 |
| hexiom                  | 9.50 ms                                                             | 6.04 ms: 1.57x faster                                                 |
| mako                    | 14.7 ms                                                             | 9.39 ms: 1.57x faster                                                 |
| crypto_pyaes            | 117 ms                                                              | 74.6 ms: 1.56x faster                                                 |
| sqlglot_parse           | 2.07 ms                                                             | 1.33 ms: 1.55x faster                                                 |
| nbody                   | 146 ms                                                              | 93.9 ms: 1.55x faster                                                 |
| deepcopy_memo           | 51.8 us                                                             | 33.6 us: 1.54x faster                                                 |
| float                   | 110 ms                                                              | 72.0 ms: 1.52x faster                                                 |
| sqlglot_transpile       | 2.45 ms                                                             | 1.62 ms: 1.52x faster                                                 |
| genshi_text             | 30.4 ms                                                             | 20.2 ms: 1.51x faster                                                 |
| unpickle_pure_python    | 300 us                                                              | 200 us: 1.50x faster                                                  |
| scimark_lu              | 160 ms                                                              | 108 ms: 1.48x faster                                                  |
| html5lib                | 86.4 ms                                                             | 58.9 ms: 1.46x faster                                                 |
| chameleon               | 9.13 ms                                                             | 6.30 ms: 1.45x faster                                                 |
| logging_simple          | 8.21 us                                                             | 5.70 us: 1.44x faster                                                 |
| logging_format          | 9.07 us                                                             | 6.30 us: 1.44x faster                                                 |
| unpack_sequence         | 65.6 ns                                                             | 45.7 ns: 1.44x faster                                                 |
| pycparser               | 1.53 sec                                                            | 1.08 sec: 1.42x faster                                                |
| pprint_pformat          | 1.98 sec                                                            | 1.39 sec: 1.42x faster                                                |
| json_dumps              | 13.7 ms                                                             | 9.66 ms: 1.42x faster                                                 |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.00 ms: 1.41x faster                                                 |
| regex_compile           | 177 ms                                                              | 127 ms: 1.40x faster                                                  |
| django_template         | 45.8 ms                                                             | 32.8 ms: 1.40x faster                                                 |
| pprint_safe_repr        | 953 ms                                                              | 685 ms: 1.39x faster                                                  |
| xml_etree_process       | 74.8 ms                                                             | 53.9 ms: 1.39x faster                                                 |
| thrift                  | 1.04 ms                                                             | 748 us: 1.39x faster                                                  |
| tornado_http            | 129 ms                                                              | 93.1 ms: 1.38x faster                                                 |
| scimark_fft             | 425 ms                                                              | 309 ms: 1.38x faster                                                  |
| 2to3                    | 336 ms                                                              | 245 ms: 1.37x faster                                                  |
| genshi_xml              | 64.3 ms                                                             | 47.0 ms: 1.37x faster                                                 |
| async_tree_none         | 713 ms                                                              | 527 ms: 1.35x faster                                                  |
| aiohttp                 | 1.35 ms                                                             | 999 us: 1.35x faster                                                  |
| async_tree_io           | 1.78 sec                                                            | 1.32 sec: 1.35x faster                                                |
| deepcopy                | 438 us                                                              | 328 us: 1.34x faster                                                  |
| gunicorn                | 1.43 ms                                                             | 1.08 ms: 1.33x faster                                                 |
| mypy2                   | 432 ms                                                              | 325 ms: 1.33x faster                                                  |
| deepcopy_reduce         | 3.80 us                                                             | 2.89 us: 1.32x faster                                                 |
| fannkuch                | 485 ms                                                              | 369 ms: 1.32x faster                                                  |
| async_tree_memoization  | 853 ms                                                              | 653 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed | 944 ms                                                              | 730 ms: 1.29x faster                                                  |
| coroutines              | 31.8 ms                                                             | 24.7 ms: 1.29x faster                                                 |
| sqlglot_optimize        | 65.3 ms                                                             | 51.0 ms: 1.28x faster                                                 |
| docutils                | 3.19 sec                                                            | 2.50 sec: 1.28x faster                                                |
| sqlglot_normalize       | 135 ms                                                              | 105 ms: 1.28x faster                                                  |
| dulwich_log             | 76.3 ms                                                             | 61.8 ms: 1.23x faster                                                 |
| xml_etree_generate      | 94.9 ms                                                             | 77.2 ms: 1.23x faster                                                 |
| json_loads              | 29.3 us                                                             | 23.9 us: 1.23x faster                                                 |
| bench_thread_pool       | 954 us                                                              | 780 us: 1.22x faster                                                  |
| nqueens                 | 98.8 ms                                                             | 81.1 ms: 1.22x faster                                                 |
| dask                    | 437 ms                                                              | 360 ms: 1.21x faster                                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.4 ms: 1.19x faster                                                 |
| sympy_expand            | 540 ms                                                              | 456 ms: 1.18x faster                                                  |
| regex_v8                | 24.9 ms                                                             | 21.1 ms: 1.18x faster                                                 |
| async_generators        | 420 ms                                                              | 355 ms: 1.18x faster                                                  |
| json                    | 5.41 ms                                                             | 4.65 ms: 1.16x faster                                                 |
| pickle_list             | 4.73 us                                                             | 4.06 us: 1.16x faster                                                 |
| sympy_str               | 328 ms                                                              | 282 ms: 1.16x faster                                                  |
| comprehensions          | 27.3 us                                                             | 23.4 us: 1.16x faster                                                 |
| unpickle                | 15.0 us                                                             | 12.9 us: 1.16x faster                                                 |
| sqlite_synth            | 2.97 us                                                             | 2.60 us: 1.14x faster                                                 |
| create_gc_cycles        | 1.64 ms                                                             | 1.46 ms: 1.13x faster                                                 |
| meteor_contest          | 115 ms                                                              | 102 ms: 1.12x faster                                                  |
| sympy_sum               | 185 ms                                                              | 165 ms: 1.12x faster                                                  |
| djangocms               | 36.3 us                                                             | 32.5 us: 1.12x faster                                                 |
| pathlib                 | 19.8 ms                                                             | 17.7 ms: 1.11x faster                                                 |
| mdp                     | 2.75 sec                                                            | 2.48 sec: 1.11x faster                                                |
| xml_etree_parse         | 164 ms                                                              | 149 ms: 1.10x faster                                                  |
| xml_etree_iterparse     | 111 ms                                                              | 103 ms: 1.08x faster                                                  |
| telco                   | 6.67 ms                                                             | 6.38 ms: 1.05x faster                                                 |
| asyncio_tcp             | 922 ms                                                              | 884 ms: 1.04x faster                                                  |
| pickle                  | 10.2 us                                                             | 9.88 us: 1.04x faster                                                 |
| regex_dna               | 213 ms                                                              | 208 ms: 1.03x faster                                                  |
| pidigits                | 190 ms                                                              | 189 ms: 1.00x faster                                                  |
| bench_mp_pool           | 24.0 ms                                                             | 24.0 ms: 1.00x slower                                                 |
| unpickle_list           | 4.94 us                                                             | 4.98 us: 1.01x slower                                                 |
| generators              | 75.7 ms                                                             | 77.4 ms: 1.02x slower                                                 |
| python_startup_no_site  | 5.80 ms                                                             | 6.12 ms: 1.06x slower                                                 |
| gc_traversal            | 3.53 ms                                                             | 3.77 ms: 1.07x slower                                                 |
| regex_effbot            | 3.22 ms                                                             | 3.47 ms: 1.08x slower                                                 |
| pickle_dict             | 27.8 us                                                             | 30.8 us: 1.11x slower                                                 |
| coverage                | 70.6 ms                                                             | 101 ms: 1.42x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.30x faster                                                          |
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
