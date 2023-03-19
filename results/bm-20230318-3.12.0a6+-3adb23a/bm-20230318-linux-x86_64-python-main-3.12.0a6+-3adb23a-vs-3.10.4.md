
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3adb23a
- commit date: 2023-03-18
- overall geometric mean: 1.31x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.35 ms: 1.39x faster                                  |
| docutils       | 3.18 sec                                               | 2.53 sec: 1.26x faster                                 |
| html5lib       | 85.8 ms                                                | 61.2 ms: 1.40x faster                                  |
| tornado_http   | 128 ms                                                 | 91.2 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                  | 1.36x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 136 ms                                                 | 86.0 ms: 1.58x faster                                  |
| float          | 108 ms                                                 | 73.9 ms: 1.46x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.32x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 135 ms: 1.29x faster                                   |
| regex_v8       | 25.0 ms                                                | 21.7 ms: 1.15x faster                                  |
| regex_dna      | 214 ms                                                 | 201 ms: 1.06x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.63 ms: 1.13x slower                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 284 us: 1.60x faster                                   |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.49x faster                                   |
| json_dumps           | 13.5 ms                                                | 9.57 ms: 1.41x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 55.2 ms: 1.35x faster                                  |
| json_loads           | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.4 ms: 1.16x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 149 ms: 1.10x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.09x faster                                   |
| pickle_list          | 4.50 us                                                | 4.26 us: 1.06x faster                                  |
| unpickle             | 14.3 us                                                | 13.5 us: 1.06x faster                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.3 us: 1.10x slower                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.91 ms: 1.56x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.52 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| mako            | 14.3 ms                                                | 10.1 ms: 1.42x faster                                  |
| django_template | 46.3 ms                                                | 32.9 ms: 1.40x faster                                  |
| genshi_xml      | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| Geometric mean  | (ref)                                                  | 1.41x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.3 ms: 2.58x faster                                  |
| deltablue               | 7.39 ms                                                | 3.17 ms: 2.33x faster                                  |
| logging_silent          | 173 ns                                                 | 94.9 ns: 1.83x faster                                  |
| scimark_sor             | 193 ms                                                 | 106 ms: 1.82x faster                                   |
| richards                | 71.4 ms                                                | 41.9 ms: 1.70x faster                                  |
| go                      | 226 ms                                                 | 137 ms: 1.66x faster                                   |
| raytrace                | 461 ms                                                 | 280 ms: 1.64x faster                                   |
| pyflate                 | 675 ms                                                 | 414 ms: 1.63x faster                                   |
| spectral_norm           | 148 ms                                                 | 92.7 ms: 1.60x faster                                  |
| pickle_pure_python      | 453 us                                                 | 284 us: 1.60x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.7 ms: 1.59x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 73.7 ms: 1.59x faster                                  |
| nbody                   | 136 ms                                                 | 86.0 ms: 1.58x faster                                  |
| chaos                   | 104 ms                                                 | 66.0 ms: 1.58x faster                                  |
| python_startup          | 13.9 ms                                                | 8.91 ms: 1.56x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.11 ms: 1.54x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.49x faster                                   |
| deepcopy_memo           | 50.0 us                                                | 34.2 us: 1.46x faster                                  |
| float                   | 108 ms                                                 | 73.9 ms: 1.46x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| scimark_lu              | 158 ms                                                 | 109 ms: 1.45x faster                                   |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.43x faster                                  |
| mako                    | 14.3 ms                                                | 10.1 ms: 1.42x faster                                  |
| logging_simple          | 8.06 us                                                | 5.69 us: 1.42x faster                                  |
| logging_format          | 8.92 us                                                | 6.31 us: 1.41x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.71 ms: 1.41x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.57 ms: 1.41x faster                                  |
| tornado_http            | 128 ms                                                 | 91.2 ms: 1.41x faster                                  |
| django_template         | 46.3 ms                                                | 32.9 ms: 1.40x faster                                  |
| html5lib                | 85.8 ms                                                | 61.2 ms: 1.40x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.41 sec: 1.40x faster                                 |
| chameleon               | 8.86 ms                                                | 6.35 ms: 1.39x faster                                  |
| coroutines              | 31.7 ms                                                | 22.8 ms: 1.39x faster                                  |
| scimark_fft             | 414 ms                                                 | 300 ms: 1.38x faster                                   |
| unpack_sequence         | 59.5 ns                                                | 43.2 ns: 1.38x faster                                  |
| pprint_safe_repr        | 943 ms                                                 | 686 ms: 1.37x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.29 sec: 1.37x faster                                 |
| async_tree_none         | 713 ms                                                 | 523 ms: 1.36x faster                                   |
| pycparser               | 1.51 sec                                               | 1.11 sec: 1.36x faster                                 |
| genshi_xml              | 63.6 ms                                                | 47.1 ms: 1.35x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 55.2 ms: 1.35x faster                                  |
| thrift                  | 1.03 ms                                                | 771 us: 1.34x faster                                   |
| 2to3                    | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.33x faster                                  |
| deepcopy                | 429 us                                                 | 323 us: 1.33x faster                                   |
| async_tree_memoization  | 854 ms                                                 | 644 ms: 1.33x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.15 ms: 1.32x faster                                  |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.32x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 103 ms: 1.31x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.90 us: 1.29x faster                                  |
| regex_compile           | 174 ms                                                 | 135 ms: 1.29x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                | 50.9 ms: 1.28x faster                                  |
| nqueens                 | 99.3 ms                                                | 77.9 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 747 ms: 1.27x faster                                   |
| fannkuch                | 477 ms                                                 | 377 ms: 1.27x faster                                   |
| docutils                | 3.18 sec                                               | 2.53 sec: 1.26x faster                                 |
| sqlalchemy_declarative  | 165 ms                                                 | 137 ms: 1.21x faster                                   |
| bench_thread_pool       | 943 us                                                 | 785 us: 1.20x faster                                   |
| dulwich_log             | 75.5 ms                                                | 63.0 ms: 1.20x faster                                  |
| json_loads              | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.8 ms: 1.18x faster                                  |
| sympy_expand            | 537 ms                                                 | 458 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 80.4 ms: 1.16x faster                                  |
| json                    | 5.35 ms                                                | 4.62 ms: 1.16x faster                                  |
| regex_v8                | 25.0 ms                                                | 21.7 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 283 ms: 1.15x faster                                   |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.62 us: 1.11x faster                                  |
| sympy_sum               | 183 ms                                                 | 166 ms: 1.10x faster                                   |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 149 ms: 1.10x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.09x faster                                   |
| mdp                     | 2.82 sec                                               | 2.61 sec: 1.08x faster                                 |
| regex_dna               | 214 ms                                                 | 201 ms: 1.06x faster                                   |
| pickle_list             | 4.50 us                                                | 4.26 us: 1.06x faster                                  |
| unpickle                | 14.3 us                                                | 13.5 us: 1.06x faster                                  |
| telco                   | 6.68 ms                                                | 6.43 ms: 1.04x faster                                  |
| async_generators        | 428 ms                                                 | 413 ms: 1.03x faster                                   |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                   |
| pickle                  | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.3 us: 1.10x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.63 ms: 1.13x slower                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.52 ms: 1.13x slower                                  |
| coverage                | 75.3 ms                                                | 97.0 ms: 1.29x slower                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                           |

Benchmark hidden because not significant (2): bench_mp_pool, unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230318-3.12.0a6+-3adb23a/bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
