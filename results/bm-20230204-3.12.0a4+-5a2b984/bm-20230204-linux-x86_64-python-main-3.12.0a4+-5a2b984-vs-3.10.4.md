
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a2b984
- commit date: 2023-02-04
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 253 ms: 1.31x faster                                   |
| chameleon      | 8.86 ms                                                | 6.29 ms: 1.41x faster                                  |
| docutils       | 3.18 sec                                               | 2.51 sec: 1.27x faster                                 |
| html5lib       | 85.8 ms                                                | 60.0 ms: 1.43x faster                                  |
| tornado_http   | 128 ms                                                 | 94.1 ms: 1.36x faster                                  |
| Geometric mean | (ref)                                                  | 1.36x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.8 ms: 1.48x faster                                  |
| nbody          | 136 ms                                                 | 93.8 ms: 1.45x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_v8       | 25.0 ms                                                | 22.4 ms: 1.11x faster                                  |
| regex_dna      | 214 ms                                                 | 216 ms: 1.01x slower                                   |
| regex_effbot   | 3.21 ms                                                | 3.64 ms: 1.14x slower                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 283 us: 1.60x faster                                   |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.50x faster                                   |
| json_dumps           | 13.5 ms                                                | 9.26 ms: 1.46x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.2 ms: 1.40x faster                                  |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 77.3 ms: 1.21x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 146 ms: 1.12x faster                                   |
| pickle_list          | 4.50 us                                                | 4.05 us: 1.11x faster                                  |
| unpickle             | 14.3 us                                                | 13.0 us: 1.10x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.09x faster                                   |
| unpickle_list        | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| pickle_dict          | 28.3 us                                                | 30.8 us: 1.09x slower                                  |
| Geometric mean       | (ref)                                                  | 1.19x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.93 ms: 1.56x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.46 ms: 1.12x slower                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.6 ms: 1.49x faster                                  |
| mako            | 14.3 ms                                                | 9.70 ms: 1.47x faster                                  |
| django_template | 46.3 ms                                                | 32.8 ms: 1.41x faster                                  |
| genshi_xml      | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.22 ms: 2.29x faster                                  |
| logging_silent          | 173 ns                                                 | 92.8 ns: 1.87x faster                                  |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.80x faster                                   |
| go                      | 226 ms                                                 | 136 ms: 1.67x faster                                   |
| pyflate                 | 675 ms                                                 | 405 ms: 1.67x faster                                   |
| richards                | 71.4 ms                                                | 43.2 ms: 1.65x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 72.3 ms: 1.63x faster                                  |
| spectral_norm           | 148 ms                                                 | 91.5 ms: 1.62x faster                                  |
| chaos                   | 104 ms                                                 | 64.7 ms: 1.61x faster                                  |
| pickle_pure_python      | 453 us                                                 | 283 us: 1.60x faster                                   |
| raytrace                | 461 ms                                                 | 288 ms: 1.60x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 66.8 ms: 1.57x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.01 ms: 1.57x faster                                  |
| python_startup          | 13.9 ms                                                | 8.93 ms: 1.56x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.50x faster                                   |
| genshi_text             | 30.6 ms                                                | 20.6 ms: 1.49x faster                                  |
| float                   | 108 ms                                                 | 72.8 ms: 1.48x faster                                  |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.47x faster                                   |
| mako                    | 14.3 ms                                                | 9.70 ms: 1.47x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.1 us: 1.47x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.26 ms: 1.46x faster                                  |
| nbody                   | 136 ms                                                 | 93.8 ms: 1.45x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                 |
| sqlglot_parse           | 2.04 ms                                                | 1.42 ms: 1.43x faster                                  |
| html5lib                | 85.8 ms                                                | 60.0 ms: 1.43x faster                                  |
| logging_format          | 8.92 us                                                | 6.28 us: 1.42x faster                                  |
| logging_simple          | 8.06 us                                                | 5.70 us: 1.41x faster                                  |
| pprint_safe_repr        | 943 ms                                                 | 668 ms: 1.41x faster                                   |
| sqlglot_transpile       | 2.42 ms                                                | 1.71 ms: 1.41x faster                                  |
| django_template         | 46.3 ms                                                | 32.8 ms: 1.41x faster                                  |
| chameleon               | 8.86 ms                                                | 6.29 ms: 1.41x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.2 ms: 1.40x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 42.7 ns: 1.39x faster                                  |
| scimark_fft             | 414 ms                                                 | 299 ms: 1.38x faster                                   |
| thrift                  | 1.03 ms                                                | 747 us: 1.38x faster                                   |
| tornado_http            | 128 ms                                                 | 94.1 ms: 1.36x faster                                  |
| async_tree_none         | 713 ms                                                 | 524 ms: 1.36x faster                                   |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| genshi_xml              | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                 |
| aiohttp                 | 1.34 ms                                                | 999 us: 1.34x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                  |
| pycparser               | 1.51 sec                                               | 1.14 sec: 1.32x faster                                 |
| 2to3                    | 332 ms                                                 | 253 ms: 1.31x faster                                   |
| deepcopy                | 429 us                                                 | 327 us: 1.31x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.20 ms: 1.31x faster                                  |
| async_tree_memoization  | 854 ms                                                 | 655 ms: 1.30x faster                                   |
| fannkuch                | 477 ms                                                 | 368 ms: 1.30x faster                                   |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.29x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                | 50.7 ms: 1.29x faster                                  |
| coroutines              | 31.7 ms                                                | 24.9 ms: 1.27x faster                                  |
| docutils                | 3.18 sec                                               | 2.51 sec: 1.27x faster                                 |
| deepcopy_reduce         | 3.75 us                                                | 2.97 us: 1.26x faster                                  |
| nqueens                 | 99.3 ms                                                | 78.8 ms: 1.26x faster                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 755 ms: 1.26x faster                                   |
| mypy                    | 1.01 sec                                               | 808 ms: 1.26x faster                                   |
| async_generators        | 428 ms                                                 | 349 ms: 1.22x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 19.8 ms: 1.21x faster                                  |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 77.3 ms: 1.21x faster                                  |
| bench_thread_pool       | 943 us                                                 | 785 us: 1.20x faster                                   |
| dulwich_log             | 75.5 ms                                                | 63.2 ms: 1.19x faster                                  |
| sympy_str               | 324 ms                                                 | 272 ms: 1.19x faster                                   |
| sympy_sum               | 183 ms                                                 | 156 ms: 1.18x faster                                   |
| sympy_expand            | 537 ms                                                 | 457 ms: 1.17x faster                                   |
| json                    | 5.35 ms                                                | 4.57 ms: 1.17x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 146 ms: 1.12x faster                                   |
| mdp                     | 2.82 sec                                               | 2.53 sec: 1.11x faster                                 |
| regex_v8                | 25.0 ms                                                | 22.4 ms: 1.11x faster                                  |
| pickle_list             | 4.50 us                                                | 4.05 us: 1.11x faster                                  |
| unpickle                | 14.3 us                                                | 13.0 us: 1.10x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.09x faster                                   |
| meteor_contest          | 114 ms                                                 | 107 ms: 1.06x faster                                   |
| telco                   | 6.68 ms                                                | 6.35 ms: 1.05x faster                                  |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                   |
| unpickle_list           | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| regex_dna               | 214 ms                                                 | 216 ms: 1.01x slower                                   |
| generators              | 75.8 ms                                                | 76.8 ms: 1.01x slower                                  |
| pickle_dict             | 28.3 us                                                | 30.8 us: 1.09x slower                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.46 ms: 1.12x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.64 ms: 1.14x slower                                  |
| coverage                | 75.3 ms                                                | 96.2 ms: 1.28x slower                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (2): bench_mp_pool, pickle
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230204-3.12.0a4+-5a2b984/bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
