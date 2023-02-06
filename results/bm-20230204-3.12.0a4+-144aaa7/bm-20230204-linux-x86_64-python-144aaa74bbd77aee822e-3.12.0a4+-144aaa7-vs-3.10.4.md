
# Results vs. 3.10.4

- fork: python
- ref: 144aaa74bbd77aee822e
- machine: linux-x86_64
- commit hash: 144aaa7
- commit date: 2023-02-04
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 253 ms: 1.32x faster                                                   |
| chameleon      | 8.86 ms                                                | 6.25 ms: 1.42x faster                                                  |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                                 |
| html5lib       | 85.8 ms                                                | 59.6 ms: 1.44x faster                                                  |
| tornado_http   | 128 ms                                                 | 93.8 ms: 1.37x faster                                                  |
| Geometric mean | (ref)                                                  | 1.36x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 108 ms                                                 | 72.4 ms: 1.49x faster                                                  |
| nbody          | 136 ms                                                 | 97.5 ms: 1.40x faster                                                  |
| pidigits       | 190 ms                                                 | 193 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 126 ms: 1.38x faster                                                   |
| regex_v8       | 25.0 ms                                                | 22.2 ms: 1.12x faster                                                  |
| regex_dna      | 214 ms                                                 | 210 ms: 1.02x faster                                                   |
| regex_effbot   | 3.21 ms                                                | 3.63 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 281 us: 1.61x faster                                                   |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.50x faster                                                   |
| json_dumps           | 13.5 ms                                                | 9.48 ms: 1.42x faster                                                  |
| xml_etree_process    | 74.5 ms                                                | 53.5 ms: 1.39x faster                                                  |
| xml_etree_generate   | 93.3 ms                                                | 77.4 ms: 1.21x faster                                                  |
| json_loads           | 28.9 us                                                | 24.1 us: 1.20x faster                                                  |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                                   |
| pickle_list          | 4.50 us                                                | 4.24 us: 1.06x faster                                                  |
| unpickle_list        | 4.99 us                                                | 5.12 us: 1.03x slower                                                  |
| unpickle             | 14.3 us                                                | 14.9 us: 1.04x slower                                                  |
| pickle_dict          | 28.3 us                                                | 31.9 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.93 ms: 1.56x faster                                                  |
| python_startup_no_site | 5.76 ms                                                | 6.46 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.5 ms: 1.49x faster                                                  |
| mako            | 14.3 ms                                                | 9.79 ms: 1.46x faster                                                  |
| django_template | 46.3 ms                                                | 32.6 ms: 1.42x faster                                                  |
| genshi_xml      | 63.6 ms                                                | 47.0 ms: 1.35x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.31x faster                                                  |
| logging_silent          | 173 ns                                                 | 92.3 ns: 1.88x faster                                                  |
| scimark_sor             | 193 ms                                                 | 109 ms: 1.78x faster                                                   |
| richards                | 71.4 ms                                                | 42.3 ms: 1.69x faster                                                  |
| go                      | 226 ms                                                 | 134 ms: 1.68x faster                                                   |
| pyflate                 | 675 ms                                                 | 404 ms: 1.67x faster                                                   |
| raytrace                | 461 ms                                                 | 282 ms: 1.64x faster                                                   |
| crypto_pyaes            | 118 ms                                                 | 72.1 ms: 1.63x faster                                                  |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.61x faster                                                   |
| chaos                   | 104 ms                                                 | 65.0 ms: 1.60x faster                                                  |
| python_startup          | 13.9 ms                                                | 8.93 ms: 1.56x faster                                                  |
| scimark_monte_carlo     | 105 ms                                                 | 67.2 ms: 1.56x faster                                                  |
| hexiom                  | 9.42 ms                                                | 6.05 ms: 1.56x faster                                                  |
| spectral_norm           | 148 ms                                                 | 97.2 ms: 1.52x faster                                                  |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.50x faster                                                   |
| genshi_text             | 30.6 ms                                                | 20.5 ms: 1.49x faster                                                  |
| float                   | 108 ms                                                 | 72.4 ms: 1.49x faster                                                  |
| deepcopy_memo           | 50.0 us                                                | 34.2 us: 1.46x faster                                                  |
| mako                    | 14.3 ms                                                | 9.79 ms: 1.46x faster                                                  |
| scimark_lu              | 158 ms                                                 | 110 ms: 1.44x faster                                                   |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                                 |
| html5lib                | 85.8 ms                                                | 59.6 ms: 1.44x faster                                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.43x faster                                                  |
| unpack_sequence         | 59.5 ns                                                | 41.7 ns: 1.43x faster                                                  |
| json_dumps              | 13.5 ms                                                | 9.48 ms: 1.42x faster                                                  |
| logging_format          | 8.92 us                                                | 6.29 us: 1.42x faster                                                  |
| django_template         | 46.3 ms                                                | 32.6 ms: 1.42x faster                                                  |
| chameleon               | 8.86 ms                                                | 6.25 ms: 1.42x faster                                                  |
| logging_simple          | 8.06 us                                                | 5.71 us: 1.41x faster                                                  |
| pprint_safe_repr        | 943 ms                                                 | 669 ms: 1.41x faster                                                   |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.41x faster                                                  |
| nbody                   | 136 ms                                                 | 97.5 ms: 1.40x faster                                                  |
| xml_etree_process       | 74.5 ms                                                | 53.5 ms: 1.39x faster                                                  |
| regex_compile           | 174 ms                                                 | 126 ms: 1.38x faster                                                   |
| tornado_http            | 128 ms                                                 | 93.8 ms: 1.37x faster                                                  |
| thrift                  | 1.03 ms                                                | 758 us: 1.36x faster                                                   |
| async_tree_none         | 713 ms                                                 | 526 ms: 1.36x faster                                                   |
| genshi_xml              | 63.6 ms                                                | 47.0 ms: 1.35x faster                                                  |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                                 |
| aiohttp                 | 1.34 ms                                                | 997 us: 1.34x faster                                                   |
| scimark_fft             | 414 ms                                                 | 310 ms: 1.33x faster                                                   |
| deepcopy                | 429 us                                                 | 323 us: 1.33x faster                                                   |
| pycparser               | 1.51 sec                                               | 1.14 sec: 1.33x faster                                                 |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.32x faster                                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.15 ms: 1.32x faster                                                  |
| 2to3                    | 332 ms                                                 | 253 ms: 1.32x faster                                                   |
| fannkuch                | 477 ms                                                 | 363 ms: 1.31x faster                                                   |
| async_tree_memoization  | 854 ms                                                 | 652 ms: 1.31x faster                                                   |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                                   |
| sqlglot_optimize        | 65.3 ms                                                | 50.8 ms: 1.29x faster                                                  |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.27x faster                                                  |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                                 |
| nqueens                 | 99.3 ms                                                | 78.3 ms: 1.27x faster                                                  |
| mypy                    | 1.01 sec                                               | 805 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 760 ms: 1.25x faster                                                   |
| coroutines              | 31.7 ms                                                | 25.7 ms: 1.23x faster                                                  |
| async_generators        | 428 ms                                                 | 352 ms: 1.22x faster                                                   |
| sympy_integrate         | 23.9 ms                                                | 19.7 ms: 1.21x faster                                                  |
| xml_etree_generate      | 93.3 ms                                                | 77.4 ms: 1.21x faster                                                  |
| sympy_str               | 324 ms                                                 | 270 ms: 1.20x faster                                                   |
| dulwich_log             | 75.5 ms                                                | 62.8 ms: 1.20x faster                                                  |
| bench_thread_pool       | 943 us                                                 | 785 us: 1.20x faster                                                   |
| json_loads              | 28.9 us                                                | 24.1 us: 1.20x faster                                                  |
| sympy_expand            | 537 ms                                                 | 455 ms: 1.18x faster                                                   |
| sympy_sum               | 183 ms                                                 | 156 ms: 1.18x faster                                                   |
| json                    | 5.35 ms                                                | 4.72 ms: 1.13x faster                                                  |
| regex_v8                | 25.0 ms                                                | 22.2 ms: 1.12x faster                                                  |
| sqlite_synth            | 2.90 us                                                | 2.60 us: 1.12x faster                                                  |
| pathlib                 | 20.0 ms                                                | 18.0 ms: 1.11x faster                                                  |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                                   |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                                   |
| mdp                     | 2.82 sec                                               | 2.61 sec: 1.08x faster                                                 |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                                   |
| pickle_list             | 4.50 us                                                | 4.24 us: 1.06x faster                                                  |
| telco                   | 6.68 ms                                                | 6.55 ms: 1.02x faster                                                  |
| regex_dna               | 214 ms                                                 | 210 ms: 1.02x faster                                                   |
| generators              | 75.8 ms                                                | 76.4 ms: 1.01x slower                                                  |
| pidigits                | 190 ms                                                 | 193 ms: 1.01x slower                                                   |
| unpickle_list           | 4.99 us                                                | 5.12 us: 1.03x slower                                                  |
| unpickle                | 14.3 us                                                | 14.9 us: 1.04x slower                                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.46 ms: 1.12x slower                                                  |
| pickle_dict             | 28.3 us                                                | 31.9 us: 1.13x slower                                                  |
| regex_effbot            | 3.21 ms                                                | 3.63 ms: 1.13x slower                                                  |
| coverage                | 75.3 ms                                                | 94.5 ms: 1.25x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                           |

Benchmark hidden because not significant (2): bench_mp_pool, pickle
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230204-3.12.0a4+-144aaa7/bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
