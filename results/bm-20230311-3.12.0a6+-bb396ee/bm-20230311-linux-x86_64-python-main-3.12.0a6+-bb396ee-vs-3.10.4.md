
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: bb396ee
- commit date: 2023-03-11
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| chameleon      | 8.86 ms                                                | 6.37 ms: 1.39x faster                                  |
| docutils       | 3.18 sec                                               | 2.55 sec: 1.24x faster                                 |
| html5lib       | 85.8 ms                                                | 61.6 ms: 1.39x faster                                  |
| tornado_http   | 128 ms                                                 | 91.2 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 136 ms                                                 | 92.1 ms: 1.48x faster                                  |
| float          | 108 ms                                                 | 74.1 ms: 1.45x faster                                  |
| pidigits       | 190 ms                                                 | 192 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 134 ms: 1.30x faster                                   |
| regex_v8       | 25.0 ms                                                | 21.7 ms: 1.15x faster                                  |
| regex_dna      | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.66 ms: 1.14x slower                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 287 us: 1.58x faster                                   |
| unpickle_pure_python | 297 us                                                 | 201 us: 1.47x faster                                   |
| json_dumps           | 13.5 ms                                                | 9.48 ms: 1.42x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 55.8 ms: 1.33x faster                                  |
| json_loads           | 28.9 us                                                | 24.0 us: 1.20x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.6 ms: 1.16x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 101 ms: 1.09x faster                                   |
| pickle_list          | 4.50 us                                                | 4.24 us: 1.06x faster                                  |
| unpickle             | 14.3 us                                                | 13.5 us: 1.05x faster                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.3 us: 1.10x slower                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.96 ms: 1.55x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.50 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.9 ms: 1.41x faster                                  |
| mako            | 14.3 ms                                                | 10.1 ms: 1.41x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.8 ms: 1.40x faster                                  |
| genshi_xml      | 63.6 ms                                                | 48.2 ms: 1.32x faster                                  |
| Geometric mean  | (ref)                                                  | 1.38x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.8 ms                                                | 30.3 ms: 2.50x faster                                  |
| deltablue               | 7.39 ms                                                | 3.22 ms: 2.30x faster                                  |
| logging_silent          | 173 ns                                                 | 95.2 ns: 1.82x faster                                  |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                   |
| go                      | 226 ms                                                 | 135 ms: 1.68x faster                                   |
| pyflate                 | 675 ms                                                 | 403 ms: 1.68x faster                                   |
| richards                | 71.4 ms                                                | 42.9 ms: 1.66x faster                                  |
| raytrace                | 461 ms                                                 | 284 ms: 1.62x faster                                   |
| crypto_pyaes            | 118 ms                                                 | 73.9 ms: 1.59x faster                                  |
| spectral_norm           | 148 ms                                                 | 93.3 ms: 1.59x faster                                  |
| pickle_pure_python      | 453 us                                                 | 287 us: 1.58x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 66.5 ms: 1.58x faster                                  |
| python_startup          | 13.9 ms                                                | 8.96 ms: 1.55x faster                                  |
| chaos                   | 104 ms                                                 | 67.8 ms: 1.53x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.17 ms: 1.53x faster                                  |
| nbody                   | 136 ms                                                 | 92.1 ms: 1.48x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 201 us: 1.47x faster                                   |
| float                   | 108 ms                                                 | 74.1 ms: 1.45x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 41.3 ns: 1.44x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.8 us: 1.44x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.42 ms: 1.43x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.48 ms: 1.42x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                 |
| django_template         | 46.3 ms                                                | 32.9 ms: 1.41x faster                                  |
| tornado_http            | 128 ms                                                 | 91.2 ms: 1.41x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.41x faster                                  |
| mako                    | 14.3 ms                                                | 10.1 ms: 1.41x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.8 ms: 1.40x faster                                  |
| logging_format          | 8.92 us                                                | 6.36 us: 1.40x faster                                  |
| logging_simple          | 8.06 us                                                | 5.77 us: 1.40x faster                                  |
| coroutines              | 31.7 ms                                                | 22.7 ms: 1.39x faster                                  |
| html5lib                | 85.8 ms                                                | 61.6 ms: 1.39x faster                                  |
| chameleon               | 8.86 ms                                                | 6.37 ms: 1.39x faster                                  |
| pprint_safe_repr        | 943 ms                                                 | 680 ms: 1.39x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.28 sec: 1.39x faster                                 |
| scimark_lu              | 158 ms                                                 | 114 ms: 1.38x faster                                   |
| async_tree_none         | 713 ms                                                 | 520 ms: 1.37x faster                                   |
| fannkuch                | 477 ms                                                 | 355 ms: 1.34x faster                                   |
| pycparser               | 1.51 sec                                               | 1.13 sec: 1.34x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 55.8 ms: 1.33x faster                                  |
| 2to3                    | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                  |
| scimark_fft             | 414 ms                                                 | 313 ms: 1.32x faster                                   |
| thrift                  | 1.03 ms                                                | 782 us: 1.32x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.32x faster                                  |
| genshi_xml              | 63.6 ms                                                | 48.2 ms: 1.32x faster                                  |
| async_tree_memoization  | 854 ms                                                 | 649 ms: 1.32x faster                                   |
| regex_compile           | 174 ms                                                 | 134 ms: 1.30x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 738 ms: 1.29x faster                                   |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.28x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                | 51.0 ms: 1.28x faster                                  |
| deepcopy                | 429 us                                                 | 336 us: 1.28x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 3.00 us: 1.25x faster                                  |
| docutils                | 3.18 sec                                               | 2.55 sec: 1.24x faster                                 |
| json_loads              | 28.9 us                                                | 24.0 us: 1.20x faster                                  |
| bench_thread_pool       | 943 us                                                 | 789 us: 1.19x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.59 ms: 1.19x faster                                  |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.7 ms: 1.19x faster                                  |
| nqueens                 | 99.3 ms                                                | 83.3 ms: 1.19x faster                                  |
| dulwich_log             | 75.5 ms                                                | 63.7 ms: 1.19x faster                                  |
| sqlalchemy_declarative  | 165 ms                                                 | 140 ms: 1.18x faster                                   |
| json                    | 5.35 ms                                                | 4.57 ms: 1.17x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                  |
| sympy_expand            | 537 ms                                                 | 461 ms: 1.17x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 80.6 ms: 1.16x faster                                  |
| regex_v8                | 25.0 ms                                                | 21.7 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 284 ms: 1.14x faster                                   |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| mdp                     | 2.82 sec                                               | 2.55 sec: 1.11x faster                                 |
| sqlite_synth            | 2.90 us                                                | 2.63 us: 1.10x faster                                  |
| sympy_sum               | 183 ms                                                 | 167 ms: 1.10x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 101 ms: 1.09x faster                                   |
| meteor_contest          | 114 ms                                                 | 106 ms: 1.07x faster                                   |
| pickle_list             | 4.50 us                                                | 4.24 us: 1.06x faster                                  |
| unpickle                | 14.3 us                                                | 13.5 us: 1.05x faster                                  |
| regex_dna               | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| async_generators        | 428 ms                                                 | 415 ms: 1.03x faster                                   |
| telco                   | 6.68 ms                                                | 6.49 ms: 1.03x faster                                  |
| pidigits                | 190 ms                                                 | 192 ms: 1.01x slower                                   |
| pickle                  | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.3 us: 1.10x slower                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.50 ms: 1.13x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.66 ms: 1.14x slower                                  |
| coverage                | 75.3 ms                                                | 97.3 ms: 1.29x slower                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (2): unpickle_list, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230311-3.12.0a6+-bb396ee/bm-20230311-linux-x86_64-python-main-3.12.0a6+-bb396ee.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
