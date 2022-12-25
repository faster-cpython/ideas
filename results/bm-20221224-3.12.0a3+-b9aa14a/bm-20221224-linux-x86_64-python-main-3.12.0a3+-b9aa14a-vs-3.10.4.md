Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| chameleon      | 8.86 ms                                                | 6.38 ms: 1.39x faster                                  |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                 |
| html5lib       | 85.8 ms                                                | 60.2 ms: 1.43x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.1 ms: 1.49x faster                                  |
| nbody          | 136 ms                                                 | 96.5 ms: 1.41x faster                                  |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_dna      | 214 ms                                                 | 206 ms: 1.04x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.40 ms: 1.06x slower                                  |
| regex_v8       | 25.0 ms                                                | 21.9 ms: 1.14x faster                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.42 ms: 1.43x faster                                  |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 32.4 us: 1.15x slower                                  |
| pickle_list          | 4.50 us                                                | 4.25 us: 1.06x faster                                  |
| pickle_pure_python   | 453 us                                                 | 282 us: 1.61x faster                                   |
| unpickle             | 14.3 us                                                | 13.0 us: 1.10x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.91 us: 1.02x faster                                  |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.50x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.9 ms: 1.23x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.49 ms: 1.64x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.08 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 33.0 ms: 1.40x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.9 ms: 1.47x faster                                  |
| genshi_xml      | 63.6 ms                                                | 49.0 ms: 1.30x faster                                  |
| mako            | 14.3 ms                                                | 9.59 ms: 1.49x faster                                  |
| Geometric mean  | (ref)                                                  | 1.41x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| async_generators        | 428 ms                                                 | 353 ms: 1.21x faster                                   |
| async_tree_none         | 713 ms                                                 | 525 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 759 ms: 1.25x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 622 ms: 1.37x faster                                   |
| chameleon               | 8.86 ms                                                | 6.38 ms: 1.39x faster                                  |
| chaos                   | 104 ms                                                 | 69.6 ms: 1.50x faster                                  |
| bench_thread_pool       | 943 us                                                 | 781 us: 1.21x faster                                   |
| coroutines              | 31.7 ms                                                | 24.8 ms: 1.28x faster                                  |
| coverage                | 75.3 ms                                                | 98.1 ms: 1.30x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 75.2 ms: 1.56x faster                                  |
| deepcopy                | 429 us                                                 | 330 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.95 us: 1.27x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 33.4 us: 1.50x faster                                  |
| deltablue               | 7.39 ms                                                | 3.27 ms: 2.26x faster                                  |
| django_template         | 46.3 ms                                                | 33.0 ms: 1.40x faster                                  |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.3 ms: 1.21x faster                                  |
| fannkuch                | 477 ms                                                 | 375 ms: 1.27x faster                                   |
| float                   | 108 ms                                                 | 72.1 ms: 1.49x faster                                  |
| generators              | 75.8 ms                                                | 77.6 ms: 1.02x slower                                  |
| genshi_text             | 30.6 ms                                                | 20.9 ms: 1.47x faster                                  |
| genshi_xml              | 63.6 ms                                                | 49.0 ms: 1.30x faster                                  |
| go                      | 226 ms                                                 | 138 ms: 1.64x faster                                   |
| hexiom                  | 9.42 ms                                                | 6.09 ms: 1.55x faster                                  |
| html5lib                | 85.8 ms                                                | 60.2 ms: 1.43x faster                                  |
| json                    | 5.35 ms                                                | 4.74 ms: 1.13x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.42 ms: 1.43x faster                                  |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| logging_format          | 8.92 us                                                | 6.29 us: 1.42x faster                                  |
| logging_silent          | 173 ns                                                 | 94.8 ns: 1.83x faster                                  |
| logging_simple          | 8.06 us                                                | 5.67 us: 1.42x faster                                  |
| mako                    | 14.3 ms                                                | 9.59 ms: 1.49x faster                                  |
| mdp                     | 2.82 sec                                               | 2.54 sec: 1.11x faster                                 |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                   |
| mypy                    | 1.01 sec                                               | 810 ms: 1.25x faster                                   |
| nbody                   | 136 ms                                                 | 96.5 ms: 1.41x faster                                  |
| nqueens                 | 99.3 ms                                                | 79.1 ms: 1.26x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 32.4 us: 1.15x slower                                  |
| pickle_list             | 4.50 us                                                | 4.25 us: 1.06x faster                                  |
| pickle_pure_python      | 453 us                                                 | 282 us: 1.61x faster                                   |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 671 ms: 1.41x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                 |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.38x faster                                 |
| pyflate                 | 675 ms                                                 | 403 ms: 1.67x faster                                   |
| python_startup          | 13.9 ms                                                | 8.49 ms: 1.64x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.08 ms: 1.06x slower                                  |
| raytrace                | 461 ms                                                 | 282 ms: 1.64x faster                                   |
| regex_compile           | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_dna               | 214 ms                                                 | 206 ms: 1.04x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.40 ms: 1.06x slower                                  |
| regex_v8                | 25.0 ms                                                | 21.9 ms: 1.14x faster                                  |
| richards                | 71.4 ms                                                | 41.8 ms: 1.71x faster                                  |
| scimark_fft             | 414 ms                                                 | 316 ms: 1.31x faster                                   |
| scimark_lu              | 158 ms                                                 | 109 ms: 1.45x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.6 ms: 1.60x faster                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.85x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.25 ms: 1.29x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.4 ms: 1.55x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.40 ms: 1.46x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.70 ms: 1.42x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.9 ms: 1.28x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.28x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.56 us: 1.13x faster                                  |
| sympy_expand            | 537 ms                                                 | 456 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 162 ms: 1.13x faster                                   |
| sympy_str               | 324 ms                                                 | 281 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.25 ms: 1.07x faster                                  |
| thrift                  | 1.03 ms                                                | 750 us: 1.38x faster                                   |
| unpack_sequence         | 59.5 ns                                                | 43.2 ns: 1.38x faster                                  |
| unpickle                | 14.3 us                                                | 13.0 us: 1.10x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.91 us: 1.02x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.50x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.9 ms: 1.23x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20221224-3.12.0a3+-b9aa14a/bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a.json: djangocms
