
# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialized_send
- machine: linux-x86_64
- commit hash: 685d559
- commit date: 2023-02-10
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 246 ms: 1.35x faster                                                         |
| chameleon      | 8.86 ms                                                | 6.51 ms: 1.36x faster                                                        |
| docutils       | 3.18 sec                                               | 2.54 sec: 1.25x faster                                                       |
| html5lib       | 85.8 ms                                                | 61.3 ms: 1.40x faster                                                        |
| tornado_http   | 128 ms                                                 | 95.1 ms: 1.35x faster                                                        |
| Geometric mean | (ref)                                                  | 1.34x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 136 ms                                                 | 93.0 ms: 1.47x faster                                                        |
| float          | 108 ms                                                 | 73.9 ms: 1.46x faster                                                        |
| pidigits       | 190 ms                                                 | 197 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                  | 1.27x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 131 ms: 1.33x faster                                                         |
| regex_v8       | 25.0 ms                                                | 22.3 ms: 1.12x faster                                                        |
| regex_dna      | 214 ms                                                 | 211 ms: 1.01x faster                                                         |
| regex_effbot   | 3.21 ms                                                | 3.38 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 283 us: 1.60x faster                                                         |
| unpickle_pure_python | 297 us                                                 | 199 us: 1.49x faster                                                         |
| json_dumps           | 13.5 ms                                                | 9.46 ms: 1.43x faster                                                        |
| xml_etree_process    | 74.5 ms                                                | 55.9 ms: 1.33x faster                                                        |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                                        |
| xml_etree_generate   | 93.3 ms                                                | 80.6 ms: 1.16x faster                                                        |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                                         |
| pickle_list          | 4.50 us                                                | 4.12 us: 1.09x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                                         |
| unpickle             | 14.3 us                                                | 13.7 us: 1.04x faster                                                        |
| pickle               | 10.1 us                                                | 10.1 us: 1.01x faster                                                        |
| pickle_dict          | 28.3 us                                                | 30.9 us: 1.09x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.96 ms: 1.56x faster                                                        |
| python_startup_no_site | 5.76 ms                                                | 6.49 ms: 1.13x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.8 ms: 1.47x faster                                                        |
| mako            | 14.3 ms                                                | 9.75 ms: 1.46x faster                                                        |
| django_template | 46.3 ms                                                | 32.5 ms: 1.42x faster                                                        |
| genshi_xml      | 63.6 ms                                                | 48.1 ms: 1.32x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.42x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 31.1 ms: 2.43x faster                                                        |
| deltablue               | 7.39 ms                                                | 3.19 ms: 2.32x faster                                                        |
| logging_silent          | 173 ns                                                 | 94.0 ns: 1.84x faster                                                        |
| scimark_sor             | 193 ms                                                 | 109 ms: 1.78x faster                                                         |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                                         |
| pyflate                 | 675 ms                                                 | 403 ms: 1.68x faster                                                         |
| richards                | 71.4 ms                                                | 42.9 ms: 1.66x faster                                                        |
| raytrace                | 461 ms                                                 | 285 ms: 1.62x faster                                                         |
| pickle_pure_python      | 453 us                                                 | 283 us: 1.60x faster                                                         |
| crypto_pyaes            | 118 ms                                                 | 73.7 ms: 1.60x faster                                                        |
| scimark_monte_carlo     | 105 ms                                                 | 66.1 ms: 1.58x faster                                                        |
| chaos                   | 104 ms                                                 | 66.1 ms: 1.57x faster                                                        |
| python_startup          | 13.9 ms                                                | 8.96 ms: 1.56x faster                                                        |
| spectral_norm           | 148 ms                                                 | 95.8 ms: 1.55x faster                                                        |
| hexiom                  | 9.42 ms                                                | 6.14 ms: 1.53x faster                                                        |
| unpickle_pure_python    | 297 us                                                 | 199 us: 1.49x faster                                                         |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.49x faster                                                         |
| genshi_text             | 30.6 ms                                                | 20.8 ms: 1.47x faster                                                        |
| nbody                   | 136 ms                                                 | 93.0 ms: 1.47x faster                                                        |
| mako                    | 14.3 ms                                                | 9.75 ms: 1.46x faster                                                        |
| float                   | 108 ms                                                 | 73.9 ms: 1.46x faster                                                        |
| deepcopy_memo           | 50.0 us                                                | 34.5 us: 1.45x faster                                                        |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.43x faster                                                        |
| logging_format          | 8.92 us                                                | 6.26 us: 1.43x faster                                                        |
| json_dumps              | 13.5 ms                                                | 9.46 ms: 1.43x faster                                                        |
| django_template         | 46.3 ms                                                | 32.5 ms: 1.42x faster                                                        |
| coroutines              | 31.7 ms                                                | 22.3 ms: 1.42x faster                                                        |
| logging_simple          | 8.06 us                                                | 5.67 us: 1.42x faster                                                        |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.87 ms: 1.42x faster                                                        |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.40x faster                                                        |
| pprint_pformat          | 1.97 sec                                               | 1.41 sec: 1.40x faster                                                       |
| html5lib                | 85.8 ms                                                | 61.3 ms: 1.40x faster                                                        |
| unpack_sequence         | 59.5 ns                                                | 43.4 ns: 1.37x faster                                                        |
| pycparser               | 1.51 sec                                               | 1.11 sec: 1.37x faster                                                       |
| pprint_safe_repr        | 943 ms                                                 | 690 ms: 1.37x faster                                                         |
| chameleon               | 8.86 ms                                                | 6.51 ms: 1.36x faster                                                        |
| async_tree_none         | 713 ms                                                 | 525 ms: 1.36x faster                                                         |
| 2to3                    | 332 ms                                                 | 246 ms: 1.35x faster                                                         |
| tornado_http            | 128 ms                                                 | 95.1 ms: 1.35x faster                                                        |
| async_tree_memoization  | 854 ms                                                 | 633 ms: 1.35x faster                                                         |
| thrift                  | 1.03 ms                                                | 766 us: 1.35x faster                                                         |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                                       |
| xml_etree_process       | 74.5 ms                                                | 55.9 ms: 1.33x faster                                                        |
| regex_compile           | 174 ms                                                 | 131 ms: 1.33x faster                                                         |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                                        |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.32x faster                                                        |
| scimark_fft             | 414 ms                                                 | 313 ms: 1.32x faster                                                         |
| genshi_xml              | 63.6 ms                                                | 48.1 ms: 1.32x faster                                                        |
| sqlglot_normalize       | 135 ms                                                 | 103 ms: 1.31x faster                                                         |
| deepcopy                | 429 us                                                 | 333 us: 1.29x faster                                                         |
| sqlglot_optimize        | 65.3 ms                                                | 50.6 ms: 1.29x faster                                                        |
| deepcopy_reduce         | 3.75 us                                                | 2.92 us: 1.28x faster                                                        |
| fannkuch                | 477 ms                                                 | 376 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed | 949 ms                                                 | 750 ms: 1.27x faster                                                         |
| docutils                | 3.18 sec                                               | 2.54 sec: 1.25x faster                                                       |
| nqueens                 | 99.3 ms                                                | 81.2 ms: 1.22x faster                                                        |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                                        |
| sympy_integrate         | 23.9 ms                                                | 19.8 ms: 1.21x faster                                                        |
| sqlalchemy_declarative  | 165 ms                                                 | 138 ms: 1.20x faster                                                         |
| sympy_str               | 324 ms                                                 | 270 ms: 1.20x faster                                                         |
| bench_thread_pool       | 943 us                                                 | 789 us: 1.20x faster                                                         |
| dulwich_log             | 75.5 ms                                                | 63.4 ms: 1.19x faster                                                        |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.7 ms: 1.19x faster                                                        |
| sympy_expand            | 537 ms                                                 | 456 ms: 1.18x faster                                                         |
| sympy_sum               | 183 ms                                                 | 158 ms: 1.16x faster                                                         |
| json                    | 5.35 ms                                                | 4.61 ms: 1.16x faster                                                        |
| xml_etree_generate      | 93.3 ms                                                | 80.6 ms: 1.16x faster                                                        |
| sqlite_synth            | 2.90 us                                                | 2.58 us: 1.13x faster                                                        |
| regex_v8                | 25.0 ms                                                | 22.3 ms: 1.12x faster                                                        |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                                        |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                                         |
| pickle_list             | 4.50 us                                                | 4.12 us: 1.09x faster                                                        |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                                         |
| meteor_contest          | 114 ms                                                 | 106 ms: 1.07x faster                                                         |
| telco                   | 6.68 ms                                                | 6.32 ms: 1.06x faster                                                        |
| async_generators        | 428 ms                                                 | 410 ms: 1.04x faster                                                         |
| unpickle                | 14.3 us                                                | 13.7 us: 1.04x faster                                                        |
| mdp                     | 2.82 sec                                               | 2.75 sec: 1.03x faster                                                       |
| regex_dna               | 214 ms                                                 | 211 ms: 1.01x faster                                                         |
| pickle                  | 10.1 us                                                | 10.1 us: 1.01x faster                                                        |
| pidigits                | 190 ms                                                 | 197 ms: 1.04x slower                                                         |
| regex_effbot            | 3.21 ms                                                | 3.38 ms: 1.05x slower                                                        |
| pickle_dict             | 28.3 us                                                | 30.9 us: 1.09x slower                                                        |
| python_startup_no_site  | 5.76 ms                                                | 6.49 ms: 1.13x slower                                                        |
| coverage                | 75.3 ms                                                | 98.1 ms: 1.30x slower                                                        |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                                 |

Benchmark hidden because not significant (2): unpickle_list, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230210-3.12.0a5+-685d559/bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
