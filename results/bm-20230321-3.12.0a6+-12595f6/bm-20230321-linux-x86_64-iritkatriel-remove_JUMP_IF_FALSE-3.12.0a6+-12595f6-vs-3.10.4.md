
# Results vs. 3.10.4

- fork: iritkatriel
- ref: remove_JUMP_IF_FALSE
- machine: linux-x86_64
- commit hash: 12595f6
- commit date: 2023-03-21
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.34x faster                                                        |
| chameleon      | 8.86 ms                                                | 6.56 ms: 1.35x faster                                                       |
| docutils       | 3.18 sec                                               | 2.54 sec: 1.25x faster                                                      |
| html5lib       | 85.8 ms                                                | 60.8 ms: 1.41x faster                                                       |
| tornado_http   | 128 ms                                                 | 91.5 ms: 1.40x faster                                                       |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 136 ms                                                 | 87.2 ms: 1.56x faster                                                       |
| float          | 108 ms                                                 | 73.2 ms: 1.47x faster                                                       |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 134 ms: 1.30x faster                                                        |
| regex_v8       | 25.0 ms                                                | 22.0 ms: 1.14x faster                                                       |
| regex_dna      | 214 ms                                                 | 201 ms: 1.06x faster                                                        |
| regex_effbot   | 3.21 ms                                                | 3.59 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 287 us: 1.58x faster                                                        |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.49x faster                                                        |
| json_dumps           | 13.5 ms                                                | 9.51 ms: 1.42x faster                                                       |
| xml_etree_process    | 74.5 ms                                                | 56.8 ms: 1.31x faster                                                       |
| json_loads           | 28.9 us                                                | 24.0 us: 1.20x faster                                                       |
| xml_etree_generate   | 93.3 ms                                                | 81.6 ms: 1.14x faster                                                       |
| pickle_list          | 4.50 us                                                | 4.08 us: 1.10x faster                                                       |
| xml_etree_parse      | 163 ms                                                 | 150 ms: 1.09x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                                        |
| pickle               | 10.1 us                                                | 10.2 us: 1.01x slower                                                       |
| pickle_dict          | 28.3 us                                                | 30.8 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                                |

