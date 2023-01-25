
# Results vs. 3.10.4

- fork: brandtbucher
- ref: load_attr_class_from
- machine: linux-x86_64
- commit hash: 8b346a3
- commit date: 2023-01-16
- overall geometric mean: 1.31x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                                         |
| chameleon      | 8.86 ms                                                | 6.33 ms: 1.40x faster                                                        |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                                       |
| html5lib       | 85.8 ms                                                | 60.1 ms: 1.43x faster                                                        |
| tornado_http   | 128 ms                                                 | 94.4 ms: 1.36x faster                                                        |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 71.8 ms: 1.50x faster                                                        |
| nbody          | 136 ms                                                 | 93.6 ms: 1.46x faster                                                        |
| pidigits       | 190 ms                                                 | 193 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                  | 1.29x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                                         |
| regex_dna      | 214 ms                                                 | 210 ms: 1.02x faster                                                         |
| regex_effbot   | 3.21 ms                                                | 3.47 ms: 1.08x slower                                                        |
| regex_v8       | 25.0 ms                                                | 22.4 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.28 ms: 1.45x faster                                                        |
| json_loads           | 28.9 us                                                | 24.0 us: 1.20x faster                                                        |
| pickle_dict          | 28.3 us                                                | 30.5 us: 1.08x slower                                                        |
| pickle_list          | 4.50 us                                                | 4.10 us: 1.10x faster                                                        |
| pickle_pure_python   | 453 us                                                 | 272 us: 1.66x faster                                                         |
| unpickle             | 14.3 us                                                | 13.3 us: 1.07x faster                                                        |
| unpickle_list        | 4.99 us                                                | 5.03 us: 1.01x slower                                                        |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.51x faster                                                         |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                                         |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                                         |
| xml_etree_generate   | 93.3 ms                                                | 78.4 ms: 1.19x faster                                                        |
| xml_etree_process    | 74.5 ms                                                | 54.1 ms: 1.38x faster                                                        |
| Geometric mean       | (ref)                                                  | 1.19x faster                                                                 |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.93 ms: 1.56x faster                                                        |
| python_startup_no_site | 5.76 ms                                                | 6.46 ms: 1.12x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.3 ms: 1.43x faster                                                        |
| genshi_text     | 30.6 ms                                                | 20.5 ms: 1.50x faster                                                        |
| genshi_xml      | 63.6 ms                                                | 47.1 ms: 1.35x faster                                                        |
| mako            | 14.3 ms                                                | 9.58 ms: 1.49x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.44x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                                         |
| aiohttp                 | 1.34 ms                                                | 994 us: 1.35x faster                                                         |
| async_generators        | 428 ms                                                 | 349 ms: 1.22x faster                                                         |
| async_tree_none         | 713 ms                                                 | 524 ms: 1.36x faster                                                         |
| async_tree_cpu_io_mixed | 949 ms                                                 | 756 ms: 1.25x faster                                                         |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                                       |
| async_tree_memoization  | 854 ms                                                 | 629 ms: 1.36x faster                                                         |
| chameleon               | 8.86 ms                                                | 6.33 ms: 1.40x faster                                                        |
| chaos                   | 104 ms                                                 | 64.8 ms: 1.61x faster                                                        |
| bench_thread_pool       | 943 us                                                 | 774 us: 1.22x faster                                                         |
| coroutines              | 31.7 ms                                                | 25.3 ms: 1.25x faster                                                        |
| coverage                | 75.3 ms                                                | 96.0 ms: 1.27x slower                                                        |
| crypto_pyaes            | 118 ms                                                 | 67.2 ms: 1.75x faster                                                        |
| deepcopy                | 429 us                                                 | 326 us: 1.32x faster                                                         |
| deepcopy_reduce         | 3.75 us                                                | 2.95 us: 1.27x faster                                                        |
| deepcopy_memo           | 50.0 us                                                | 34.0 us: 1.47x faster                                                        |
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.30x faster                                                        |
| django_template         | 46.3 ms                                                | 32.3 ms: 1.43x faster                                                        |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                                       |
| dulwich_log             | 75.5 ms                                                | 62.5 ms: 1.21x faster                                                        |
| fannkuch                | 477 ms                                                 | 371 ms: 1.29x faster                                                         |
| float                   | 108 ms                                                 | 71.8 ms: 1.50x faster                                                        |
| generators              | 75.8 ms                                                | 77.2 ms: 1.02x slower                                                        |
| genshi_text             | 30.6 ms                                                | 20.5 ms: 1.50x faster                                                        |
| genshi_xml              | 63.6 ms                                                | 47.1 ms: 1.35x faster                                                        |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                                         |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                                        |
| hexiom                  | 9.42 ms                                                | 5.98 ms: 1.58x faster                                                        |
| html5lib                | 85.8 ms                                                | 60.1 ms: 1.43x faster                                                        |
| json                    | 5.35 ms                                                | 4.57 ms: 1.17x faster                                                        |
| json_dumps              | 13.5 ms                                                | 9.28 ms: 1.45x faster                                                        |
| json_loads              | 28.9 us                                                | 24.0 us: 1.20x faster                                                        |
| logging_format          | 8.92 us                                                | 6.31 us: 1.41x faster                                                        |
| logging_silent          | 173 ns                                                 | 93.6 ns: 1.85x faster                                                        |
| logging_simple          | 8.06 us                                                | 5.69 us: 1.42x faster                                                        |
| mako                    | 14.3 ms                                                | 9.58 ms: 1.49x faster                                                        |
| mdp                     | 2.82 sec                                               | 2.46 sec: 1.15x faster                                                       |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.08x faster                                                         |
| mypy                    | 1.01 sec                                               | 806 ms: 1.26x faster                                                         |
| nbody                   | 136 ms                                                 | 93.6 ms: 1.46x faster                                                        |
| nqueens                 | 99.3 ms                                                | 78.0 ms: 1.27x faster                                                        |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                                        |
| pickle_dict             | 28.3 us                                                | 30.5 us: 1.08x slower                                                        |
| pickle_list             | 4.50 us                                                | 4.10 us: 1.10x faster                                                        |
| pickle_pure_python      | 453 us                                                 | 272 us: 1.66x faster                                                         |
| pidigits                | 190 ms                                                 | 193 ms: 1.01x slower                                                         |
| pprint_safe_repr        | 943 ms                                                 | 679 ms: 1.39x faster                                                         |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                                       |
| pycparser               | 1.51 sec                                               | 1.14 sec: 1.32x faster                                                       |
| pyflate                 | 675 ms                                                 | 403 ms: 1.67x faster                                                         |
| python_startup          | 13.9 ms                                                | 8.93 ms: 1.56x faster                                                        |
| python_startup_no_site  | 5.76 ms                                                | 6.46 ms: 1.12x slower                                                        |
| raytrace                | 461 ms                                                 | 283 ms: 1.63x faster                                                         |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                                         |
| regex_dna               | 214 ms                                                 | 210 ms: 1.02x faster                                                         |
| regex_effbot            | 3.21 ms                                                | 3.47 ms: 1.08x slower                                                        |
| regex_v8                | 25.0 ms                                                | 22.4 ms: 1.11x faster                                                        |
| richards                | 71.4 ms                                                | 42.3 ms: 1.69x faster                                                        |
| scimark_fft             | 414 ms                                                 | 300 ms: 1.38x faster                                                         |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.50x faster                                                         |
| scimark_monte_carlo     | 105 ms                                                 | 62.1 ms: 1.69x faster                                                        |
| scimark_sor             | 193 ms                                                 | 105 ms: 1.84x faster                                                         |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.97 ms: 1.38x faster                                                        |
| spectral_norm           | 148 ms                                                 | 95.9 ms: 1.54x faster                                                        |
| sqlglot_parse           | 2.04 ms                                                | 1.42 ms: 1.44x faster                                                        |
| sqlglot_transpile       | 2.42 ms                                                | 1.70 ms: 1.42x faster                                                        |
| sqlglot_optimize        | 65.3 ms                                                | 50.9 ms: 1.28x faster                                                        |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                                         |
| sqlite_synth            | 2.90 us                                                | 2.57 us: 1.13x faster                                                        |
| sympy_expand            | 537 ms                                                 | 456 ms: 1.18x faster                                                         |
| sympy_integrate         | 23.9 ms                                                | 19.8 ms: 1.21x faster                                                        |
| sympy_sum               | 183 ms                                                 | 156 ms: 1.18x faster                                                         |
| sympy_str               | 324 ms                                                 | 269 ms: 1.20x faster                                                         |
| telco                   | 6.68 ms                                                | 6.50 ms: 1.03x faster                                                        |
| thrift                  | 1.03 ms                                                | 745 us: 1.38x faster                                                         |
| tornado_http            | 128 ms                                                 | 94.4 ms: 1.36x faster                                                        |
| unpack_sequence         | 59.5 ns                                                | 41.6 ns: 1.43x faster                                                        |
| unpickle                | 14.3 us                                                | 13.3 us: 1.07x faster                                                        |
| unpickle_list           | 4.99 us                                                | 5.03 us: 1.01x slower                                                        |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.51x faster                                                         |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                                         |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                                         |
| xml_etree_generate      | 93.3 ms                                                | 78.4 ms: 1.19x faster                                                        |
| xml_etree_process       | 74.5 ms                                                | 54.1 ms: 1.38x faster                                                        |
| Geometric mean          | (ref)                                                  | 1.31x faster                                                                 |

Benchmark hidden because not significant (2): bench_mp_pool, pickle
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230116-3.12.0a4+-8b346a3/bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
