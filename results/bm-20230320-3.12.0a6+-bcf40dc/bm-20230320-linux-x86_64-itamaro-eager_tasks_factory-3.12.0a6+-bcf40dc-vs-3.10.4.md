
# Results vs. 3.10.4

- fork: itamaro
- ref: eager_tasks_factory
- machine: linux-x86_64
- commit hash: bcf40dc
- commit date: 2023-03-20
- overall geometric mean: 1.31x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.33x faster                                                   |
| chameleon      | 8.86 ms                                                | 6.27 ms: 1.41x faster                                                  |
| docutils       | 3.18 sec                                               | 2.52 sec: 1.26x faster                                                 |
| html5lib       | 85.8 ms                                                | 60.6 ms: 1.41x faster                                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 136 ms                                                 | 87.6 ms: 1.55x faster                                                  |
| float          | 108 ms                                                 | 74.0 ms: 1.46x faster                                                  |
| pidigits       | 190 ms                                                 | 197 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 132 ms: 1.32x faster                                                   |
| regex_v8       | 25.0 ms                                                | 22.1 ms: 1.13x faster                                                  |
| regex_dna      | 214 ms                                                 | 204 ms: 1.05x faster                                                   |
| regex_effbot   | 3.21 ms                                                | 3.30 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 281 us: 1.61x faster                                                   |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.50x faster                                                   |
| json_dumps           | 13.5 ms                                                | 9.51 ms: 1.42x faster                                                  |
| xml_etree_process    | 74.5 ms                                                | 55.3 ms: 1.35x faster                                                  |
| json_loads           | 28.9 us                                                | 24.0 us: 1.20x faster                                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.1 ms: 1.16x faster                                                  |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                                   |
| pickle_list          | 4.50 us                                                | 4.21 us: 1.07x faster                                                  |
| unpickle             | 14.3 us                                                | 13.4 us: 1.06x faster                                                  |
| unpickle_list        | 4.99 us                                                | 4.97 us: 1.00x faster                                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.03x slower                                                  |
| pickle_dict          | 28.3 us                                                | 31.3 us: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.96 ms: 1.55x faster                                                  |
| python_startup_no_site | 5.76 ms                                                | 6.55 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.0 ms: 1.46x faster                                                  |
| mako            | 14.3 ms                                                | 9.99 ms: 1.43x faster                                                  |
| django_template | 46.3 ms                                                | 33.2 ms: 1.39x faster                                                  |
| genshi_xml      | 63.6 ms                                                | 47.8 ms: 1.33x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.40x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.4 ms: 2.57x faster                                                  |
| deltablue               | 7.39 ms                                                | 3.14 ms: 2.35x faster                                                  |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                                   |
| logging_silent          | 173 ns                                                 | 96.2 ns: 1.80x faster                                                  |
| richards                | 71.4 ms                                                | 42.0 ms: 1.70x faster                                                  |
| go                      | 226 ms                                                 | 135 ms: 1.68x faster                                                   |
| spectral_norm           | 148 ms                                                 | 88.2 ms: 1.68x faster                                                  |
| pyflate                 | 675 ms                                                 | 403 ms: 1.68x faster                                                   |
| raytrace                | 461 ms                                                 | 284 ms: 1.62x faster                                                   |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.61x faster                                                   |
| crypto_pyaes            | 118 ms                                                 | 73.2 ms: 1.61x faster                                                  |
| scimark_monte_carlo     | 105 ms                                                 | 65.5 ms: 1.60x faster                                                  |
| chaos                   | 104 ms                                                 | 65.5 ms: 1.59x faster                                                  |
| python_startup          | 13.9 ms                                                | 8.96 ms: 1.55x faster                                                  |
| nbody                   | 136 ms                                                 | 87.6 ms: 1.55x faster                                                  |
| hexiom                  | 9.42 ms                                                | 6.08 ms: 1.55x faster                                                  |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.50x faster                                                   |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.48x faster                                                   |
| deepcopy_memo           | 50.0 us                                                | 34.0 us: 1.47x faster                                                  |
| genshi_text             | 30.6 ms                                                | 21.0 ms: 1.46x faster                                                  |
| float                   | 108 ms                                                 | 74.0 ms: 1.46x faster                                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.41 ms: 1.44x faster                                                  |
| logging_format          | 8.92 us                                                | 6.23 us: 1.43x faster                                                  |
| mako                    | 14.3 ms                                                | 9.99 ms: 1.43x faster                                                  |
| json_dumps              | 13.5 ms                                                | 9.51 ms: 1.42x faster                                                  |
| logging_simple          | 8.06 us                                                | 5.69 us: 1.42x faster                                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.71 ms: 1.41x faster                                                  |
| html5lib                | 85.8 ms                                                | 60.6 ms: 1.41x faster                                                  |
| coroutines              | 31.7 ms                                                | 22.4 ms: 1.41x faster                                                  |
| chameleon               | 8.86 ms                                                | 6.27 ms: 1.41x faster                                                  |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                                 |
| scimark_fft             | 414 ms                                                 | 297 ms: 1.39x faster                                                   |
| django_template         | 46.3 ms                                                | 33.2 ms: 1.39x faster                                                  |
| unpack_sequence         | 59.5 ns                                                | 42.9 ns: 1.38x faster                                                  |
| async_tree_memoization  | 854 ms                                                 | 619 ms: 1.38x faster                                                   |
| async_tree_io           | 1.78 sec                                               | 1.29 sec: 1.38x faster                                                 |
| pprint_safe_repr        | 943 ms                                                 | 687 ms: 1.37x faster                                                   |
| async_tree_none         | 713 ms                                                 | 521 ms: 1.37x faster                                                   |
| pycparser               | 1.51 sec                                               | 1.12 sec: 1.35x faster                                                 |
| xml_etree_process       | 74.5 ms                                                | 55.3 ms: 1.35x faster                                                  |
| 2to3                    | 332 ms                                                 | 249 ms: 1.33x faster                                                   |
| deepcopy                | 429 us                                                 | 323 us: 1.33x faster                                                   |
| genshi_xml              | 63.6 ms                                                | 47.8 ms: 1.33x faster                                                  |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                                  |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.32x faster                                                  |
| regex_compile           | 174 ms                                                 | 132 ms: 1.32x faster                                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.18 ms: 1.31x faster                                                  |
| thrift                  | 1.03 ms                                                | 788 us: 1.31x faster                                                   |
| sqlglot_normalize       | 135 ms                                                 | 103 ms: 1.31x faster                                                   |
| fannkuch                | 477 ms                                                 | 365 ms: 1.31x faster                                                   |
| sqlglot_optimize        | 65.3 ms                                                | 50.6 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 736 ms: 1.29x faster                                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.28x faster                                                  |
| nqueens                 | 99.3 ms                                                | 78.2 ms: 1.27x faster                                                  |
| docutils                | 3.18 sec                                               | 2.52 sec: 1.26x faster                                                 |
| sqlalchemy_declarative  | 165 ms                                                 | 136 ms: 1.22x faster                                                   |
| bench_thread_pool       | 943 us                                                 | 783 us: 1.20x faster                                                   |
| json_loads              | 28.9 us                                                | 24.0 us: 1.20x faster                                                  |
| dulwich_log             | 75.5 ms                                                | 62.9 ms: 1.20x faster                                                  |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.6 ms: 1.20x faster                                                  |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                                  |
| sympy_expand            | 537 ms                                                 | 455 ms: 1.18x faster                                                   |
| json                    | 5.35 ms                                                | 4.59 ms: 1.17x faster                                                  |
| xml_etree_generate      | 93.3 ms                                                | 80.1 ms: 1.16x faster                                                  |
| sympy_str               | 324 ms                                                 | 281 ms: 1.16x faster                                                   |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                                  |
| regex_v8                | 25.0 ms                                                | 22.1 ms: 1.13x faster                                                  |
| sqlite_synth            | 2.90 us                                                | 2.58 us: 1.12x faster                                                  |
| sympy_sum               | 183 ms                                                 | 165 ms: 1.11x faster                                                   |
| mdp                     | 2.82 sec                                               | 2.55 sec: 1.11x faster                                                 |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                                   |
| meteor_contest          | 114 ms                                                 | 106 ms: 1.08x faster                                                   |
| pickle_list             | 4.50 us                                                | 4.21 us: 1.07x faster                                                  |
| unpickle                | 14.3 us                                                | 13.4 us: 1.06x faster                                                  |
| telco                   | 6.68 ms                                                | 6.36 ms: 1.05x faster                                                  |
| regex_dna               | 214 ms                                                 | 204 ms: 1.05x faster                                                   |
| async_generators        | 428 ms                                                 | 411 ms: 1.04x faster                                                   |
| unpickle_list           | 4.99 us                                                | 4.97 us: 1.00x faster                                                  |
| regex_effbot            | 3.21 ms                                                | 3.30 ms: 1.03x slower                                                  |
| pickle                  | 10.1 us                                                | 10.4 us: 1.03x slower                                                  |
| pidigits                | 190 ms                                                 | 197 ms: 1.04x slower                                                   |
| pickle_dict             | 28.3 us                                                | 31.3 us: 1.10x slower                                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.55 ms: 1.14x slower                                                  |
| coverage                | 75.3 ms                                                | 96.8 ms: 1.28x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint, tornado_http
Ignored benchmarks (7) of public/results/bm-20230320-3.12.0a6+-bcf40dc/bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
