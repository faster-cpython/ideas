
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c1c5882
- commit date: 2023-01-21
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 254 ms: 1.31x faster                                   |
| chameleon      | 8.86 ms                                                | 6.32 ms: 1.40x faster                                  |
| docutils       | 3.18 sec                                               | 2.51 sec: 1.27x faster                                 |
| html5lib       | 85.8 ms                                                | 60.8 ms: 1.41x faster                                  |
| tornado_http   | 128 ms                                                 | 93.9 ms: 1.37x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.0 ms: 1.50x faster                                  |
| nbody          | 136 ms                                                 | 92.7 ms: 1.47x faster                                  |
| pidigits       | 190 ms                                                 | 193 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna      | 214 ms                                                 | 210 ms: 1.02x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.65 ms: 1.14x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.5 ms: 1.11x faster                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.39 ms: 1.44x faster                                  |
| json_loads           | 28.9 us                                                | 24.1 us: 1.20x faster                                  |
| pickle               | 10.1 us                                                | 10.0 us: 1.01x faster                                  |
| pickle_dict          | 28.3 us                                                | 30.3 us: 1.07x slower                                  |
| pickle_list          | 4.50 us                                                | 4.01 us: 1.12x faster                                  |
| pickle_pure_python   | 453 us                                                 | 283 us: 1.60x faster                                   |
| unpickle             | 14.3 us                                                | 13.6 us: 1.05x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 159 ms: 1.03x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 106 ms: 1.04x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 78.1 ms: 1.19x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 54.1 ms: 1.38x faster                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.95 ms: 1.56x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.49 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.3 ms: 1.43x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.1 ms: 1.45x faster                                  |
| genshi_xml      | 63.6 ms                                                | 47.3 ms: 1.34x faster                                  |
| mako            | 14.3 ms                                                | 9.90 ms: 1.44x faster                                  |
| Geometric mean  | (ref)                                                  | 1.42x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 254 ms: 1.31x faster                                   |
| aiohttp                 | 1.34 ms                                                | 996 us: 1.34x faster                                   |
| async_generators        | 428 ms                                                 | 347 ms: 1.23x faster                                   |
| async_tree_none         | 713 ms                                                 | 527 ms: 1.35x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 755 ms: 1.26x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 645 ms: 1.32x faster                                   |
| chameleon               | 8.86 ms                                                | 6.32 ms: 1.40x faster                                  |
| chaos                   | 104 ms                                                 | 62.4 ms: 1.67x faster                                  |
| bench_thread_pool       | 943 us                                                 | 781 us: 1.21x faster                                   |
| coroutines              | 31.7 ms                                                | 24.6 ms: 1.29x faster                                  |
| coverage                | 75.3 ms                                                | 96.0 ms: 1.27x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 72.8 ms: 1.61x faster                                  |
| deepcopy                | 429 us                                                 | 325 us: 1.32x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.91 us: 1.29x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 33.9 us: 1.47x faster                                  |
| deltablue               | 7.39 ms                                                | 3.19 ms: 2.32x faster                                  |
| django_template         | 46.3 ms                                                | 32.3 ms: 1.43x faster                                  |
| docutils                | 3.18 sec                                               | 2.51 sec: 1.27x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.5 ms: 1.21x faster                                  |
| fannkuch                | 477 ms                                                 | 364 ms: 1.31x faster                                   |
| float                   | 108 ms                                                 | 72.0 ms: 1.50x faster                                  |
| generators              | 75.8 ms                                                | 76.6 ms: 1.01x slower                                  |
| genshi_text             | 30.6 ms                                                | 21.1 ms: 1.45x faster                                  |
| genshi_xml              | 63.6 ms                                                | 47.3 ms: 1.34x faster                                  |
| go                      | 226 ms                                                 | 136 ms: 1.67x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.33x faster                                  |
| hexiom                  | 9.42 ms                                                | 5.88 ms: 1.60x faster                                  |
| html5lib                | 85.8 ms                                                | 60.8 ms: 1.41x faster                                  |
| json                    | 5.35 ms                                                | 4.73 ms: 1.13x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.39 ms: 1.44x faster                                  |
| json_loads              | 28.9 us                                                | 24.1 us: 1.20x faster                                  |
| logging_format          | 8.92 us                                                | 6.34 us: 1.41x faster                                  |
| logging_silent          | 173 ns                                                 | 92.0 ns: 1.88x faster                                  |
| logging_simple          | 8.06 us                                                | 5.84 us: 1.38x faster                                  |
| mako                    | 14.3 ms                                                | 9.90 ms: 1.44x faster                                  |
| mdp                     | 2.82 sec                                               | 2.46 sec: 1.15x faster                                 |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.08x faster                                   |
| mypy                    | 1.01 sec                                               | 809 ms: 1.25x faster                                   |
| nbody                   | 136 ms                                                 | 92.7 ms: 1.47x faster                                  |
| nqueens                 | 99.3 ms                                                | 76.0 ms: 1.31x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                  |
| pickle                  | 10.1 us                                                | 10.0 us: 1.01x faster                                  |
| pickle_dict             | 28.3 us                                                | 30.3 us: 1.07x slower                                  |
| pickle_list             | 4.50 us                                                | 4.01 us: 1.12x faster                                  |
| pickle_pure_python      | 453 us                                                 | 283 us: 1.60x faster                                   |
| pidigits                | 190 ms                                                 | 193 ms: 1.01x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 665 ms: 1.42x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.38 sec: 1.43x faster                                 |
| pycparser               | 1.51 sec                                               | 1.15 sec: 1.32x faster                                 |
| pyflate                 | 675 ms                                                 | 398 ms: 1.70x faster                                   |
| python_startup          | 13.9 ms                                                | 8.95 ms: 1.56x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.49 ms: 1.13x slower                                  |
| raytrace                | 461 ms                                                 | 283 ms: 1.63x faster                                   |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna               | 214 ms                                                 | 210 ms: 1.02x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.65 ms: 1.14x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.5 ms: 1.11x faster                                  |
| richards                | 71.4 ms                                                | 42.9 ms: 1.67x faster                                  |
| scimark_fft             | 414 ms                                                 | 302 ms: 1.37x faster                                   |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.49x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.5 ms: 1.62x faster                                  |
| scimark_sor             | 193 ms                                                 | 105 ms: 1.84x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.97 ms: 1.38x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.8 ms: 1.55x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.40 ms: 1.45x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.70 ms: 1.42x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.6 ms: 1.29x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.56 us: 1.14x faster                                  |
| sympy_expand            | 537 ms                                                 | 452 ms: 1.19x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.2 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 163 ms: 1.13x faster                                   |
| sympy_str               | 324 ms                                                 | 281 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.39 ms: 1.05x faster                                  |
| thrift                  | 1.03 ms                                                | 744 us: 1.39x faster                                   |
| tornado_http            | 128 ms                                                 | 93.9 ms: 1.37x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 41.7 ns: 1.42x faster                                  |
| unpickle                | 14.3 us                                                | 13.6 us: 1.05x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 159 ms: 1.03x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 106 ms: 1.04x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 78.1 ms: 1.19x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 54.1 ms: 1.38x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230121-3.12.0a4+-c1c5882/bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
