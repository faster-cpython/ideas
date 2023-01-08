
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 951303f
- commit date: 2023-01-07
- overall geometric mean: 1.29x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 255 ms: 1.31x faster                                   |
| chameleon      | 8.86 ms                                                | 6.41 ms: 1.38x faster                                  |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                 |
| html5lib       | 85.8 ms                                                | 59.7 ms: 1.44x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.8 ms: 1.48x faster                                  |
| nbody          | 136 ms                                                 | 96.7 ms: 1.41x faster                                  |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna      | 214 ms                                                 | 189 ms: 1.13x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.17 ms: 1.01x faster                                  |
| regex_v8       | 25.0 ms                                                | 20.8 ms: 1.20x faster                                  |
| Geometric mean | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.51 ms: 1.42x faster                                  |
| json_loads           | 28.9 us                                                | 26.1 us: 1.11x faster                                  |
| pickle_dict          | 28.3 us                                                | 31.5 us: 1.11x slower                                  |
| pickle_list          | 4.50 us                                                | 4.14 us: 1.09x faster                                  |
| pickle_pure_python   | 453 us                                                 | 284 us: 1.59x faster                                   |
| unpickle             | 14.3 us                                                | 13.1 us: 1.09x faster                                  |
| unpickle_pure_python | 297 us                                                 | 210 us: 1.41x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 150 ms: 1.09x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 104 ms: 1.06x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 78.2 ms: 1.19x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.4 ms: 1.39x faster                                  |
| Geometric mean       | (ref)                                                  | 1.16x faster                                           |

Benchmark hidden because not significant (2): pickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.51 ms: 1.64x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.09 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.24x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.9 ms: 1.40x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.7 ms: 1.48x faster                                  |
| genshi_xml      | 63.6 ms                                                | 47.4 ms: 1.34x faster                                  |
| mako            | 14.3 ms                                                | 9.54 ms: 1.49x faster                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 255 ms: 1.31x faster                                   |
| async_generators        | 428 ms                                                 | 356 ms: 1.20x faster                                   |
| async_tree_none         | 713 ms                                                 | 536 ms: 1.33x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 757 ms: 1.25x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.33 sec: 1.33x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 672 ms: 1.27x faster                                   |
| chameleon               | 8.86 ms                                                | 6.41 ms: 1.38x faster                                  |
| chaos                   | 104 ms                                                 | 70.2 ms: 1.48x faster                                  |
| bench_thread_pool       | 943 us                                                 | 781 us: 1.21x faster                                   |
| coroutines              | 31.7 ms                                                | 25.2 ms: 1.26x faster                                  |
| coverage                | 75.3 ms                                                | 99.3 ms: 1.32x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 77.2 ms: 1.52x faster                                  |
| deepcopy                | 429 us                                                 | 330 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.90 us: 1.29x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 33.6 us: 1.49x faster                                  |
| deltablue               | 7.39 ms                                                | 3.25 ms: 2.27x faster                                  |
| django_template         | 46.3 ms                                                | 32.9 ms: 1.40x faster                                  |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.9 ms: 1.20x faster                                  |
| fannkuch                | 477 ms                                                 | 376 ms: 1.27x faster                                   |
| float                   | 108 ms                                                 | 72.8 ms: 1.48x faster                                  |
| generators              | 75.8 ms                                                | 76.2 ms: 1.01x slower                                  |
| genshi_text             | 30.6 ms                                                | 20.7 ms: 1.48x faster                                  |
| genshi_xml              | 63.6 ms                                                | 47.4 ms: 1.34x faster                                  |
| go                      | 226 ms                                                 | 136 ms: 1.66x faster                                   |
| hexiom                  | 9.42 ms                                                | 6.06 ms: 1.55x faster                                  |
| html5lib                | 85.8 ms                                                | 59.7 ms: 1.44x faster                                  |
| json                    | 5.35 ms                                                | 4.92 ms: 1.09x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.51 ms: 1.42x faster                                  |
| json_loads              | 28.9 us                                                | 26.1 us: 1.11x faster                                  |
| logging_format          | 8.92 us                                                | 6.31 us: 1.42x faster                                  |
| logging_silent          | 173 ns                                                 | 94.1 ns: 1.84x faster                                  |
| logging_simple          | 8.06 us                                                | 5.77 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.54 ms: 1.49x faster                                  |
| mdp                     | 2.82 sec                                               | 2.63 sec: 1.07x faster                                 |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.08x faster                                   |
| mypy                    | 1.01 sec                                               | 815 ms: 1.24x faster                                   |
| nbody                   | 136 ms                                                 | 96.7 ms: 1.41x faster                                  |
| nqueens                 | 99.3 ms                                                | 81.0 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                  |
| pickle_dict             | 28.3 us                                                | 31.5 us: 1.11x slower                                  |
| pickle_list             | 4.50 us                                                | 4.14 us: 1.09x faster                                  |
| pickle_pure_python      | 453 us                                                 | 284 us: 1.59x faster                                   |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 681 ms: 1.38x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                 |
| pycparser               | 1.51 sec                                               | 1.13 sec: 1.34x faster                                 |
| pyflate                 | 675 ms                                                 | 402 ms: 1.68x faster                                   |
| python_startup          | 13.9 ms                                                | 8.51 ms: 1.64x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.09 ms: 1.06x slower                                  |
| raytrace                | 461 ms                                                 | 282 ms: 1.63x faster                                   |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna               | 214 ms                                                 | 189 ms: 1.13x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.17 ms: 1.01x faster                                  |
| regex_v8                | 25.0 ms                                                | 20.8 ms: 1.20x faster                                  |
| richards                | 71.4 ms                                                | 42.3 ms: 1.69x faster                                  |
| scimark_fft             | 414 ms                                                 | 325 ms: 1.27x faster                                   |
| scimark_lu              | 158 ms                                                 | 109 ms: 1.45x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.6 ms: 1.62x faster                                  |
| scimark_sor             | 193 ms                                                 | 108 ms: 1.79x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.11 ms: 1.33x faster                                  |
| spectral_norm           | 148 ms                                                 | 98.6 ms: 1.50x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.40 ms: 1.46x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.69 ms: 1.43x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.7 ms: 1.26x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 107 ms: 1.26x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.60 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 462 ms: 1.16x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                  |
| sympy_sum               | 183 ms                                                 | 165 ms: 1.11x faster                                   |
| sympy_str               | 324 ms                                                 | 285 ms: 1.14x faster                                   |
| telco                   | 6.68 ms                                                | 6.36 ms: 1.05x faster                                  |
| thrift                  | 1.03 ms                                                | 757 us: 1.36x faster                                   |
| unpack_sequence         | 59.5 ns                                                | 42.4 ns: 1.40x faster                                  |
| unpickle                | 14.3 us                                                | 13.1 us: 1.09x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 210 us: 1.41x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 150 ms: 1.09x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 104 ms: 1.06x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 78.2 ms: 1.19x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.4 ms: 1.39x faster                                  |
| Geometric mean          | (ref)                                                  | 1.29x faster                                           |

Benchmark hidden because not significant (3): bench_mp_pool, pickle, unpickle_list
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20230107-3.12.0a3+-951303f/bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f.json: djangocms
