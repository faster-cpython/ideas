Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 244 ms: 1.36x faster                                                   |
| chameleon      | 8.86 ms                                                | 6.31 ms: 1.40x faster                                                  |
| docutils       | 3.18 sec                                               | 2.48 sec: 1.28x faster                                                 |
| html5lib       | 85.8 ms                                                | 59.1 ms: 1.45x faster                                                  |
| tornado_http   | 128 ms                                                 | 92.8 ms: 1.38x faster                                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 108 ms                                                 | 73.1 ms: 1.47x faster                                                  |
| nbody          | 136 ms                                                 | 93.7 ms: 1.45x faster                                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                                   |
| regex_dna      | 214 ms                                                 | 209 ms: 1.02x faster                                                   |
| regex_effbot   | 3.21 ms                                                | 3.55 ms: 1.11x slower                                                  |
| regex_v8       | 25.0 ms                                                | 21.0 ms: 1.19x faster                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.51 ms: 1.42x faster                                                  |
| json_loads           | 28.9 us                                                | 23.8 us: 1.21x faster                                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.02x slower                                                  |
| pickle_dict          | 28.3 us                                                | 31.3 us: 1.11x slower                                                  |
| pickle_list          | 4.50 us                                                | 3.97 us: 1.13x faster                                                  |
| pickle_pure_python   | 453 us                                                 | 281 us: 1.62x faster                                                   |
| unpickle             | 14.3 us                                                | 13.6 us: 1.05x faster                                                  |
| unpickle_list        | 4.99 us                                                | 5.13 us: 1.03x slower                                                  |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.49x faster                                                   |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.09x faster                                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.3 ms: 1.22x faster                                                  |
| xml_etree_process    | 74.5 ms                                                | 52.8 ms: 1.41x faster                                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.48 ms: 1.64x faster                                                  |
| python_startup_no_site | 5.76 ms                                                | 6.12 ms: 1.06x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.1 ms: 1.44x faster                                                  |
| genshi_text     | 30.6 ms                                                | 20.2 ms: 1.52x faster                                                  |
| genshi_xml      | 63.6 ms                                                | 46.6 ms: 1.36x faster                                                  |
| mako            | 14.3 ms                                                | 9.56 ms: 1.49x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.45x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 244 ms: 1.36x faster                                                   |
| aiohttp                 | 1.34 ms                                                | 991 us: 1.35x faster                                                   |
| async_generators        | 428 ms                                                 | 358 ms: 1.19x faster                                                   |
| async_tree_none         | 713 ms                                                 | 530 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 755 ms: 1.26x faster                                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                                 |
| async_tree_memoization  | 854 ms                                                 | 622 ms: 1.37x faster                                                   |
| chameleon               | 8.86 ms                                                | 6.31 ms: 1.40x faster                                                  |
| chaos                   | 104 ms                                                 | 65.6 ms: 1.59x faster                                                  |
| bench_thread_pool       | 943 us                                                 | 774 us: 1.22x faster                                                   |
| coroutines              | 31.7 ms                                                | 24.5 ms: 1.29x faster                                                  |
| coverage                | 75.3 ms                                                | 102 ms: 1.35x slower                                                   |
| crypto_pyaes            | 118 ms                                                 | 75.1 ms: 1.57x faster                                                  |
| deepcopy                | 429 us                                                 | 330 us: 1.30x faster                                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.99 us: 1.26x faster                                                  |
| deepcopy_memo           | 50.0 us                                                | 33.8 us: 1.48x faster                                                  |
| deltablue               | 7.39 ms                                                | 3.17 ms: 2.34x faster                                                  |
| django_template         | 46.3 ms                                                | 32.1 ms: 1.44x faster                                                  |
| docutils                | 3.18 sec                                               | 2.48 sec: 1.28x faster                                                 |
| dulwich_log             | 75.5 ms                                                | 61.5 ms: 1.23x faster                                                  |
| fannkuch                | 477 ms                                                 | 373 ms: 1.28x faster                                                   |
| float                   | 108 ms                                                 | 73.1 ms: 1.47x faster                                                  |
| generators              | 75.8 ms                                                | 77.7 ms: 1.03x slower                                                  |
| genshi_text             | 30.6 ms                                                | 20.2 ms: 1.52x faster                                                  |
| genshi_xml              | 63.6 ms                                                | 46.6 ms: 1.36x faster                                                  |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                                   |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                                  |
| hexiom                  | 9.42 ms                                                | 6.18 ms: 1.52x faster                                                  |
| html5lib                | 85.8 ms                                                | 59.1 ms: 1.45x faster                                                  |
| json                    | 5.35 ms                                                | 4.61 ms: 1.16x faster                                                  |
| json_dumps              | 13.5 ms                                                | 9.51 ms: 1.42x faster                                                  |
| json_loads              | 28.9 us                                                | 23.8 us: 1.21x faster                                                  |
| logging_format          | 8.92 us                                                | 6.29 us: 1.42x faster                                                  |
| logging_silent          | 173 ns                                                 | 94.1 ns: 1.84x faster                                                  |
| logging_simple          | 8.06 us                                                | 5.62 us: 1.43x faster                                                  |
| mako                    | 14.3 ms                                                | 9.56 ms: 1.49x faster                                                  |
| mdp                     | 2.82 sec                                               | 2.69 sec: 1.05x faster                                                 |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.12x faster                                                   |
| mypy                    | 1.01 sec                                               | 798 ms: 1.27x faster                                                   |
| nbody                   | 136 ms                                                 | 93.7 ms: 1.45x faster                                                  |
| nqueens                 | 99.3 ms                                                | 82.0 ms: 1.21x faster                                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                                  |
| pickle                  | 10.1 us                                                | 10.4 us: 1.02x slower                                                  |
| pickle_dict             | 28.3 us                                                | 31.3 us: 1.11x slower                                                  |
| pickle_list             | 4.50 us                                                | 3.97 us: 1.13x faster                                                  |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.62x faster                                                   |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                                   |
| pprint_safe_repr        | 943 ms                                                 | 676 ms: 1.39x faster                                                   |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                                 |
| pycparser               | 1.51 sec                                               | 1.07 sec: 1.42x faster                                                 |
| pyflate                 | 675 ms                                                 | 397 ms: 1.70x faster                                                   |
| python_startup          | 13.9 ms                                                | 8.48 ms: 1.64x faster                                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.12 ms: 1.06x slower                                                  |
| raytrace                | 461 ms                                                 | 280 ms: 1.65x faster                                                   |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                                   |
| regex_dna               | 214 ms                                                 | 209 ms: 1.02x faster                                                   |
| regex_effbot            | 3.21 ms                                                | 3.55 ms: 1.11x slower                                                  |
| regex_v8                | 25.0 ms                                                | 21.0 ms: 1.19x faster                                                  |
| richards                | 71.4 ms                                                | 41.3 ms: 1.73x faster                                                  |
| scimark_fft             | 414 ms                                                 | 307 ms: 1.35x faster                                                   |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.49x faster                                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.0 ms: 1.61x faster                                                  |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.08 ms: 1.34x faster                                                  |
| spectral_norm           | 148 ms                                                 | 95.6 ms: 1.55x faster                                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.32 ms: 1.54x faster                                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.61 ms: 1.50x faster                                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.2 ms: 1.30x faster                                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                                   |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                                  |
| sympy_expand            | 537 ms                                                 | 454 ms: 1.18x faster                                                   |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                                  |
| sympy_sum               | 183 ms                                                 | 163 ms: 1.13x faster                                                   |
| sympy_str               | 324 ms                                                 | 280 ms: 1.16x faster                                                   |
| telco                   | 6.68 ms                                                | 6.44 ms: 1.04x faster                                                  |
| thrift                  | 1.03 ms                                                | 748 us: 1.38x faster                                                   |
| tornado_http            | 128 ms                                                 | 92.8 ms: 1.38x faster                                                  |
| unpack_sequence         | 59.5 ns                                                | 45.1 ns: 1.32x faster                                                  |
| unpickle                | 14.3 us                                                | 13.6 us: 1.05x faster                                                  |
| unpickle_list           | 4.99 us                                                | 5.13 us: 1.03x slower                                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.49x faster                                                   |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.09x faster                                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.3 ms: 1.22x faster                                                  |
| xml_etree_process       | 74.5 ms                                                | 52.8 ms: 1.41x faster                                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
