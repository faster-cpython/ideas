Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.71 ms: 1.32x faster                                  |
| html5lib       | 85.8 ms                                                | 59.2 ms: 1.45x faster                                  |
| tornado_http   | 128 ms                                                 | 92.6 ms: 1.38x faster                                  |
| Geometric mean | (ref)                                                  | 1.37x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.2 ms: 1.49x faster                                  |
| nbody          | 136 ms                                                 | 94.2 ms: 1.45x faster                                  |
| pidigits       | 190 ms                                                 | 199 ms: 1.05x slower                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 129 ms: 1.35x faster                                   |
| regex_dna      | 214 ms                                                 | 200 ms: 1.07x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.60 ms: 1.12x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.2 ms: 1.12x faster                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.60 ms: 1.40x faster                                  |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.1 us: 1.10x slower                                  |
| pickle_list          | 4.50 us                                                | 4.14 us: 1.09x faster                                  |
| pickle_pure_python   | 453 us                                                 | 293 us: 1.55x faster                                   |
| unpickle             | 14.3 us                                                | 12.9 us: 1.11x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.96 us: 1.01x faster                                  |
| unpickle_pure_python | 297 us                                                 | 202 us: 1.47x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 145 ms: 1.12x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.9 ms: 1.21x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.7 ms: 1.39x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.41 ms: 1.66x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.09 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.6 ms: 1.42x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| genshi_xml      | 63.6 ms                                                | 49.2 ms: 1.29x faster                                  |
| mako            | 14.3 ms                                                | 9.82 ms: 1.45x faster                                  |
| Geometric mean  | (ref)                                                  | 1.40x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| aiohttp                 | 1.34 ms                                                | 997 us: 1.34x faster                                   |
| async_tree_none         | 713 ms                                                 | 533 ms: 1.34x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 730 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 647 ms: 1.32x faster                                   |
| chameleon               | 8.86 ms                                                | 6.71 ms: 1.32x faster                                  |
| chaos                   | 104 ms                                                 | 66.1 ms: 1.58x faster                                  |
| coroutines              | 31.7 ms                                                | 24.6 ms: 1.29x faster                                  |
| coverage                | 75.3 ms                                                | 98.4 ms: 1.31x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 75.2 ms: 1.56x faster                                  |
| deepcopy                | 429 us                                                 | 332 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.91 us: 1.29x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.6 us: 1.44x faster                                  |
| deltablue               | 7.39 ms                                                | 3.31 ms: 2.23x faster                                  |
| django_template         | 46.3 ms                                                | 32.6 ms: 1.42x faster                                  |
| dulwich_log             | 75.5 ms                                                | 60.9 ms: 1.24x faster                                  |
| fannkuch                | 477 ms                                                 | 368 ms: 1.29x faster                                   |
| float                   | 108 ms                                                 | 72.2 ms: 1.49x faster                                  |
| generators              | 75.8 ms                                                | 71.8 ms: 1.05x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| genshi_xml              | 63.6 ms                                                | 49.2 ms: 1.29x faster                                  |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.05 ms: 1.56x faster                                  |
| html5lib                | 85.8 ms                                                | 59.2 ms: 1.45x faster                                  |
| json                    | 5.35 ms                                                | 4.78 ms: 1.12x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.60 ms: 1.40x faster                                  |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| logging_format          | 8.92 us                                                | 6.38 us: 1.40x faster                                  |
| logging_silent          | 173 ns                                                 | 92.9 ns: 1.86x faster                                  |
| logging_simple          | 8.06 us                                                | 5.73 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.82 ms: 1.45x faster                                  |
| mdp                     | 2.82 sec                                               | 2.54 sec: 1.11x faster                                 |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                   |
| mypy                    | 1.01 sec                                               | 801 ms: 1.27x faster                                   |
| nbody                   | 136 ms                                                 | 94.2 ms: 1.45x faster                                  |
| nqueens                 | 99.3 ms                                                | 79.5 ms: 1.25x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.1 us: 1.10x slower                                  |
| pickle_list             | 4.50 us                                                | 4.14 us: 1.09x faster                                  |
| pickle_pure_python      | 453 us                                                 | 293 us: 1.55x faster                                   |
| pidigits                | 190 ms                                                 | 199 ms: 1.05x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 669 ms: 1.41x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                 |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.38x faster                                 |
| pyflate                 | 675 ms                                                 | 402 ms: 1.68x faster                                   |
| pylint                  | 519 ms                                                 | 455 ms: 1.14x faster                                   |
| python_startup          | 13.9 ms                                                | 8.41 ms: 1.66x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.09 ms: 1.06x slower                                  |
| raytrace                | 461 ms                                                 | 285 ms: 1.62x faster                                   |
| regex_compile           | 174 ms                                                 | 129 ms: 1.35x faster                                   |
| regex_dna               | 214 ms                                                 | 200 ms: 1.07x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.60 ms: 1.12x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.2 ms: 1.12x faster                                  |
| richards                | 71.4 ms                                                | 43.0 ms: 1.66x faster                                  |
| scimark_fft             | 414 ms                                                 | 315 ms: 1.31x faster                                   |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.46x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.6 ms: 1.60x faster                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.86x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.16 ms: 1.32x faster                                  |
| spectral_norm           | 148 ms                                                 | 96.7 ms: 1.53x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.34 ms: 1.52x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.63 ms: 1.49x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.5 ms: 1.27x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.62 us: 1.11x faster                                  |
| sympy_expand            | 537 ms                                                 | 458 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                  |
| sympy_sum               | 183 ms                                                 | 163 ms: 1.12x faster                                   |
| sympy_str               | 324 ms                                                 | 281 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.46 ms: 1.03x faster                                  |
| thrift                  | 1.03 ms                                                | 742 us: 1.39x faster                                   |
| tornado_http            | 128 ms                                                 | 92.6 ms: 1.38x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 44.1 ns: 1.35x faster                                  |
| unpickle                | 14.3 us                                                | 12.9 us: 1.11x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.96 us: 1.01x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 202 us: 1.47x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 145 ms: 1.12x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.9 ms: 1.21x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.7 ms: 1.39x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |
Ignored benchmarks (7) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
