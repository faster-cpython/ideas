
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 666c084
- commit date: 2023-01-28
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| chameleon      | 8.86 ms                                                | 6.45 ms: 1.37x faster                                  |
| docutils       | 3.18 sec                                               | 2.48 sec: 1.28x faster                                 |
| html5lib       | 85.8 ms                                                | 60.1 ms: 1.43x faster                                  |
| tornado_http   | 128 ms                                                 | 94.4 ms: 1.36x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 71.4 ms: 1.51x faster                                  |
| nbody          | 136 ms                                                 | 94.7 ms: 1.44x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 129 ms: 1.35x faster                                   |
| regex_dna      | 214 ms                                                 | 208 ms: 1.03x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.46 ms: 1.08x slower                                  |
| regex_v8       | 25.0 ms                                                | 21.2 ms: 1.18x faster                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.57 ms: 1.41x faster                                  |
| json_loads           | 28.9 us                                                | 24.1 us: 1.20x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.0 us: 1.09x slower                                  |
| pickle_list          | 4.50 us                                                | 4.01 us: 1.12x faster                                  |
| pickle_pure_python   | 453 us                                                 | 284 us: 1.60x faster                                   |
| unpickle             | 14.3 us                                                | 13.4 us: 1.06x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.93 us: 1.01x faster                                  |
| unpickle_pure_python | 297 us                                                 | 201 us: 1.47x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 77.6 ms: 1.20x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.5 ms: 1.39x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.90 ms: 1.57x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.44 ms: 1.12x slower                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.8 ms: 1.41x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.6 ms: 1.49x faster                                  |
| genshi_xml      | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| mako            | 14.3 ms                                                | 9.70 ms: 1.47x faster                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| aiohttp                 | 1.34 ms                                                | 998 us: 1.34x faster                                   |
| async_generators        | 428 ms                                                 | 350 ms: 1.22x faster                                   |
| async_tree_none         | 713 ms                                                 | 525 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 758 ms: 1.25x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.36x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 656 ms: 1.30x faster                                   |
| chameleon               | 8.86 ms                                                | 6.45 ms: 1.37x faster                                  |
| chaos                   | 104 ms                                                 | 64.8 ms: 1.61x faster                                  |
| bench_thread_pool       | 943 us                                                 | 786 us: 1.20x faster                                   |
| coroutines              | 31.7 ms                                                | 24.9 ms: 1.27x faster                                  |
| coverage                | 75.3 ms                                                | 98.3 ms: 1.30x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 72.9 ms: 1.61x faster                                  |
| deepcopy                | 429 us                                                 | 327 us: 1.31x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 3.00 us: 1.25x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.7 us: 1.44x faster                                  |
| deltablue               | 7.39 ms                                                | 3.19 ms: 2.31x faster                                  |
| django_template         | 46.3 ms                                                | 32.8 ms: 1.41x faster                                  |
| docutils                | 3.18 sec                                               | 2.48 sec: 1.28x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.9 ms: 1.20x faster                                  |
| fannkuch                | 477 ms                                                 | 361 ms: 1.32x faster                                   |
| float                   | 108 ms                                                 | 71.4 ms: 1.51x faster                                  |
| generators              | 75.8 ms                                                | 76.5 ms: 1.01x slower                                  |
| genshi_text             | 30.6 ms                                                | 20.6 ms: 1.49x faster                                  |
| genshi_xml              | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| go                      | 226 ms                                                 | 140 ms: 1.62x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                  |
| hexiom                  | 9.42 ms                                                | 5.94 ms: 1.59x faster                                  |
| html5lib                | 85.8 ms                                                | 60.1 ms: 1.43x faster                                  |
| json                    | 5.35 ms                                                | 4.66 ms: 1.15x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.57 ms: 1.41x faster                                  |
| json_loads              | 28.9 us                                                | 24.1 us: 1.20x faster                                  |
| logging_format          | 8.92 us                                                | 6.35 us: 1.41x faster                                  |
| logging_silent          | 173 ns                                                 | 92.4 ns: 1.87x faster                                  |
| logging_simple          | 8.06 us                                                | 5.79 us: 1.39x faster                                  |
| mako                    | 14.3 ms                                                | 9.70 ms: 1.47x faster                                  |
| mdp                     | 2.82 sec                                               | 2.68 sec: 1.05x faster                                 |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.09x faster                                   |
| mypy                    | 1.01 sec                                               | 802 ms: 1.26x faster                                   |
| nbody                   | 136 ms                                                 | 94.7 ms: 1.44x faster                                  |
| nqueens                 | 99.3 ms                                                | 78.1 ms: 1.27x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.6 ms: 1.14x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.0 us: 1.09x slower                                  |
| pickle_list             | 4.50 us                                                | 4.01 us: 1.12x faster                                  |
| pickle_pure_python      | 453 us                                                 | 284 us: 1.60x faster                                   |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 675 ms: 1.40x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                 |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.37x faster                                 |
| pyflate                 | 675 ms                                                 | 399 ms: 1.69x faster                                   |
| python_startup          | 13.9 ms                                                | 8.90 ms: 1.57x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.44 ms: 1.12x slower                                  |
| raytrace                | 461 ms                                                 | 282 ms: 1.64x faster                                   |
| regex_compile           | 174 ms                                                 | 129 ms: 1.35x faster                                   |
| regex_dna               | 214 ms                                                 | 208 ms: 1.03x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.46 ms: 1.08x slower                                  |
| regex_v8                | 25.0 ms                                                | 21.2 ms: 1.18x faster                                  |
| richards                | 71.4 ms                                                | 42.7 ms: 1.67x faster                                  |
| scimark_fft             | 414 ms                                                 | 308 ms: 1.34x faster                                   |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.47x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.5 ms: 1.60x faster                                  |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.15 ms: 1.32x faster                                  |
| spectral_norm           | 148 ms                                                 | 97.9 ms: 1.51x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.41 ms: 1.44x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.70 ms: 1.42x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.0 ms: 1.28x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.28x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.58 us: 1.13x faster                                  |
| sympy_expand            | 537 ms                                                 | 457 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 19.9 ms: 1.20x faster                                  |
| sympy_sum               | 183 ms                                                 | 155 ms: 1.18x faster                                   |
| sympy_str               | 324 ms                                                 | 272 ms: 1.19x faster                                   |
| telco                   | 6.68 ms                                                | 6.45 ms: 1.04x faster                                  |
| thrift                  | 1.03 ms                                                | 744 us: 1.39x faster                                   |
| tornado_http            | 128 ms                                                 | 94.4 ms: 1.36x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 41.9 ns: 1.42x faster                                  |
| unpickle                | 14.3 us                                                | 13.4 us: 1.06x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.93 us: 1.01x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 201 us: 1.47x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 77.6 ms: 1.20x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.5 ms: 1.39x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230128-3.12.0a4+-666c084/bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
