
# Results vs. 3.10.4

- fork: python
- ref: v3.11.0
- machine: linux-x86_64
- commit hash: deaf509
- commit date: 2022-10-24
- overall geometric mean: 1.26x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 257 ms: 1.29x faster                                   |
| chameleon      | 8.86 ms                                                | 6.41 ms: 1.38x faster                                  |
| docutils       | 3.18 sec                                               | 2.60 sec: 1.23x faster                                 |
| html5lib       | 85.8 ms                                                | 63.2 ms: 1.36x faster                                  |
| tornado_http   | 128 ms                                                 | 96.6 ms: 1.33x faster                                  |
| Geometric mean | (ref)                                                  | 1.32x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 136 ms                                                 | 95.0 ms: 1.43x faster                                  |
| float          | 108 ms                                                 | 76.3 ms: 1.41x faster                                  |
| pidigits       | 190 ms                                                 | 199 ms: 1.05x slower                                   |
| Geometric mean | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 136 ms: 1.28x faster                                   |
| regex_v8       | 25.0 ms                                                | 22.3 ms: 1.12x faster                                  |
| regex_dna      | 214 ms                                                 | 203 ms: 1.05x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.36 ms: 1.05x slower                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 304 us: 1.49x faster                                   |
| xml_etree_process    | 74.5 ms                                                | 53.8 ms: 1.38x faster                                  |
| unpickle_pure_python | 297 us                                                 | 225 us: 1.32x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.2 ms: 1.22x faster                                  |
| json_loads           | 28.9 us                                                | 26.2 us: 1.10x faster                                  |
| pickle_list          | 4.50 us                                                | 4.17 us: 1.08x faster                                  |
| unpickle             | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| json_dumps           | 13.5 ms                                                | 12.7 ms: 1.06x faster                                  |
| pickle               | 10.1 us                                                | 9.79 us: 1.03x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 158 ms: 1.03x faster                                   |
| unpickle_list        | 4.99 us                                                | 4.95 us: 1.01x faster                                  |
| pickle_dict          | 28.3 us                                                | 31.4 us: 1.11x slower                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.36 ms: 1.67x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 5.96 ms: 1.03x slower                                  |
| Geometric mean         | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 14.3 ms                                                | 9.85 ms: 1.45x faster                                  |
| django_template | 46.3 ms                                                | 32.5 ms: 1.43x faster                                  |
| genshi_text     | 30.6 ms                                                | 22.1 ms: 1.39x faster                                  |
| genshi_xml      | 63.6 ms                                                | 52.1 ms: 1.22x faster                                  |
| Geometric mean  | (ref)                                                  | 1.37x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.64 ms: 2.03x faster                                  |
| logging_silent          | 173 ns                                                 | 98.5 ns: 1.76x faster                                  |
| scimark_sor             | 193 ms                                                 | 115 ms: 1.68x faster                                   |
| python_startup          | 13.9 ms                                                | 8.36 ms: 1.67x faster                                  |
| pyflate                 | 675 ms                                                 | 417 ms: 1.62x faster                                   |
| crypto_pyaes            | 118 ms                                                 | 73.9 ms: 1.59x faster                                  |
| raytrace                | 461 ms                                                 | 290 ms: 1.59x faster                                   |
| go                      | 226 ms                                                 | 143 ms: 1.58x faster                                   |
| richards                | 71.4 ms                                                | 46.2 ms: 1.55x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 68.3 ms: 1.53x faster                                  |
| chaos                   | 104 ms                                                 | 68.6 ms: 1.52x faster                                  |
| mypy                    | 1.01 sec                                               | 669 ms: 1.52x faster                                   |
| pickle_pure_python      | 453 us                                                 | 304 us: 1.49x faster                                   |
| sqlglot_parse           | 2.04 ms                                                | 1.37 ms: 1.49x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.35 ms: 1.48x faster                                  |
| spectral_norm           | 148 ms                                                 | 99.9 ms: 1.48x faster                                  |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.47x faster                                   |
| sqlglot_transpile       | 2.42 ms                                                | 1.66 ms: 1.46x faster                                  |
| mako                    | 14.3 ms                                                | 9.85 ms: 1.45x faster                                  |
| nbody                   | 136 ms                                                 | 95.0 ms: 1.43x faster                                  |
| django_template         | 46.3 ms                                                | 32.5 ms: 1.43x faster                                  |
| float                   | 108 ms                                                 | 76.3 ms: 1.41x faster                                  |
| genshi_text             | 30.6 ms                                                | 22.1 ms: 1.39x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.8 ms: 1.38x faster                                  |
| chameleon               | 8.86 ms                                                | 6.41 ms: 1.38x faster                                  |
| thrift                  | 1.03 ms                                                | 752 us: 1.37x faster                                   |
| deepcopy_memo           | 50.0 us                                                | 36.4 us: 1.37x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 43.4 ns: 1.37x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.44 sec: 1.37x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 625 ms: 1.37x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 691 ms: 1.36x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.36x faster                                 |
| html5lib                | 85.8 ms                                                | 63.2 ms: 1.36x faster                                  |
| logging_format          | 8.92 us                                                | 6.62 us: 1.35x faster                                  |
| async_tree_none         | 713 ms                                                 | 529 ms: 1.35x faster                                   |
| logging_simple          | 8.06 us                                                | 6.06 us: 1.33x faster                                  |
| tornado_http            | 128 ms                                                 | 96.6 ms: 1.33x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 225 us: 1.32x faster                                   |
| 2to3                    | 332 ms                                                 | 257 ms: 1.29x faster                                   |
| pycparser               | 1.51 sec                                               | 1.17 sec: 1.29x faster                                 |
| regex_compile           | 174 ms                                                 | 136 ms: 1.28x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.05 ms: 1.28x faster                                  |
| gunicorn                | 1.43 ms                                                | 1.12 ms: 1.28x faster                                  |
| deepcopy_reduce         | 3.75 us                                                | 2.97 us: 1.26x faster                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 752 ms: 1.26x faster                                   |
| scimark_fft             | 414 ms                                                 | 329 ms: 1.26x faster                                   |
| sqlglot_normalize       | 135 ms                                                 | 108 ms: 1.25x faster                                   |
| deepcopy                | 429 us                                                 | 344 us: 1.25x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.40 ms: 1.25x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 53.0 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 388 ms: 1.23x faster                                   |
| docutils                | 3.18 sec                                               | 2.60 sec: 1.23x faster                                 |
| xml_etree_generate      | 93.3 ms                                                | 76.2 ms: 1.22x faster                                  |
| genshi_xml              | 63.6 ms                                                | 52.1 ms: 1.22x faster                                  |
| coroutines              | 31.7 ms                                                | 26.1 ms: 1.21x faster                                  |
| sqlalchemy_declarative  | 165 ms                                                 | 139 ms: 1.19x faster                                   |
| async_generators        | 428 ms                                                 | 359 ms: 1.19x faster                                   |
| flaskblogging           | 8.38 ms                                                | 7.08 ms: 1.18x faster                                  |
| dulwich_log             | 75.5 ms                                                | 63.9 ms: 1.18x faster                                  |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.0 ms: 1.17x faster                                  |
| nqueens                 | 99.3 ms                                                | 85.0 ms: 1.17x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.49 us: 1.17x faster                                  |
| bench_thread_pool       | 943 us                                                 | 810 us: 1.16x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.9 ms: 1.15x faster                                  |
| sympy_expand            | 537 ms                                                 | 472 ms: 1.14x faster                                   |
| sympy_str               | 324 ms                                                 | 287 ms: 1.13x faster                                   |
| pylint                  | 519 ms                                                 | 463 ms: 1.12x faster                                   |
| regex_v8                | 25.0 ms                                                | 22.3 ms: 1.12x faster                                  |
| sympy_sum               | 183 ms                                                 | 166 ms: 1.11x faster                                   |
| pathlib                 | 20.0 ms                                                | 18.2 ms: 1.10x faster                                  |
| json_loads              | 28.9 us                                                | 26.2 us: 1.10x faster                                  |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.09x faster                                   |
| json                    | 5.35 ms                                                | 4.95 ms: 1.08x faster                                  |
| pickle_list             | 4.50 us                                                | 4.17 us: 1.08x faster                                  |
| mdp                     | 2.82 sec                                               | 2.62 sec: 1.08x faster                                 |
| unpickle                | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| json_dumps              | 13.5 ms                                                | 12.7 ms: 1.06x faster                                  |
| regex_dna               | 214 ms                                                 | 203 ms: 1.05x faster                                   |
| generators              | 75.8 ms                                                | 72.2 ms: 1.05x faster                                  |
| pickle                  | 10.1 us                                                | 9.79 us: 1.03x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 158 ms: 1.03x faster                                   |
| telco                   | 6.68 ms                                                | 6.62 ms: 1.01x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.95 us: 1.01x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 5.96 ms: 1.03x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.36 ms: 1.05x slower                                  |
| pidigits                | 190 ms                                                 | 199 ms: 1.05x slower                                   |
| pickle_dict             | 28.3 us                                                | 31.4 us: 1.11x slower                                  |
| coverage                | 75.3 ms                                                | 101 ms: 1.33x slower                                   |
| Geometric mean          | (ref)                                                  | 1.26x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
