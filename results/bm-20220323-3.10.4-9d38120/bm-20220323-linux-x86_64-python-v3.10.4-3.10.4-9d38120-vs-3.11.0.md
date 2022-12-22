Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 332 ms: 1.29x slower                                   |
| chameleon      | 6.41 ms                                                | 8.86 ms: 1.38x slower                                  |
| docutils       | 2.60 sec                                               | 3.18 sec: 1.23x slower                                 |
| html5lib       | 63.2 ms                                                | 85.8 ms: 1.36x slower                                  |
| tornado_http   | 96.6 ms                                                | 128 ms: 1.33x slower                                   |
| Geometric mean | (ref)                                                  | 1.32x slower                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 108 ms: 1.41x slower                                   |
| nbody          | 95.0 ms                                                | 136 ms: 1.43x slower                                   |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.25x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 174 ms: 1.28x slower                                   |
| regex_dna      | 203 ms                                                 | 214 ms: 1.05x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.21 ms: 1.05x faster                                  |
| regex_v8       | 22.3 ms                                                | 25.0 ms: 1.12x slower                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 13.5 ms: 1.06x slower                                  |
| json_loads           | 26.2 us                                                | 28.9 us: 1.10x slower                                  |
| pickle               | 9.79 us                                                | 10.1 us: 1.03x slower                                  |
| pickle_dict          | 31.4 us                                                | 28.3 us: 1.11x faster                                  |
| pickle_list          | 4.17 us                                                | 4.50 us: 1.08x slower                                  |
| pickle_pure_python   | 304 us                                                 | 453 us: 1.49x slower                                   |
| unpickle             | 13.3 us                                                | 14.3 us: 1.08x slower                                  |
| unpickle_list        | 4.95 us                                                | 4.99 us: 1.01x slower                                  |
| unpickle_pure_python | 225 us                                                 | 297 us: 1.32x slower                                   |
| xml_etree_parse      | 158 ms                                                 | 163 ms: 1.03x slower                                   |
| xml_etree_iterparse  | 103 ms                                                 | 110 ms: 1.07x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 93.3 ms: 1.22x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 74.5 ms: 1.38x slower                                  |
| Geometric mean       | (ref)                                                  | 1.13x slower                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 13.9 ms: 1.67x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 5.76 ms: 1.03x faster                                  |
| Geometric mean         | (ref)                                                  | 1.27x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 46.3 ms: 1.43x slower                                  |
| genshi_text     | 22.1 ms                                                | 30.6 ms: 1.39x slower                                  |
| genshi_xml      | 52.1 ms                                                | 63.6 ms: 1.22x slower                                  |
| mako            | 9.85 ms                                                | 14.3 ms: 1.45x slower                                  |
| Geometric mean  | (ref)                                                  | 1.37x slower                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 332 ms: 1.29x slower                                   |
| aiohttp                 | 1.05 ms                                                | 1.34 ms: 1.28x slower                                  |
| async_generators        | 359 ms                                                 | 428 ms: 1.19x slower                                   |
| async_tree_none         | 529 ms                                                 | 713 ms: 1.35x slower                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 949 ms: 1.26x slower                                   |
| async_tree_io           | 1.31 sec                                               | 1.78 sec: 1.36x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 854 ms: 1.37x slower                                   |
| chameleon               | 6.41 ms                                                | 8.86 ms: 1.38x slower                                  |
| chaos                   | 68.6 ms                                                | 104 ms: 1.52x slower                                   |
| bench_thread_pool       | 810 us                                                 | 943 us: 1.16x slower                                   |
| coroutines              | 26.1 ms                                                | 31.7 ms: 1.21x slower                                  |
| coverage                | 101 ms                                                 | 75.3 ms: 1.33x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 118 ms: 1.59x slower                                   |
| deepcopy                | 344 us                                                 | 429 us: 1.25x slower                                   |
| deepcopy_reduce         | 2.97 us                                                | 3.75 us: 1.26x slower                                  |
| deepcopy_memo           | 36.4 us                                                | 50.0 us: 1.37x slower                                  |
| deltablue               | 3.64 ms                                                | 7.39 ms: 2.03x slower                                  |
| django_template         | 32.5 ms                                                | 46.3 ms: 1.43x slower                                  |
| docutils                | 2.60 sec                                               | 3.18 sec: 1.23x slower                                 |
| dulwich_log             | 63.9 ms                                                | 75.5 ms: 1.18x slower                                  |
| fannkuch                | 388 ms                                                 | 477 ms: 1.23x slower                                   |
| flaskblogging           | 7.08 ms                                                | 8.38 ms: 1.18x slower                                  |
| float                   | 76.3 ms                                                | 108 ms: 1.41x slower                                   |
| generators              | 72.2 ms                                                | 75.8 ms: 1.05x slower                                  |
| genshi_text             | 22.1 ms                                                | 30.6 ms: 1.39x slower                                  |
| genshi_xml              | 52.1 ms                                                | 63.6 ms: 1.22x slower                                  |
| go                      | 143 ms                                                 | 226 ms: 1.58x slower                                   |
| gunicorn                | 1.12 ms                                                | 1.43 ms: 1.28x slower                                  |
| hexiom                  | 6.35 ms                                                | 9.42 ms: 1.48x slower                                  |
| html5lib                | 63.2 ms                                                | 85.8 ms: 1.36x slower                                  |
| json                    | 4.95 ms                                                | 5.35 ms: 1.08x slower                                  |
| json_dumps              | 12.7 ms                                                | 13.5 ms: 1.06x slower                                  |
| json_loads              | 26.2 us                                                | 28.9 us: 1.10x slower                                  |
| logging_format          | 6.62 us                                                | 8.92 us: 1.35x slower                                  |
| logging_silent          | 98.5 ns                                                | 173 ns: 1.76x slower                                   |
| logging_simple          | 6.06 us                                                | 8.06 us: 1.33x slower                                  |
| mako                    | 9.85 ms                                                | 14.3 ms: 1.45x slower                                  |
| mdp                     | 2.62 sec                                               | 2.82 sec: 1.08x slower                                 |
| meteor_contest          | 105 ms                                                 | 114 ms: 1.09x slower                                   |
| mypy                    | 669 ms                                                 | 1.01 sec: 1.52x slower                                 |
| nbody                   | 95.0 ms                                                | 136 ms: 1.43x slower                                   |
| nqueens                 | 85.0 ms                                                | 99.3 ms: 1.17x slower                                  |
| pathlib                 | 18.2 ms                                                | 20.0 ms: 1.10x slower                                  |
| pickle                  | 9.79 us                                                | 10.1 us: 1.03x slower                                  |
| pickle_dict             | 31.4 us                                                | 28.3 us: 1.11x faster                                  |
| pickle_list             | 4.17 us                                                | 4.50 us: 1.08x slower                                  |
| pickle_pure_python      | 304 us                                                 | 453 us: 1.49x slower                                   |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 943 ms: 1.36x slower                                   |
| pprint_pformat          | 1.44 sec                                               | 1.97 sec: 1.37x slower                                 |
| pycparser               | 1.17 sec                                               | 1.51 sec: 1.29x slower                                 |
| pyflate                 | 417 ms                                                 | 675 ms: 1.62x slower                                   |
| pylint                  | 463 ms                                                 | 519 ms: 1.12x slower                                   |
| python_startup          | 8.36 ms                                                | 13.9 ms: 1.67x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 5.76 ms: 1.03x faster                                  |
| raytrace                | 290 ms                                                 | 461 ms: 1.59x slower                                   |
| regex_compile           | 136 ms                                                 | 174 ms: 1.28x slower                                   |
| regex_dna               | 203 ms                                                 | 214 ms: 1.05x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.21 ms: 1.05x faster                                  |
| regex_v8                | 22.3 ms                                                | 25.0 ms: 1.12x slower                                  |
| richards                | 46.2 ms                                                | 71.4 ms: 1.55x slower                                  |
| scimark_fft             | 329 ms                                                 | 414 ms: 1.26x slower                                   |
| scimark_lu              | 107 ms                                                 | 158 ms: 1.47x slower                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 105 ms: 1.53x slower                                   |
| scimark_sor             | 115 ms                                                 | 193 ms: 1.68x slower                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 5.48 ms: 1.25x slower                                  |
| spectral_norm           | 99.9 ms                                                | 148 ms: 1.48x slower                                   |
| sqlalchemy_declarative  | 139 ms                                                 | 165 ms: 1.19x slower                                   |
| sqlalchemy_imperative   | 18.0 ms                                                | 21.0 ms: 1.17x slower                                  |
| sqlglot_parse           | 1.37 ms                                                | 2.04 ms: 1.49x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 2.42 ms: 1.46x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 65.3 ms: 1.23x slower                                  |
| sqlglot_normalize       | 108 ms                                                 | 135 ms: 1.25x slower                                   |
| sqlite_synth            | 2.49 us                                                | 2.90 us: 1.17x slower                                  |
| sympy_expand            | 472 ms                                                 | 537 ms: 1.14x slower                                   |
| sympy_integrate         | 20.9 ms                                                | 23.9 ms: 1.15x slower                                  |
| sympy_sum               | 166 ms                                                 | 183 ms: 1.11x slower                                   |
| sympy_str               | 287 ms                                                 | 324 ms: 1.13x slower                                   |
| telco                   | 6.62 ms                                                | 6.68 ms: 1.01x slower                                  |
| thrift                  | 752 us                                                 | 1.03 ms: 1.37x slower                                  |
| tornado_http            | 96.6 ms                                                | 128 ms: 1.33x slower                                   |
| unpack_sequence         | 43.4 ns                                                | 59.5 ns: 1.37x slower                                  |
| unpickle                | 13.3 us                                                | 14.3 us: 1.08x slower                                  |
| unpickle_list           | 4.95 us                                                | 4.99 us: 1.01x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 297 us: 1.32x slower                                   |
| xml_etree_parse         | 158 ms                                                 | 163 ms: 1.03x slower                                   |
| xml_etree_iterparse     | 103 ms                                                 | 110 ms: 1.07x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 93.3 ms: 1.22x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 74.5 ms: 1.38x slower                                  |
| Geometric mean          | (ref)                                                  | 1.26x slower                                           |

Benchmark hidden because not significant (1): bench_mp_pool
