Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.61 ms: 1.34x faster                                  |
| html5lib       | 85.8 ms                                                | 59.7 ms: 1.44x faster                                  |
| tornado_http   | 128 ms                                                 | 93.4 ms: 1.37x faster                                  |
| Geometric mean | (ref)                                                  | 1.37x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.3 ms: 1.49x faster                                  |
| nbody          | 136 ms                                                 | 94.6 ms: 1.44x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna      | 214 ms                                                 | 203 ms: 1.05x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.60 ms: 1.12x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.1 ms: 1.13x faster                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.44 ms: 1.43x faster                                  |
| json_loads           | 28.9 us                                                | 23.8 us: 1.21x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.9 us: 1.13x slower                                  |
| pickle_list          | 4.50 us                                                | 4.06 us: 1.11x faster                                  |
| pickle_pure_python   | 453 us                                                 | 293 us: 1.55x faster                                   |
| unpickle             | 14.3 us                                                | 13.0 us: 1.10x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python | 297 us                                                 | 204 us: 1.46x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 146 ms: 1.12x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 101 ms: 1.09x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.6 ms: 1.22x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.7 ms: 1.39x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.38 ms: 1.66x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.06 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 33.3 ms: 1.39x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.8 ms: 1.40x faster                                  |
| genshi_xml      | 63.6 ms                                                | 49.1 ms: 1.29x faster                                  |
| mako            | 14.3 ms                                                | 9.84 ms: 1.45x faster                                  |
| Geometric mean  | (ref)                                                  | 1.38x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.34x faster                                  |
| async_tree_none         | 713 ms                                                 | 530 ms: 1.34x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 731 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 646 ms: 1.32x faster                                   |
| chameleon               | 8.86 ms                                                | 6.61 ms: 1.34x faster                                  |
| chaos                   | 104 ms                                                 | 65.5 ms: 1.59x faster                                  |
| coroutines              | 31.7 ms                                                | 25.0 ms: 1.27x faster                                  |
| coverage                | 75.3 ms                                                | 98.9 ms: 1.31x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 75.3 ms: 1.56x faster                                  |
| deepcopy                | 429 us                                                 | 331 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.90 us: 1.29x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.3 us: 1.46x faster                                  |
| deltablue               | 7.39 ms                                                | 3.40 ms: 2.17x faster                                  |
| django_template         | 46.3 ms                                                | 33.3 ms: 1.39x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.1 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 362 ms: 1.32x faster                                   |
| float                   | 108 ms                                                 | 72.3 ms: 1.49x faster                                  |
| generators              | 75.8 ms                                                | 73.8 ms: 1.03x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.8 ms: 1.40x faster                                  |
| genshi_xml              | 63.6 ms                                                | 49.1 ms: 1.29x faster                                  |
| go                      | 226 ms                                                 | 138 ms: 1.64x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.02 ms: 1.56x faster                                  |
| html5lib                | 85.8 ms                                                | 59.7 ms: 1.44x faster                                  |
| json                    | 5.35 ms                                                | 4.72 ms: 1.13x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.44 ms: 1.43x faster                                  |
| json_loads              | 28.9 us                                                | 23.8 us: 1.21x faster                                  |
| logging_format          | 8.92 us                                                | 6.43 us: 1.39x faster                                  |
| logging_silent          | 173 ns                                                 | 92.7 ns: 1.87x faster                                  |
| logging_simple          | 8.06 us                                                | 5.74 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.84 ms: 1.45x faster                                  |
| mdp                     | 2.82 sec                                               | 2.59 sec: 1.09x faster                                 |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                   |
| mypy                    | 1.01 sec                                               | 799 ms: 1.27x faster                                   |
| nbody                   | 136 ms                                                 | 94.6 ms: 1.44x faster                                  |
| nqueens                 | 99.3 ms                                                | 79.2 ms: 1.25x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.9 us: 1.13x slower                                  |
| pickle_list             | 4.50 us                                                | 4.06 us: 1.11x faster                                  |
| pickle_pure_python      | 453 us                                                 | 293 us: 1.55x faster                                   |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 682 ms: 1.38x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                 |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.39x faster                                 |
| pyflate                 | 675 ms                                                 | 407 ms: 1.66x faster                                   |
| pylint                  | 519 ms                                                 | 454 ms: 1.15x faster                                   |
| python_startup          | 13.9 ms                                                | 8.38 ms: 1.66x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.06 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 284 ms: 1.62x faster                                   |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna               | 214 ms                                                 | 203 ms: 1.05x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.60 ms: 1.12x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.1 ms: 1.13x faster                                  |
| richards                | 71.4 ms                                                | 44.4 ms: 1.61x faster                                  |
| scimark_fft             | 414 ms                                                 | 316 ms: 1.31x faster                                   |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.47x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 66.3 ms: 1.58x faster                                  |
| scimark_sor             | 193 ms                                                 | 105 ms: 1.85x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.20 ms: 1.31x faster                                  |
| spectral_norm           | 148 ms                                                 | 96.4 ms: 1.54x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.34 ms: 1.52x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.64 ms: 1.47x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.4 ms: 1.27x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.29x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.60 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 456 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                  |
| sympy_sum               | 183 ms                                                 | 164 ms: 1.12x faster                                   |
| sympy_str               | 324 ms                                                 | 280 ms: 1.16x faster                                   |
| telco                   | 6.68 ms                                                | 6.32 ms: 1.06x faster                                  |
| thrift                  | 1.03 ms                                                | 737 us: 1.40x faster                                   |
| tornado_http            | 128 ms                                                 | 93.4 ms: 1.37x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 50.2 ns: 1.18x faster                                  |
| unpickle                | 14.3 us                                                | 13.0 us: 1.10x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 204 us: 1.46x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 146 ms: 1.12x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 101 ms: 1.09x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.6 ms: 1.22x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.7 ms: 1.39x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |
Ignored benchmarks (7) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
