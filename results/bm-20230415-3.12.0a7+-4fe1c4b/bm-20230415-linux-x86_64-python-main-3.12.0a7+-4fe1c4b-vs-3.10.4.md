
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.31x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 249 ms: 1.35x faster                                   |
| chameleon      | 9.13 ms                                                             | 6.33 ms: 1.44x faster                                  |
| docutils       | 3.19 sec                                                            | 2.51 sec: 1.27x faster                                 |
| html5lib       | 86.4 ms                                                             | 60.7 ms: 1.42x faster                                  |
| tornado_http   | 129 ms                                                              | 92.4 ms: 1.39x faster                                  |
| Geometric mean | (ref)                                                               | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 146 ms                                                              | 85.1 ms: 1.71x faster                                  |
| float          | 110 ms                                                              | 73.5 ms: 1.49x faster                                  |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                               | 1.37x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 132 ms: 1.34x faster                                   |
| regex_v8       | 24.9 ms                                                             | 21.3 ms: 1.17x faster                                  |
| regex_dna      | 213 ms                                                              | 202 ms: 1.05x faster                                   |
| regex_effbot   | 3.22 ms                                                             | 3.32 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                               | 1.13x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 285 us: 1.60x faster                                   |
| unpickle_pure_python | 300 us                                                              | 203 us: 1.48x faster                                   |
| json_dumps           | 13.7 ms                                                             | 9.46 ms: 1.45x faster                                  |
| xml_etree_process    | 74.8 ms                                                             | 55.0 ms: 1.36x faster                                  |
| json_loads           | 29.3 us                                                             | 24.1 us: 1.22x faster                                  |
| xml_etree_generate   | 94.9 ms                                                             | 79.9 ms: 1.19x faster                                  |
| xml_etree_iterparse  | 111 ms                                                              | 99.3 ms: 1.12x faster                                  |
| xml_etree_parse      | 164 ms                                                              | 148 ms: 1.10x faster                                   |
| pickle_list          | 4.73 us                                                             | 4.31 us: 1.10x faster                                  |
| unpickle_list        | 4.94 us                                                             | 4.88 us: 1.01x faster                                  |
| pickle               | 10.2 us                                                             | 10.9 us: 1.07x slower                                  |
| pickle_dict          | 27.8 us                                                             | 32.9 us: 1.18x slower                                  |
| Geometric mean       | (ref)                                                               | 1.17x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.91 ms: 1.59x faster                                  |
| python_startup_no_site | 5.80 ms                                                             | 6.60 ms: 1.14x slower                                  |
| Geometric mean         | (ref)                                                               | 1.18x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.86 ms: 1.49x faster                                  |
| genshi_text     | 30.4 ms                                                             | 21.0 ms: 1.45x faster                                  |
| django_template | 45.8 ms                                                             | 32.4 ms: 1.41x faster                                  |
| genshi_xml      | 64.3 ms                                                             | 47.1 ms: 1.36x faster                                  |
| Geometric mean  | (ref)                                                               | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230415-linux-x86_64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:-------------------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 28.0 ms: 2.70x faster                                  |
| deltablue               | 7.30 ms                                                             | 3.20 ms: 2.28x faster                                  |
| asyncio_tcp             | 922 ms                                                              | 501 ms: 1.84x faster                                   |
| richards                | 74.2 ms                                                             | 40.9 ms: 1.82x faster                                  |
| scimark_sor             | 198 ms                                                              | 109 ms: 1.81x faster                                   |
| logging_silent          | 169 ns                                                              | 97.0 ns: 1.74x faster                                  |
| sqlglot_parse           | 2.07 ms                                                             | 1.19 ms: 1.73x faster                                  |
| nbody                   | 146 ms                                                              | 85.1 ms: 1.71x faster                                  |
| go                      | 226 ms                                                              | 133 ms: 1.70x faster                                   |
| raytrace                | 470 ms                                                              | 279 ms: 1.69x faster                                   |
| sqlglot_transpile       | 2.45 ms                                                             | 1.48 ms: 1.66x faster                                  |
| spectral_norm           | 150 ms                                                              | 91.5 ms: 1.64x faster                                  |
| pyflate                 | 671 ms                                                              | 414 ms: 1.62x faster                                   |
| chaos                   | 106 ms                                                              | 65.7 ms: 1.61x faster                                  |
| scimark_monte_carlo     | 109 ms                                                              | 67.6 ms: 1.61x faster                                  |
| pickle_pure_python      | 457 us                                                              | 285 us: 1.60x faster                                   |
| hexiom                  | 9.50 ms                                                             | 5.94 ms: 1.60x faster                                  |
| python_startup          | 14.1 ms                                                             | 8.91 ms: 1.59x faster                                  |
| crypto_pyaes            | 117 ms                                                              | 74.6 ms: 1.56x faster                                  |
| unpack_sequence         | 65.6 ns                                                             | 42.5 ns: 1.54x faster                                  |
| deepcopy_memo           | 51.8 us                                                             | 34.3 us: 1.51x faster                                  |
| scimark_lu              | 160 ms                                                              | 107 ms: 1.50x faster                                   |
| float                   | 110 ms                                                              | 73.5 ms: 1.49x faster                                  |
| mako                    | 14.7 ms                                                             | 9.86 ms: 1.49x faster                                  |
| coroutines              | 31.8 ms                                                             | 21.5 ms: 1.48x faster                                  |
| unpickle_pure_python    | 300 us                                                              | 203 us: 1.48x faster                                   |
| logging_format          | 9.07 us                                                             | 6.22 us: 1.46x faster                                  |
| json_dumps              | 13.7 ms                                                             | 9.46 ms: 1.45x faster                                  |
| genshi_text             | 30.4 ms                                                             | 21.0 ms: 1.45x faster                                  |
| chameleon               | 9.13 ms                                                             | 6.33 ms: 1.44x faster                                  |
| logging_simple          | 8.21 us                                                             | 5.72 us: 1.43x faster                                  |
| html5lib                | 86.4 ms                                                             | 60.7 ms: 1.42x faster                                  |
| pprint_pformat          | 1.98 sec                                                            | 1.39 sec: 1.42x faster                                 |
| django_template         | 45.8 ms                                                             | 32.4 ms: 1.41x faster                                  |
| pprint_safe_repr        | 953 ms                                                              | 675 ms: 1.41x faster                                   |
| tornado_http            | 129 ms                                                              | 92.4 ms: 1.39x faster                                  |
| pycparser               | 1.53 sec                                                            | 1.10 sec: 1.39x faster                                 |
| async_tree_memoization  | 853 ms                                                              | 612 ms: 1.39x faster                                   |
| async_tree_io           | 1.78 sec                                                            | 1.28 sec: 1.39x faster                                 |
| async_tree_none         | 713 ms                                                              | 518 ms: 1.38x faster                                   |
| scimark_fft             | 425 ms                                                              | 309 ms: 1.38x faster                                   |
| genshi_xml              | 64.3 ms                                                             | 47.1 ms: 1.36x faster                                  |
| xml_etree_process       | 74.8 ms                                                             | 55.0 ms: 1.36x faster                                  |
| 2to3                    | 336 ms                                                              | 249 ms: 1.35x faster                                   |
| aiohttp                 | 1.35 ms                                                             | 1.00 ms: 1.34x faster                                  |
| regex_compile           | 177 ms                                                              | 132 ms: 1.34x faster                                   |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.20 ms: 1.34x faster                                  |
| deepcopy                | 438 us                                                              | 328 us: 1.33x faster                                   |
| thrift                  | 1.04 ms                                                             | 780 us: 1.33x faster                                   |
| gunicorn                | 1.43 ms                                                             | 1.08 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed | 944 ms                                                              | 716 ms: 1.32x faster                                   |
| mypy2                   | 432 ms                                                              | 331 ms: 1.30x faster                                   |
| sqlglot_normalize       | 135 ms                                                              | 104 ms: 1.29x faster                                   |
| fannkuch                | 485 ms                                                              | 378 ms: 1.28x faster                                   |
| deepcopy_reduce         | 3.80 us                                                             | 2.97 us: 1.28x faster                                  |
| docutils                | 3.19 sec                                                            | 2.51 sec: 1.27x faster                                 |
| sqlglot_optimize        | 65.3 ms                                                             | 51.4 ms: 1.27x faster                                  |
| comprehensions          | 27.3 us                                                             | 21.5 us: 1.27x faster                                  |
| nqueens                 | 98.8 ms                                                             | 79.1 ms: 1.25x faster                                  |
| dulwich_log             | 76.3 ms                                                             | 61.8 ms: 1.24x faster                                  |
| sqlalchemy_declarative  | 166 ms                                                              | 135 ms: 1.23x faster                                   |
| bench_thread_pool       | 954 us                                                              | 781 us: 1.22x faster                                   |
| json_loads              | 29.3 us                                                             | 24.1 us: 1.22x faster                                  |
| sqlalchemy_imperative   | 21.2 ms                                                             | 17.4 ms: 1.21x faster                                  |
| sympy_integrate         | 24.3 ms                                                             | 20.3 ms: 1.20x faster                                  |
| pylint                  | 521 ms                                                              | 435 ms: 1.20x faster                                   |
| sympy_expand            | 540 ms                                                              | 454 ms: 1.19x faster                                   |
| xml_etree_generate      | 94.9 ms                                                             | 79.9 ms: 1.19x faster                                  |
| sympy_str               | 328 ms                                                              | 279 ms: 1.18x faster                                   |
| regex_v8                | 24.9 ms                                                             | 21.3 ms: 1.17x faster                                  |
| json                    | 5.41 ms                                                             | 4.65 ms: 1.16x faster                                  |
| pathlib                 | 19.8 ms                                                             | 17.0 ms: 1.16x faster                                  |
| sqlite_synth            | 2.97 us                                                             | 2.62 us: 1.14x faster                                  |
| sympy_sum               | 185 ms                                                              | 163 ms: 1.13x faster                                   |
| djangocms               | 36.3 us                                                             | 32.1 us: 1.13x faster                                  |
| xml_etree_iterparse     | 111 ms                                                              | 99.3 ms: 1.12x faster                                  |
| meteor_contest          | 115 ms                                                              | 103 ms: 1.12x faster                                   |
| xml_etree_parse         | 164 ms                                                              | 148 ms: 1.10x faster                                   |
| mdp                     | 2.75 sec                                                            | 2.49 sec: 1.10x faster                                 |
| pickle_list             | 4.73 us                                                             | 4.31 us: 1.10x faster                                  |
| create_gc_cycles        | 1.64 ms                                                             | 1.50 ms: 1.09x faster                                  |
| regex_dna               | 213 ms                                                              | 202 ms: 1.05x faster                                   |
| telco                   | 6.67 ms                                                             | 6.54 ms: 1.02x faster                                  |
| unpickle_list           | 4.94 us                                                             | 4.88 us: 1.01x faster                                  |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                   |
| async_generators        | 420 ms                                                              | 430 ms: 1.02x slower                                   |
| regex_effbot            | 3.22 ms                                                             | 3.32 ms: 1.03x slower                                  |
| pickle                  | 10.2 us                                                             | 10.9 us: 1.07x slower                                  |
| dask                    | 437 ms                                                              | 492 ms: 1.13x slower                                   |
| gc_traversal            | 3.53 ms                                                             | 3.98 ms: 1.13x slower                                  |
| python_startup_no_site  | 5.80 ms                                                             | 6.60 ms: 1.14x slower                                  |
| pickle_dict             | 27.8 us                                                             | 32.9 us: 1.18x slower                                  |
| coverage                | 70.6 ms                                                             | 96.0 ms: 1.36x slower                                  |
| Geometric mean          | (ref)                                                               | 1.31x faster                                           |

Benchmark hidden because not significant (2): unpickle, bench_mp_pool
Ignored benchmarks (1) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging
