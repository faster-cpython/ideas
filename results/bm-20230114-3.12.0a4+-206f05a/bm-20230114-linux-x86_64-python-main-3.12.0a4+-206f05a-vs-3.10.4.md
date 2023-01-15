
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 206f05a
- commit date: 2023-01-14
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| chameleon      | 8.86 ms                                                | 6.35 ms: 1.40x faster                                  |
| docutils       | 3.18 sec                                               | 2.48 sec: 1.28x faster                                 |
| html5lib       | 85.8 ms                                                | 59.2 ms: 1.45x faster                                  |
| tornado_http   | 128 ms                                                 | 93.4 ms: 1.37x faster                                  |
| Geometric mean | (ref)                                                  | 1.36x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.2 ms: 1.49x faster                                  |
| nbody          | 136 ms                                                 | 95.1 ms: 1.43x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_dna      | 214 ms                                                 | 201 ms: 1.07x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.39 ms: 1.06x slower                                  |
| regex_v8       | 25.0 ms                                                | 21.2 ms: 1.18x faster                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.40 ms: 1.43x faster                                  |
| json_loads           | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.2 us: 1.01x slower                                  |
| pickle_dict          | 28.3 us                                                | 30.5 us: 1.08x slower                                  |
| pickle_list          | 4.50 us                                                | 4.08 us: 1.10x faster                                  |
| pickle_pure_python   | 453 us                                                 | 281 us: 1.61x faster                                   |
| unpickle             | 14.3 us                                                | 13.1 us: 1.09x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.97 us: 1.00x faster                                  |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 149 ms: 1.10x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 107 ms: 1.03x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.6 ms: 1.22x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.5 ms: 1.39x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.95 ms: 1.56x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.49 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.0 ms: 1.45x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.2 ms: 1.51x faster                                  |
| genshi_xml      | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| mako            | 14.3 ms                                                | 9.90 ms: 1.44x faster                                  |
| Geometric mean  | (ref)                                                  | 1.44x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| aiohttp                 | 1.34 ms                                                | 998 us: 1.34x faster                                   |
| async_generators        | 428 ms                                                 | 358 ms: 1.19x faster                                   |
| async_tree_none         | 713 ms                                                 | 524 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 732 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 627 ms: 1.36x faster                                   |
| chameleon               | 8.86 ms                                                | 6.35 ms: 1.40x faster                                  |
| chaos                   | 104 ms                                                 | 67.9 ms: 1.53x faster                                  |
| bench_thread_pool       | 943 us                                                 | 779 us: 1.21x faster                                   |
| coroutines              | 31.7 ms                                                | 25.2 ms: 1.26x faster                                  |
| coverage                | 75.3 ms                                                | 98.6 ms: 1.31x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 74.3 ms: 1.58x faster                                  |
| deepcopy                | 429 us                                                 | 331 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.28x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 33.7 us: 1.48x faster                                  |
| deltablue               | 7.39 ms                                                | 3.23 ms: 2.29x faster                                  |
| django_template         | 46.3 ms                                                | 32.0 ms: 1.45x faster                                  |
| docutils                | 3.18 sec                                               | 2.48 sec: 1.28x faster                                 |
| dulwich_log             | 75.5 ms                                                | 61.9 ms: 1.22x faster                                  |
| fannkuch                | 477 ms                                                 | 371 ms: 1.28x faster                                   |
| float                   | 108 ms                                                 | 72.2 ms: 1.49x faster                                  |
| generators              | 75.8 ms                                                | 78.8 ms: 1.04x slower                                  |
| genshi_text             | 30.6 ms                                                | 20.2 ms: 1.51x faster                                  |
| genshi_xml              | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| go                      | 226 ms                                                 | 132 ms: 1.72x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.07 ms: 1.55x faster                                  |
| html5lib                | 85.8 ms                                                | 59.2 ms: 1.45x faster                                  |
| json                    | 5.35 ms                                                | 4.68 ms: 1.14x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.40 ms: 1.43x faster                                  |
| json_loads              | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.20 us: 1.44x faster                                  |
| logging_silent          | 173 ns                                                 | 90.6 ns: 1.91x faster                                  |
| logging_simple          | 8.06 us                                                | 5.61 us: 1.43x faster                                  |
| mako                    | 14.3 ms                                                | 9.90 ms: 1.44x faster                                  |
| mdp                     | 2.82 sec                                               | 2.69 sec: 1.05x faster                                 |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.09x faster                                   |
| mypy                    | 1.01 sec                                               | 811 ms: 1.25x faster                                   |
| nbody                   | 136 ms                                                 | 95.1 ms: 1.43x faster                                  |
| nqueens                 | 99.3 ms                                                | 80.8 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.2 us: 1.01x slower                                  |
| pickle_dict             | 28.3 us                                                | 30.5 us: 1.08x slower                                  |
| pickle_list             | 4.50 us                                                | 4.08 us: 1.10x faster                                  |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.61x faster                                   |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 670 ms: 1.41x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.38 sec: 1.43x faster                                 |
| pycparser               | 1.51 sec                                               | 1.08 sec: 1.39x faster                                 |
| pyflate                 | 675 ms                                                 | 398 ms: 1.70x faster                                   |
| python_startup          | 13.9 ms                                                | 8.95 ms: 1.56x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.49 ms: 1.13x slower                                  |
| raytrace                | 461 ms                                                 | 278 ms: 1.66x faster                                   |
| regex_compile           | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_dna               | 214 ms                                                 | 201 ms: 1.07x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.39 ms: 1.06x slower                                  |
| regex_v8                | 25.0 ms                                                | 21.2 ms: 1.18x faster                                  |
| richards                | 71.4 ms                                                | 41.1 ms: 1.74x faster                                  |
| scimark_fft             | 414 ms                                                 | 306 ms: 1.35x faster                                   |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.49x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 63.8 ms: 1.64x faster                                  |
| scimark_sor             | 193 ms                                                 | 106 ms: 1.82x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.05 ms: 1.35x faster                                  |
| spectral_norm           | 148 ms                                                 | 93.9 ms: 1.58x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.39 ms: 1.47x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.67 ms: 1.44x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.5 ms: 1.29x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 459 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                  |
| sympy_sum               | 183 ms                                                 | 164 ms: 1.12x faster                                   |
| sympy_str               | 324 ms                                                 | 283 ms: 1.14x faster                                   |
| telco                   | 6.68 ms                                                | 6.24 ms: 1.07x faster                                  |
| thrift                  | 1.03 ms                                                | 749 us: 1.38x faster                                   |
| tornado_http            | 128 ms                                                 | 93.4 ms: 1.37x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 41.3 ns: 1.44x faster                                  |
| unpickle                | 14.3 us                                                | 13.1 us: 1.09x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.97 us: 1.00x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 149 ms: 1.10x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 107 ms: 1.03x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.6 ms: 1.22x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.5 ms: 1.39x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230114-3.12.0a4+-206f05a/bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
