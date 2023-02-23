
# Results vs. 3.10.4

- fork: carljm
- ref: inlinecomp2
- machine: linux-x86_64
- commit hash: 9f0fc5b
- commit date: 2023-02-20
- overall geometric mean: 1.32x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 248 ms: 1.34x faster                                          |
| chameleon      | 8.86 ms                                                | 6.32 ms: 1.40x faster                                         |
| docutils       | 3.18 sec                                               | 2.53 sec: 1.26x faster                                        |
| html5lib       | 85.8 ms                                                | 60.4 ms: 1.42x faster                                         |
| tornado_http   | 128 ms                                                 | 94.3 ms: 1.36x faster                                         |
| Geometric mean | (ref)                                                  | 1.35x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 108 ms                                                 | 72.0 ms: 1.50x faster                                         |
| nbody          | 136 ms                                                 | 94.0 ms: 1.45x faster                                         |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                          |
| Geometric mean | (ref)                                                  | 1.30x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                          |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.14x faster                                         |
| regex_dna      | 214 ms                                                 | 207 ms: 1.03x faster                                          |
| regex_effbot   | 3.21 ms                                                | 3.69 ms: 1.15x slower                                         |
| Geometric mean | (ref)                                                  | 1.09x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 281 us: 1.61x faster                                          |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.50x faster                                          |
| json_dumps           | 13.5 ms                                                | 9.49 ms: 1.42x faster                                         |
| xml_etree_process    | 74.5 ms                                                | 55.5 ms: 1.34x faster                                         |
| json_loads           | 28.9 us                                                | 24.1 us: 1.20x faster                                         |
| xml_etree_generate   | 93.3 ms                                                | 80.6 ms: 1.16x faster                                         |
| pickle_list          | 4.50 us                                                | 3.97 us: 1.13x faster                                         |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                          |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                          |
| unpickle             | 14.3 us                                                | 13.4 us: 1.06x faster                                         |
| pickle               | 10.1 us                                                | 10.0 us: 1.01x faster                                         |
| unpickle_list        | 4.99 us                                                | 5.13 us: 1.03x slower                                         |
| pickle_dict          | 28.3 us                                                | 30.0 us: 1.06x slower                                         |
| Geometric mean       | (ref)                                                  | 1.18x faster                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.96 ms: 1.56x faster                                         |
| python_startup_no_site | 5.76 ms                                                | 6.50 ms: 1.13x slower                                         |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.8 ms: 1.47x faster                                         |
| mako            | 14.3 ms                                                | 9.83 ms: 1.45x faster                                         |
| django_template | 46.3 ms                                                | 32.7 ms: 1.41x faster                                         |
| genshi_xml      | 63.6 ms                                                | 47.9 ms: 1.33x faster                                         |
| Geometric mean  | (ref)                                                  | 1.41x faster                                                  |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.9 ms: 2.53x faster                                         |
| deltablue               | 7.39 ms                                                | 3.16 ms: 2.34x faster                                         |
| logging_silent          | 173 ns                                                 | 91.7 ns: 1.89x faster                                         |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                          |
| richards                | 71.4 ms                                                | 41.3 ms: 1.73x faster                                         |
| go                      | 226 ms                                                 | 131 ms: 1.73x faster                                          |
| pyflate                 | 675 ms                                                 | 398 ms: 1.70x faster                                          |
| raytrace                | 461 ms                                                 | 281 ms: 1.64x faster                                          |
| chaos                   | 104 ms                                                 | 63.5 ms: 1.64x faster                                         |
| scimark_monte_carlo     | 105 ms                                                 | 64.7 ms: 1.62x faster                                         |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.61x faster                                          |
| crypto_pyaes            | 118 ms                                                 | 73.7 ms: 1.59x faster                                         |
| hexiom                  | 9.42 ms                                                | 5.94 ms: 1.59x faster                                         |
| python_startup          | 13.9 ms                                                | 8.96 ms: 1.56x faster                                         |
| spectral_norm           | 148 ms                                                 | 96.2 ms: 1.54x faster                                         |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.50x faster                                          |
| float                   | 108 ms                                                 | 72.0 ms: 1.50x faster                                         |
| genshi_text             | 30.6 ms                                                | 20.8 ms: 1.47x faster                                         |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.47x faster                                          |
| deepcopy_memo           | 50.0 us                                                | 34.2 us: 1.46x faster                                         |
| mako                    | 14.3 ms                                                | 9.83 ms: 1.45x faster                                         |
| nbody                   | 136 ms                                                 | 94.0 ms: 1.45x faster                                         |
| coroutines              | 31.7 ms                                                | 21.8 ms: 1.45x faster                                         |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                        |
| json_dumps              | 13.5 ms                                                | 9.49 ms: 1.42x faster                                         |
| html5lib                | 85.8 ms                                                | 60.4 ms: 1.42x faster                                         |
| sqlglot_parse           | 2.04 ms                                                | 1.44 ms: 1.41x faster                                         |
| django_template         | 46.3 ms                                                | 32.7 ms: 1.41x faster                                         |
| async_tree_none         | 713 ms                                                 | 505 ms: 1.41x faster                                          |
| logging_format          | 8.92 us                                                | 6.33 us: 1.41x faster                                         |
| async_tree_io           | 1.78 sec                                               | 1.26 sec: 1.41x faster                                        |
| pprint_safe_repr        | 943 ms                                                 | 671 ms: 1.41x faster                                          |
| logging_simple          | 8.06 us                                                | 5.73 us: 1.40x faster                                         |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.40x faster                                         |
| chameleon               | 8.86 ms                                                | 6.32 ms: 1.40x faster                                         |
| async_tree_memoization  | 854 ms                                                 | 611 ms: 1.40x faster                                          |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.93 ms: 1.39x faster                                         |
| thrift                  | 1.03 ms                                                | 742 us: 1.39x faster                                          |
| unpack_sequence         | 59.5 ns                                                | 42.9 ns: 1.39x faster                                         |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                          |
| tornado_http            | 128 ms                                                 | 94.3 ms: 1.36x faster                                         |
| pycparser               | 1.51 sec                                               | 1.11 sec: 1.36x faster                                        |
| sqlglot_normalize       | 135 ms                                                 | 99.8 ms: 1.35x faster                                         |
| scimark_fft             | 414 ms                                                 | 309 ms: 1.34x faster                                          |
| 2to3                    | 332 ms                                                 | 248 ms: 1.34x faster                                          |
| xml_etree_process       | 74.5 ms                                                | 55.5 ms: 1.34x faster                                         |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                         |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.33x faster                                         |
| genshi_xml              | 63.6 ms                                                | 47.9 ms: 1.33x faster                                         |
| sqlglot_optimize        | 65.3 ms                                                | 49.7 ms: 1.32x faster                                         |
| deepcopy                | 429 us                                                 | 328 us: 1.31x faster                                          |
| fannkuch                | 477 ms                                                 | 368 ms: 1.30x faster                                          |
| async_tree_cpu_io_mixed | 949 ms                                                 | 739 ms: 1.28x faster                                          |
| deepcopy_reduce         | 3.75 us                                                | 2.96 us: 1.27x faster                                         |
| docutils                | 3.18 sec                                               | 2.53 sec: 1.26x faster                                        |
| nqueens                 | 99.3 ms                                                | 80.3 ms: 1.24x faster                                         |
| sympy_expand            | 537 ms                                                 | 444 ms: 1.21x faster                                          |
| bench_thread_pool       | 943 us                                                 | 783 us: 1.20x faster                                          |
| sqlalchemy_declarative  | 165 ms                                                 | 137 ms: 1.20x faster                                          |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.5 ms: 1.20x faster                                         |
| json_loads              | 28.9 us                                                | 24.1 us: 1.20x faster                                         |
| sympy_integrate         | 23.9 ms                                                | 20.1 ms: 1.19x faster                                         |
| dulwich_log             | 75.5 ms                                                | 63.6 ms: 1.19x faster                                         |
| sympy_str               | 324 ms                                                 | 278 ms: 1.17x faster                                          |
| json                    | 5.35 ms                                                | 4.61 ms: 1.16x faster                                         |
| xml_etree_generate      | 93.3 ms                                                | 80.6 ms: 1.16x faster                                         |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.14x faster                                         |
| mdp                     | 2.82 sec                                               | 2.48 sec: 1.14x faster                                        |
| pickle_list             | 4.50 us                                                | 3.97 us: 1.13x faster                                         |
| sympy_sum               | 183 ms                                                 | 164 ms: 1.12x faster                                          |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.11x faster                                          |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                          |
| sqlite_synth            | 2.90 us                                                | 2.63 us: 1.11x faster                                         |
| pathlib                 | 20.0 ms                                                | 18.3 ms: 1.10x faster                                         |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                          |
| unpickle                | 14.3 us                                                | 13.4 us: 1.06x faster                                         |
| telco                   | 6.68 ms                                                | 6.42 ms: 1.04x faster                                         |
| regex_dna               | 214 ms                                                 | 207 ms: 1.03x faster                                          |
| async_generators        | 428 ms                                                 | 417 ms: 1.02x faster                                          |
| pickle                  | 10.1 us                                                | 10.0 us: 1.01x faster                                         |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                          |
| unpickle_list           | 4.99 us                                                | 5.13 us: 1.03x slower                                         |
| pickle_dict             | 28.3 us                                                | 30.0 us: 1.06x slower                                         |
| python_startup_no_site  | 5.76 ms                                                | 6.50 ms: 1.13x slower                                         |
| regex_effbot            | 3.21 ms                                                | 3.69 ms: 1.15x slower                                         |
| coverage                | 75.3 ms                                                | 96.1 ms: 1.28x slower                                         |
| Geometric mean          | (ref)                                                  | 1.32x faster                                                  |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230220-3.12.0a5+-9f0fc5b/bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5+-9f0fc5b.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
