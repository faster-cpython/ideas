
# Results vs. 3.10.4

- fork: python
- ref: e3c3f9fec099fe78d2f9
- machine: linux-x86_64
- commit hash: e3c3f9f
- commit date: 2023-02-27
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 247 ms: 1.34x faster                                                   |
| chameleon      | 8.86 ms                                                | 6.37 ms: 1.39x faster                                                  |
| docutils       | 3.18 sec                                               | 2.55 sec: 1.25x faster                                                 |
| html5lib       | 85.8 ms                                                | 61.3 ms: 1.40x faster                                                  |
| tornado_http   | 128 ms                                                 | 94.2 ms: 1.36x faster                                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 108 ms                                                 | 72.5 ms: 1.49x faster                                                  |
| nbody          | 136 ms                                                 | 96.0 ms: 1.42x faster                                                  |
| pidigits       | 190 ms                                                 | 193 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 131 ms: 1.33x faster                                                   |
| regex_v8       | 25.0 ms                                                | 21.7 ms: 1.15x faster                                                  |
| regex_dna      | 214 ms                                                 | 198 ms: 1.08x faster                                                   |
| regex_effbot   | 3.21 ms                                                | 3.63 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 280 us: 1.62x faster                                                   |
| unpickle_pure_python | 297 us                                                 | 195 us: 1.52x faster                                                   |
| json_dumps           | 13.5 ms                                                | 9.52 ms: 1.42x faster                                                  |
| xml_etree_process    | 74.5 ms                                                | 55.1 ms: 1.35x faster                                                  |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.6 ms: 1.16x faster                                                  |
| xml_etree_iterparse  | 110 ms                                                 | 99.8 ms: 1.11x faster                                                  |
| xml_etree_parse      | 163 ms                                                 | 150 ms: 1.09x faster                                                   |
| unpickle             | 14.3 us                                                | 13.2 us: 1.08x faster                                                  |
| pickle_list          | 4.50 us                                                | 4.33 us: 1.04x faster                                                  |
| unpickle_list        | 4.99 us                                                | 5.08 us: 1.02x slower                                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.02x slower                                                  |
| pickle_dict          | 28.3 us                                                | 32.5 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.95 ms: 1.56x faster                                                  |
| python_startup_no_site | 5.76 ms                                                | 6.49 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.9 ms: 1.47x faster                                                  |
| mako            | 14.3 ms                                                | 9.99 ms: 1.43x faster                                                  |
| django_template | 46.3 ms                                                | 32.5 ms: 1.42x faster                                                  |
| genshi_xml      | 63.6 ms                                                | 47.0 ms: 1.35x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.42x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.9 ms: 2.53x faster                                                  |
| deltablue               | 7.39 ms                                                | 3.11 ms: 2.38x faster                                                  |
| logging_silent          | 173 ns                                                 | 92.2 ns: 1.88x faster                                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.85x faster                                                   |
| richards                | 71.4 ms                                                | 41.0 ms: 1.74x faster                                                  |
| go                      | 226 ms                                                 | 132 ms: 1.71x faster                                                   |
| pyflate                 | 675 ms                                                 | 405 ms: 1.67x faster                                                   |
| raytrace                | 461 ms                                                 | 280 ms: 1.65x faster                                                   |
| crypto_pyaes            | 118 ms                                                 | 72.1 ms: 1.63x faster                                                  |
| pickle_pure_python      | 453 us                                                 | 280 us: 1.62x faster                                                   |
| spectral_norm           | 148 ms                                                 | 94.0 ms: 1.58x faster                                                  |
| hexiom                  | 9.42 ms                                                | 6.00 ms: 1.57x faster                                                  |
| python_startup          | 13.9 ms                                                | 8.95 ms: 1.56x faster                                                  |
| scimark_monte_carlo     | 105 ms                                                 | 68.3 ms: 1.53x faster                                                  |
| chaos                   | 104 ms                                                 | 68.2 ms: 1.53x faster                                                  |
| unpickle_pure_python    | 297 us                                                 | 195 us: 1.52x faster                                                   |
| float                   | 108 ms                                                 | 72.5 ms: 1.49x faster                                                  |
| genshi_text             | 30.6 ms                                                | 20.9 ms: 1.47x faster                                                  |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.46x faster                                                   |
| deepcopy_memo           | 50.0 us                                                | 34.6 us: 1.44x faster                                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.41 ms: 1.44x faster                                                  |
| mako                    | 14.3 ms                                                | 9.99 ms: 1.43x faster                                                  |
| django_template         | 46.3 ms                                                | 32.5 ms: 1.42x faster                                                  |
| nbody                   | 136 ms                                                 | 96.0 ms: 1.42x faster                                                  |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                                 |
| json_dumps              | 13.5 ms                                                | 9.52 ms: 1.42x faster                                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.71 ms: 1.42x faster                                                  |
| unpack_sequence         | 59.5 ns                                                | 42.2 ns: 1.41x faster                                                  |
| html5lib                | 85.8 ms                                                | 61.3 ms: 1.40x faster                                                  |
| logging_format          | 8.92 us                                                | 6.38 us: 1.40x faster                                                  |
| chameleon               | 8.86 ms                                                | 6.37 ms: 1.39x faster                                                  |
| logging_simple          | 8.06 us                                                | 5.79 us: 1.39x faster                                                  |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.39x faster                                                 |
| pprint_safe_repr        | 943 ms                                                 | 680 ms: 1.39x faster                                                   |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.37x faster                                                 |
| tornado_http            | 128 ms                                                 | 94.2 ms: 1.36x faster                                                  |
| async_tree_none         | 713 ms                                                 | 524 ms: 1.36x faster                                                   |
| thrift                  | 1.03 ms                                                | 761 us: 1.36x faster                                                   |
| fannkuch                | 477 ms                                                 | 352 ms: 1.36x faster                                                   |
| genshi_xml              | 63.6 ms                                                | 47.0 ms: 1.35x faster                                                  |
| xml_etree_process       | 74.5 ms                                                | 55.1 ms: 1.35x faster                                                  |
| 2to3                    | 332 ms                                                 | 247 ms: 1.34x faster                                                   |
| coroutines              | 31.7 ms                                                | 23.7 ms: 1.34x faster                                                  |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                                  |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                                  |
| regex_compile           | 174 ms                                                 | 131 ms: 1.33x faster                                                   |
| scimark_fft             | 414 ms                                                 | 313 ms: 1.32x faster                                                   |
| async_tree_memoization  | 854 ms                                                 | 649 ms: 1.32x faster                                                   |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                                   |
| deepcopy                | 429 us                                                 | 333 us: 1.29x faster                                                   |
| sqlglot_optimize        | 65.3 ms                                                | 50.8 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 743 ms: 1.28x faster                                                   |
| nqueens                 | 99.3 ms                                                | 78.4 ms: 1.27x faster                                                  |
| docutils                | 3.18 sec                                               | 2.55 sec: 1.25x faster                                                 |
| deepcopy_reduce         | 3.75 us                                                | 3.02 us: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.48 ms: 1.22x faster                                                  |
| sqlalchemy_declarative  | 165 ms                                                 | 136 ms: 1.22x faster                                                   |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                                  |
| bench_thread_pool       | 943 us                                                 | 786 us: 1.20x faster                                                   |
| dulwich_log             | 75.5 ms                                                | 63.3 ms: 1.19x faster                                                  |
| json                    | 5.35 ms                                                | 4.53 ms: 1.18x faster                                                  |
| sympy_expand            | 537 ms                                                 | 455 ms: 1.18x faster                                                   |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.0 ms: 1.17x faster                                                  |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.16x faster                                                  |
| xml_etree_generate      | 93.3 ms                                                | 80.6 ms: 1.16x faster                                                  |
| sympy_str               | 324 ms                                                 | 281 ms: 1.16x faster                                                   |
| regex_v8                | 25.0 ms                                                | 21.7 ms: 1.15x faster                                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                                  |
| sympy_sum               | 183 ms                                                 | 165 ms: 1.11x faster                                                   |
| xml_etree_iterparse     | 110 ms                                                 | 99.8 ms: 1.11x faster                                                  |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                                   |
| sqlite_synth            | 2.90 us                                                | 2.64 us: 1.10x faster                                                  |
| xml_etree_parse         | 163 ms                                                 | 150 ms: 1.09x faster                                                   |
| regex_dna               | 214 ms                                                 | 198 ms: 1.08x faster                                                   |
| unpickle                | 14.3 us                                                | 13.2 us: 1.08x faster                                                  |
| mdp                     | 2.82 sec                                               | 2.69 sec: 1.05x faster                                                 |
| async_generators        | 428 ms                                                 | 409 ms: 1.04x faster                                                   |
| pickle_list             | 4.50 us                                                | 4.33 us: 1.04x faster                                                  |
| telco                   | 6.68 ms                                                | 6.53 ms: 1.02x faster                                                  |
| pidigits                | 190 ms                                                 | 193 ms: 1.01x slower                                                   |
| unpickle_list           | 4.99 us                                                | 5.08 us: 1.02x slower                                                  |
| pickle                  | 10.1 us                                                | 10.4 us: 1.02x slower                                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.49 ms: 1.13x slower                                                  |
| regex_effbot            | 3.21 ms                                                | 3.63 ms: 1.13x slower                                                  |
| pickle_dict             | 28.3 us                                                | 32.5 us: 1.15x slower                                                  |
| coverage                | 75.3 ms                                                | 96.5 ms: 1.28x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230227-3.12.0a5+-e3c3f9f/bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