Benchmark hidden because not significant (2): unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.87 ms: 1.57x faster                                                       |
| python_startup_no_site | 5.76 ms                                                | 6.50 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 14.3 ms                                                | 10.0 ms: 1.42x faster                                                       |
| genshi_text     | 30.6 ms                                                | 21.8 ms: 1.41x faster                                                       |
| django_template | 46.3 ms                                                | 33.2 ms: 1.39x faster                                                       |
| genshi_xml      | 63.6 ms                                                | 46.8 ms: 1.36x faster                                                       |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.2 ms: 2.59x faster                                                       |
| deltablue               | 7.39 ms                                                | 3.18 ms: 2.32x faster                                                       |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.85x faster                                                        |
| logging_silent          | 173 ns                                                 | 98.4 ns: 1.76x faster                                                       |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                                        |
| spectral_norm           | 148 ms                                                 | 88.6 ms: 1.67x faster                                                       |
| pyflate                 | 675 ms                                                 | 407 ms: 1.66x faster                                                        |
| richards                | 71.4 ms                                                | 43.5 ms: 1.64x faster                                                       |
| raytrace                | 461 ms                                                 | 283 ms: 1.63x faster                                                        |
| crypto_pyaes            | 118 ms                                                 | 73.4 ms: 1.60x faster                                                       |
| scimark_monte_carlo     | 105 ms                                                 | 66.2 ms: 1.58x faster                                                       |
| pickle_pure_python      | 453 us                                                 | 287 us: 1.58x faster                                                        |
| python_startup          | 13.9 ms                                                | 8.87 ms: 1.57x faster                                                       |
| chaos                   | 104 ms                                                 | 66.6 ms: 1.56x faster                                                       |
| nbody                   | 136 ms                                                 | 87.2 ms: 1.56x faster                                                       |
| hexiom                  | 9.42 ms                                                | 6.11 ms: 1.54x faster                                                       |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.49x faster                                                        |
| float                   | 108 ms                                                 | 73.2 ms: 1.47x faster                                                       |
| scimark_lu              | 158 ms                                                 | 109 ms: 1.46x faster                                                        |
| deepcopy_memo           | 50.0 us                                                | 34.6 us: 1.44x faster                                                       |
| coroutines              | 31.7 ms                                                | 22.0 ms: 1.44x faster                                                       |
| mako                    | 14.3 ms                                                | 10.0 ms: 1.42x faster                                                       |
| json_dumps              | 13.5 ms                                                | 9.51 ms: 1.42x faster                                                       |
| logging_format          | 8.92 us                                                | 6.32 us: 1.41x faster                                                       |
| html5lib                | 85.8 ms                                                | 60.8 ms: 1.41x faster                                                       |
| genshi_text             | 30.6 ms                                                | 21.8 ms: 1.41x faster                                                       |
| sqlglot_parse           | 2.04 ms                                                | 1.45 ms: 1.40x faster                                                       |
| tornado_http            | 128 ms                                                 | 91.5 ms: 1.40x faster                                                       |
| logging_simple          | 8.06 us                                                | 5.78 us: 1.39x faster                                                       |
| django_template         | 46.3 ms                                                | 33.2 ms: 1.39x faster                                                       |
| sqlglot_transpile       | 2.42 ms                                                | 1.74 ms: 1.39x faster                                                       |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.36x faster                                                      |
| pprint_pformat          | 1.97 sec                                               | 1.45 sec: 1.36x faster                                                      |
| genshi_xml              | 63.6 ms                                                | 46.8 ms: 1.36x faster                                                       |
| async_tree_none         | 713 ms                                                 | 527 ms: 1.35x faster                                                        |
| chameleon               | 8.86 ms                                                | 6.56 ms: 1.35x faster                                                       |
| unpack_sequence         | 59.5 ns                                                | 44.2 ns: 1.35x faster                                                       |
| pycparser               | 1.51 sec                                               | 1.13 sec: 1.34x faster                                                      |
| scimark_fft             | 414 ms                                                 | 309 ms: 1.34x faster                                                        |
| 2to3                    | 332 ms                                                 | 249 ms: 1.34x faster                                                        |
| thrift                  | 1.03 ms                                                | 773 us: 1.33x faster                                                        |
| pprint_safe_repr        | 943 ms                                                 | 711 ms: 1.33x faster                                                        |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.32x faster                                                       |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.32x faster                                                       |
| xml_etree_process       | 74.5 ms                                                | 56.8 ms: 1.31x faster                                                       |
| regex_compile           | 174 ms                                                 | 134 ms: 1.30x faster                                                        |
| deepcopy                | 429 us                                                 | 330 us: 1.30x faster                                                        |
| fannkuch                | 477 ms                                                 | 371 ms: 1.29x faster                                                        |
| async_tree_memoization  | 854 ms                                                 | 666 ms: 1.28x faster                                                        |
| sqlglot_normalize       | 135 ms                                                 | 106 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed | 949 ms                                                 | 746 ms: 1.27x faster                                                        |
| sqlglot_optimize        | 65.3 ms                                                | 51.5 ms: 1.27x faster                                                       |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.32 ms: 1.27x faster                                                       |
| deepcopy_reduce         | 3.75 us                                                | 2.98 us: 1.26x faster                                                       |
| docutils                | 3.18 sec                                               | 2.54 sec: 1.25x faster                                                      |
| nqueens                 | 99.3 ms                                                | 80.8 ms: 1.23x faster                                                       |
| sqlalchemy_declarative  | 165 ms                                                 | 136 ms: 1.21x faster                                                        |
| json_loads              | 28.9 us                                                | 24.0 us: 1.20x faster                                                       |
| bench_thread_pool       | 943 us                                                 | 788 us: 1.20x faster                                                        |
| dulwich_log             | 75.5 ms                                                | 63.3 ms: 1.19x faster                                                       |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.9 ms: 1.17x faster                                                       |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                                       |
| sympy_expand            | 537 ms                                                 | 459 ms: 1.17x faster                                                        |
| mdp                     | 2.82 sec                                               | 2.43 sec: 1.16x faster                                                      |
| json                    | 5.35 ms                                                | 4.61 ms: 1.16x faster                                                       |
| sympy_str               | 324 ms                                                 | 283 ms: 1.15x faster                                                        |
| xml_etree_generate      | 93.3 ms                                                | 81.6 ms: 1.14x faster                                                       |
| regex_v8                | 25.0 ms                                                | 22.0 ms: 1.14x faster                                                       |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                                       |
| sqlite_synth            | 2.90 us                                                | 2.61 us: 1.11x faster                                                       |
| sympy_sum               | 183 ms                                                 | 166 ms: 1.11x faster                                                        |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                                        |
| pickle_list             | 4.50 us                                                | 4.08 us: 1.10x faster                                                       |
| xml_etree_parse         | 163 ms                                                 | 150 ms: 1.09x faster                                                        |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                                        |
| regex_dna               | 214 ms                                                 | 201 ms: 1.06x faster                                                        |
| async_generators        | 428 ms                                                 | 411 ms: 1.04x faster                                                        |
| telco                   | 6.68 ms                                                | 6.51 ms: 1.03x faster                                                       |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                                        |
| pickle                  | 10.1 us                                                | 10.2 us: 1.01x slower                                                       |
| pickle_dict             | 28.3 us                                                | 30.8 us: 1.09x slower                                                       |
| regex_effbot            | 3.21 ms                                                | 3.59 ms: 1.12x slower                                                       |
| python_startup_no_site  | 5.76 ms                                                | 6.50 ms: 1.13x slower                                                       |
| coverage                | 75.3 ms                                                | 94.9 ms: 1.26x slower                                                       |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                                |

Benchmark hidden because not significant (3): unpickle, bench_mp_pool, unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230321-3.12.0a6+-12595f6/bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
