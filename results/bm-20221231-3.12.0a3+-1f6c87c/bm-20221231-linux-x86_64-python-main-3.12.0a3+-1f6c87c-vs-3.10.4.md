Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| chameleon      | 8.86 ms                                                | 6.42 ms: 1.38x faster                                  |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                 |
| html5lib       | 85.8 ms                                                | 60.3 ms: 1.42x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 71.2 ms: 1.51x faster                                  |
| nbody          | 136 ms                                                 | 94.2 ms: 1.45x faster                                  |
| pidigits       | 190 ms                                                 | 197 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 131 ms: 1.33x faster                                   |
| regex_dna      | 214 ms                                                 | 215 ms: 1.01x slower                                   |
| regex_effbot   | 3.21 ms                                                | 3.64 ms: 1.14x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.2 ms: 1.12x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.33 ms: 1.45x faster                                  |
| json_loads           | 28.9 us                                                | 23.8 us: 1.21x faster                                  |
| pickle               | 10.1 us                                                | 9.96 us: 1.02x faster                                  |
| pickle_dict          | 28.3 us                                                | 30.1 us: 1.06x slower                                  |
| pickle_list          | 4.50 us                                                | 4.00 us: 1.12x faster                                  |
| pickle_pure_python   | 453 us                                                 | 282 us: 1.61x faster                                   |
| unpickle             | 14.3 us                                                | 12.7 us: 1.13x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.95 us: 1.01x faster                                  |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.51x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.4 ms: 1.22x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean       | (ref)                                                  | 1.20x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.45 ms: 1.65x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.05 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.7 ms: 1.42x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.7 ms: 1.48x faster                                  |
| genshi_xml      | 63.6 ms                                                | 46.6 ms: 1.36x faster                                  |
| mako            | 14.3 ms                                                | 9.64 ms: 1.48x faster                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                   |
| async_generators        | 428 ms                                                 | 352 ms: 1.21x faster                                   |
| async_tree_none         | 713 ms                                                 | 524 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 751 ms: 1.26x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 620 ms: 1.38x faster                                   |
| chameleon               | 8.86 ms                                                | 6.42 ms: 1.38x faster                                  |
| chaos                   | 104 ms                                                 | 68.0 ms: 1.53x faster                                  |
| bench_thread_pool       | 943 us                                                 | 777 us: 1.21x faster                                   |
| coroutines              | 31.7 ms                                                | 25.5 ms: 1.24x faster                                  |
| coverage                | 75.3 ms                                                | 100 ms: 1.33x slower                                   |
| crypto_pyaes            | 118 ms                                                 | 74.4 ms: 1.58x faster                                  |
| deepcopy                | 429 us                                                 | 338 us: 1.27x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.27x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.1 us: 1.46x faster                                  |
| deltablue               | 7.39 ms                                                | 3.17 ms: 2.33x faster                                  |
| django_template         | 46.3 ms                                                | 32.7 ms: 1.42x faster                                  |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.4 ms: 1.21x faster                                  |
| fannkuch                | 477 ms                                                 | 377 ms: 1.26x faster                                   |
| float                   | 108 ms                                                 | 71.2 ms: 1.51x faster                                  |
| generators              | 75.8 ms                                                | 76.4 ms: 1.01x slower                                  |
| genshi_text             | 30.6 ms                                                | 20.7 ms: 1.48x faster                                  |
| genshi_xml              | 63.6 ms                                                | 46.6 ms: 1.36x faster                                  |
| go                      | 226 ms                                                 | 137 ms: 1.65x faster                                   |
| hexiom                  | 9.42 ms                                                | 6.04 ms: 1.56x faster                                  |
| html5lib                | 85.8 ms                                                | 60.3 ms: 1.42x faster                                  |
| json                    | 5.35 ms                                                | 4.64 ms: 1.15x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.33 ms: 1.45x faster                                  |
| json_loads              | 28.9 us                                                | 23.8 us: 1.21x faster                                  |
| logging_format          | 8.92 us                                                | 6.44 us: 1.39x faster                                  |
| logging_silent          | 173 ns                                                 | 91.4 ns: 1.89x faster                                  |
| logging_simple          | 8.06 us                                                | 5.72 us: 1.41x faster                                  |
| mako                    | 14.3 ms                                                | 9.64 ms: 1.48x faster                                  |
| mdp                     | 2.82 sec                                               | 2.64 sec: 1.07x faster                                 |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.11x faster                                   |
| mypy                    | 1.01 sec                                               | 811 ms: 1.25x faster                                   |
| nbody                   | 136 ms                                                 | 94.2 ms: 1.45x faster                                  |
| nqueens                 | 99.3 ms                                                | 78.9 ms: 1.26x faster                                  |
| pathlib                 | 20.0 ms                                                | 18.2 ms: 1.10x faster                                  |
| pickle                  | 10.1 us                                                | 9.96 us: 1.02x faster                                  |
| pickle_dict             | 28.3 us                                                | 30.1 us: 1.06x slower                                  |
| pickle_list             | 4.50 us                                                | 4.00 us: 1.12x faster                                  |
| pickle_pure_python      | 453 us                                                 | 282 us: 1.61x faster                                   |
| pidigits                | 190 ms                                                 | 197 ms: 1.04x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 694 ms: 1.36x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.42 sec: 1.39x faster                                 |
| pycparser               | 1.51 sec                                               | 1.14 sec: 1.33x faster                                 |
| pyflate                 | 675 ms                                                 | 402 ms: 1.68x faster                                   |
| python_startup          | 13.9 ms                                                | 8.45 ms: 1.65x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.05 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 281 ms: 1.64x faster                                   |
| regex_compile           | 174 ms                                                 | 131 ms: 1.33x faster                                   |
| regex_dna               | 214 ms                                                 | 215 ms: 1.01x slower                                   |
| regex_effbot            | 3.21 ms                                                | 3.64 ms: 1.14x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.2 ms: 1.12x faster                                  |
| richards                | 71.4 ms                                                | 41.5 ms: 1.72x faster                                  |
| scimark_fft             | 414 ms                                                 | 314 ms: 1.32x faster                                   |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.46x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.5 ms: 1.62x faster                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.86x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.30 ms: 1.27x faster                                  |
| spectral_norm           | 148 ms                                                 | 94.1 ms: 1.57x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.39 ms: 1.46x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.69 ms: 1.43x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.7 ms: 1.29x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.29x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.62 us: 1.11x faster                                  |
| sympy_expand            | 537 ms                                                 | 453 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.1 ms: 1.19x faster                                  |
| sympy_sum               | 183 ms                                                 | 162 ms: 1.13x faster                                   |
| sympy_str               | 324 ms                                                 | 281 ms: 1.16x faster                                   |
| telco                   | 6.68 ms                                                | 6.19 ms: 1.08x faster                                  |
| thrift                  | 1.03 ms                                                | 749 us: 1.38x faster                                   |
| unpack_sequence         | 59.5 ns                                                | 42.0 ns: 1.41x faster                                  |
| unpickle                | 14.3 us                                                | 12.7 us: 1.13x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.95 us: 1.01x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.51x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.4 ms: 1.22x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20221231-3.12.0a3+-1f6c87c/bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c.json: djangocms
