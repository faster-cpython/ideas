
# Results vs. 3.10.4

- fork: gvanrossum
- ref: call_family
- machine: linux-x86_64
- commit hash: cd69634
- commit date: 2023-02-08
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 251 ms: 1.32x faster                                              |
| chameleon      | 8.86 ms                                                | 6.44 ms: 1.38x faster                                             |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                            |
| html5lib       | 85.8 ms                                                | 60.7 ms: 1.41x faster                                             |
| tornado_http   | 128 ms                                                 | 94.3 ms: 1.36x faster                                             |
| Geometric mean | (ref)                                                  | 1.35x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 108 ms                                                 | 74.0 ms: 1.46x faster                                             |
| nbody          | 136 ms                                                 | 94.6 ms: 1.44x faster                                             |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                  | 1.28x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 129 ms: 1.35x faster                                              |
| regex_v8       | 25.0 ms                                                | 21.0 ms: 1.19x faster                                             |
| regex_dna      | 214 ms                                                 | 206 ms: 1.04x faster                                              |
| regex_effbot   | 3.21 ms                                                | 3.64 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.10x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 286 us: 1.59x faster                                              |
| unpickle_pure_python | 297 us                                                 | 199 us: 1.49x faster                                              |
| json_dumps           | 13.5 ms                                                | 9.44 ms: 1.43x faster                                             |
| xml_etree_process    | 74.5 ms                                                | 53.2 ms: 1.40x faster                                             |
| json_loads           | 28.9 us                                                | 23.8 us: 1.21x faster                                             |
| xml_etree_generate   | 93.3 ms                                                | 77.1 ms: 1.21x faster                                             |
| xml_etree_parse      | 163 ms                                                 | 146 ms: 1.12x faster                                              |
| pickle_list          | 4.50 us                                                | 4.03 us: 1.12x faster                                             |
| unpickle             | 14.3 us                                                | 13.0 us: 1.10x faster                                             |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                              |
| unpickle_list        | 4.99 us                                                | 4.97 us: 1.01x faster                                             |
| pickle_dict          | 28.3 us                                                | 30.3 us: 1.07x slower                                             |
| Geometric mean       | (ref)                                                  | 1.19x faster                                                      |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.91 ms: 1.56x faster                                             |
| python_startup_no_site | 5.76 ms                                                | 6.47 ms: 1.12x slower                                             |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.5 ms: 1.49x faster                                             |
| mako            | 14.3 ms                                                | 9.97 ms: 1.43x faster                                             |
| django_template | 46.3 ms                                                | 33.2 ms: 1.39x faster                                             |
| genshi_xml      | 63.6 ms                                                | 47.1 ms: 1.35x faster                                             |
| Geometric mean  | (ref)                                                  | 1.42x faster                                                      |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.17 ms: 2.33x faster                                             |
| scimark_sor             | 193 ms                                                 | 105 ms: 1.85x faster                                              |
| logging_silent          | 173 ns                                                 | 96.3 ns: 1.80x faster                                             |
| richards                | 71.4 ms                                                | 42.3 ms: 1.69x faster                                             |
| pyflate                 | 675 ms                                                 | 407 ms: 1.66x faster                                              |
| go                      | 226 ms                                                 | 138 ms: 1.64x faster                                              |
| crypto_pyaes            | 118 ms                                                 | 72.7 ms: 1.62x faster                                             |
| raytrace                | 461 ms                                                 | 288 ms: 1.60x faster                                              |
| scimark_monte_carlo     | 105 ms                                                 | 65.8 ms: 1.59x faster                                             |
| pickle_pure_python      | 453 us                                                 | 286 us: 1.59x faster                                              |
| python_startup          | 13.9 ms                                                | 8.91 ms: 1.56x faster                                             |
| hexiom                  | 9.42 ms                                                | 6.02 ms: 1.56x faster                                             |
| chaos                   | 104 ms                                                 | 66.7 ms: 1.56x faster                                             |
| spectral_norm           | 148 ms                                                 | 96.1 ms: 1.54x faster                                             |
| genshi_text             | 30.6 ms                                                | 20.5 ms: 1.49x faster                                             |
| unpickle_pure_python    | 297 us                                                 | 199 us: 1.49x faster                                              |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.46x faster                                              |
| float                   | 108 ms                                                 | 74.0 ms: 1.46x faster                                             |
| nbody                   | 136 ms                                                 | 94.6 ms: 1.44x faster                                             |
| deepcopy_memo           | 50.0 us                                                | 34.9 us: 1.43x faster                                             |
| mako                    | 14.3 ms                                                | 9.97 ms: 1.43x faster                                             |
| json_dumps              | 13.5 ms                                                | 9.44 ms: 1.43x faster                                             |
| sqlglot_parse           | 2.04 ms                                                | 1.44 ms: 1.41x faster                                             |
| html5lib                | 85.8 ms                                                | 60.7 ms: 1.41x faster                                             |
| xml_etree_process       | 74.5 ms                                                | 53.2 ms: 1.40x faster                                             |
| django_template         | 46.3 ms                                                | 33.2 ms: 1.39x faster                                             |
| thrift                  | 1.03 ms                                                | 740 us: 1.39x faster                                              |
| sqlglot_transpile       | 2.42 ms                                                | 1.74 ms: 1.39x faster                                             |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.39x faster                                            |
| logging_format          | 8.92 us                                                | 6.46 us: 1.38x faster                                             |
| pprint_pformat          | 1.97 sec                                               | 1.43 sec: 1.38x faster                                            |
| chameleon               | 8.86 ms                                                | 6.44 ms: 1.38x faster                                             |
| logging_simple          | 8.06 us                                                | 5.88 us: 1.37x faster                                             |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.01 ms: 1.37x faster                                             |
| tornado_http            | 128 ms                                                 | 94.3 ms: 1.36x faster                                             |
| async_tree_none         | 713 ms                                                 | 524 ms: 1.36x faster                                              |
| scimark_fft             | 414 ms                                                 | 305 ms: 1.36x faster                                              |
| pprint_safe_repr        | 943 ms                                                 | 697 ms: 1.35x faster                                              |
| genshi_xml              | 63.6 ms                                                | 47.1 ms: 1.35x faster                                             |
| regex_compile           | 174 ms                                                 | 129 ms: 1.35x faster                                              |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                            |
| async_tree_memoization  | 854 ms                                                 | 637 ms: 1.34x faster                                              |
| fannkuch                | 477 ms                                                 | 356 ms: 1.34x faster                                              |
| unpack_sequence         | 59.5 ns                                                | 44.4 ns: 1.34x faster                                             |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.33x faster                                             |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                             |
| 2to3                    | 332 ms                                                 | 251 ms: 1.32x faster                                              |
| coroutines              | 31.7 ms                                                | 24.3 ms: 1.30x faster                                             |
| deepcopy                | 429 us                                                 | 332 us: 1.29x faster                                              |
| sqlglot_normalize       | 135 ms                                                 | 106 ms: 1.27x faster                                              |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                            |
| sqlglot_optimize        | 65.3 ms                                                | 51.4 ms: 1.27x faster                                             |
| deepcopy_reduce         | 3.75 us                                                | 2.96 us: 1.27x faster                                             |
| async_tree_cpu_io_mixed | 949 ms                                                 | 752 ms: 1.26x faster                                              |
| nqueens                 | 99.3 ms                                                | 79.2 ms: 1.25x faster                                             |
| async_generators        | 428 ms                                                 | 346 ms: 1.23x faster                                              |
| json_loads              | 28.9 us                                                | 23.8 us: 1.21x faster                                             |
| xml_etree_generate      | 93.3 ms                                                | 77.1 ms: 1.21x faster                                             |
| sympy_integrate         | 23.9 ms                                                | 19.8 ms: 1.21x faster                                             |
| sqlalchemy_declarative  | 165 ms                                                 | 137 ms: 1.20x faster                                              |
| bench_thread_pool       | 943 us                                                 | 783 us: 1.20x faster                                              |
| sympy_str               | 324 ms                                                 | 270 ms: 1.20x faster                                              |
| regex_v8                | 25.0 ms                                                | 21.0 ms: 1.19x faster                                             |
| dulwich_log             | 75.5 ms                                                | 63.4 ms: 1.19x faster                                             |
| sympy_expand            | 537 ms                                                 | 454 ms: 1.18x faster                                              |
| sympy_sum               | 183 ms                                                 | 156 ms: 1.18x faster                                              |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.1 ms: 1.16x faster                                             |
| json                    | 5.35 ms                                                | 4.64 ms: 1.15x faster                                             |
| mdp                     | 2.82 sec                                               | 2.48 sec: 1.14x faster                                            |
| xml_etree_parse         | 163 ms                                                 | 146 ms: 1.12x faster                                              |
| sqlite_synth            | 2.90 us                                                | 2.60 us: 1.12x faster                                             |
| pickle_list             | 4.50 us                                                | 4.03 us: 1.12x faster                                             |
| pathlib                 | 20.0 ms                                                | 18.0 ms: 1.11x faster                                             |
| unpickle                | 14.3 us                                                | 13.0 us: 1.10x faster                                             |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                              |
| meteor_contest          | 114 ms                                                 | 107 ms: 1.07x faster                                              |
| generators              | 75.8 ms                                                | 72.1 ms: 1.05x faster                                             |
| telco                   | 6.68 ms                                                | 6.36 ms: 1.05x faster                                             |
| regex_dna               | 214 ms                                                 | 206 ms: 1.04x faster                                              |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                              |
| unpickle_list           | 4.99 us                                                | 4.97 us: 1.01x faster                                             |
| pickle_dict             | 28.3 us                                                | 30.3 us: 1.07x slower                                             |
| python_startup_no_site  | 5.76 ms                                                | 6.47 ms: 1.12x slower                                             |
| regex_effbot            | 3.21 ms                                                | 3.64 ms: 1.13x slower                                             |
| coverage                | 75.3 ms                                                | 98.8 ms: 1.31x slower                                             |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                      |

Benchmark hidden because not significant (2): bench_mp_pool, pickle
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230208-3.12.0a5+-cd69634/bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
