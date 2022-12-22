Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| chameleon      | 8.86 ms                                                | 6.60 ms: 1.34x faster                                  |
| html5lib       | 85.8 ms                                                | 59.1 ms: 1.45x faster                                  |
| tornado_http   | 128 ms                                                 | 93.1 ms: 1.38x faster                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.5 ms: 1.49x faster                                  |
| nbody          | 136 ms                                                 | 93.9 ms: 1.45x faster                                  |
| pidigits       | 190 ms                                                 | 199 ms: 1.05x slower                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 130 ms: 1.33x faster                                   |
| regex_dna      | 214 ms                                                 | 209 ms: 1.02x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.66 ms: 1.14x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.7 ms: 1.10x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.49 ms: 1.42x faster                                  |
| json_loads           | 28.9 us                                                | 23.5 us: 1.23x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.0 us: 1.09x slower                                  |
| pickle_list          | 4.50 us                                                | 3.96 us: 1.14x faster                                  |
| pickle_pure_python   | 453 us                                                 | 289 us: 1.57x faster                                   |
| unpickle             | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| unpickle_pure_python | 297 us                                                 | 203 us: 1.46x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.5 ms: 1.23x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.1 ms: 1.40x faster                                  |
| Geometric mean       | (ref)                                                  | 1.19x faster                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.37 ms: 1.67x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.06 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.6 ms: 1.42x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| genshi_xml      | 63.6 ms                                                | 49.7 ms: 1.28x faster                                  |
| mako            | 14.3 ms                                                | 9.75 ms: 1.46x faster                                  |
| Geometric mean  | (ref)                                                  | 1.40x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                  |
| async_tree_none         | 713 ms                                                 | 530 ms: 1.35x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 732 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.33 sec: 1.34x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 670 ms: 1.27x faster                                   |
| chameleon               | 8.86 ms                                                | 6.60 ms: 1.34x faster                                  |
| chaos                   | 104 ms                                                 | 69.7 ms: 1.49x faster                                  |
| coroutines              | 31.7 ms                                                | 24.4 ms: 1.30x faster                                  |
| coverage                | 75.3 ms                                                | 97.8 ms: 1.30x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 76.4 ms: 1.54x faster                                  |
| deepcopy                | 429 us                                                 | 331 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.89 us: 1.30x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.1 us: 1.47x faster                                  |
| deltablue               | 7.39 ms                                                | 3.30 ms: 2.24x faster                                  |
| django_template         | 46.3 ms                                                | 32.6 ms: 1.42x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.3 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 371 ms: 1.29x faster                                   |
| float                   | 108 ms                                                 | 72.5 ms: 1.49x faster                                  |
| generators              | 75.8 ms                                                | 70.6 ms: 1.07x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| genshi_xml              | 63.6 ms                                                | 49.7 ms: 1.28x faster                                  |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.07 ms: 1.55x faster                                  |
| html5lib                | 85.8 ms                                                | 59.1 ms: 1.45x faster                                  |
| json                    | 5.35 ms                                                | 4.58 ms: 1.17x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.49 ms: 1.42x faster                                  |
| json_loads              | 28.9 us                                                | 23.5 us: 1.23x faster                                  |
| logging_format          | 8.92 us                                                | 6.47 us: 1.38x faster                                  |
| logging_silent          | 173 ns                                                 | 90.5 ns: 1.91x faster                                  |
| logging_simple          | 8.06 us                                                | 5.84 us: 1.38x faster                                  |
| mako                    | 14.3 ms                                                | 9.75 ms: 1.46x faster                                  |
| mdp                     | 2.82 sec                                               | 2.48 sec: 1.14x faster                                 |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                   |
| mypy                    | 1.01 sec                                               | 799 ms: 1.27x faster                                   |
| nbody                   | 136 ms                                                 | 93.9 ms: 1.45x faster                                  |
| nqueens                 | 99.3 ms                                                | 80.3 ms: 1.24x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.0 us: 1.09x slower                                  |
| pickle_list             | 4.50 us                                                | 3.96 us: 1.14x faster                                  |
| pickle_pure_python      | 453 us                                                 | 289 us: 1.57x faster                                   |
| pidigits                | 190 ms                                                 | 199 ms: 1.05x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 678 ms: 1.39x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.38 sec: 1.43x faster                                 |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.39x faster                                 |
| pyflate                 | 675 ms                                                 | 400 ms: 1.69x faster                                   |
| pylint                  | 519 ms                                                 | 455 ms: 1.14x faster                                   |
| python_startup          | 13.9 ms                                                | 8.37 ms: 1.67x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.06 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 287 ms: 1.61x faster                                   |
| regex_compile           | 174 ms                                                 | 130 ms: 1.33x faster                                   |
| regex_dna               | 214 ms                                                 | 209 ms: 1.02x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.66 ms: 1.14x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.7 ms: 1.10x faster                                  |
| richards                | 71.4 ms                                                | 43.5 ms: 1.64x faster                                  |
| scimark_fft             | 414 ms                                                 | 317 ms: 1.31x faster                                   |
| scimark_lu              | 158 ms                                                 | 109 ms: 1.46x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 66.6 ms: 1.57x faster                                  |
| scimark_sor             | 193 ms                                                 | 105 ms: 1.85x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.22 ms: 1.30x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.1 ms: 1.56x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.33 ms: 1.53x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.63 ms: 1.48x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.6 ms: 1.27x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.28x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.61 us: 1.11x faster                                  |
| sympy_expand            | 537 ms                                                 | 454 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 164 ms: 1.12x faster                                   |
| sympy_str               | 324 ms                                                 | 282 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.54 ms: 1.02x faster                                  |
| thrift                  | 1.03 ms                                                | 739 us: 1.40x faster                                   |
| tornado_http            | 128 ms                                                 | 93.1 ms: 1.38x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 48.7 ns: 1.22x faster                                  |
| unpickle                | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 203 us: 1.46x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.5 ms: 1.23x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.1 ms: 1.40x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (7) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
