Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 246 ms: 1.35x faster                                   |
| chameleon      | 8.86 ms                                                | 6.49 ms: 1.36x faster                                  |
| html5lib       | 85.8 ms                                                | 58.9 ms: 1.46x faster                                  |
| tornado_http   | 128 ms                                                 | 92.5 ms: 1.39x faster                                  |
| Geometric mean | (ref)                                                  | 1.39x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 73.3 ms: 1.47x faster                                  |
| nbody          | 136 ms                                                 | 93.4 ms: 1.46x faster                                  |
| pidigits       | 190 ms                                                 | 197 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna      | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.64 ms: 1.13x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.2 ms: 1.12x faster                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.44 ms: 1.43x faster                                  |
| json_loads           | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.0 us: 1.01x faster                                  |
| pickle_dict          | 28.3 us                                                | 31.1 us: 1.10x slower                                  |
| pickle_list          | 4.50 us                                                | 4.14 us: 1.09x faster                                  |
| pickle_pure_python   | 453 us                                                 | 281 us: 1.61x faster                                   |
| unpickle             | 14.3 us                                                | 13.3 us: 1.07x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.91 us: 1.02x faster                                  |
| unpickle_pure_python | 297 us                                                 | 200 us: 1.48x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 149 ms: 1.09x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.8 ms: 1.21x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.0 ms: 1.41x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.52 ms: 1.64x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.24 ms: 1.08x slower                                  |
| Geometric mean         | (ref)                                                  | 1.23x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.5 ms: 1.42x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.3 ms: 1.44x faster                                  |
| genshi_xml      | 63.6 ms                                                | 46.8 ms: 1.36x faster                                  |
| mako            | 14.3 ms                                                | 9.70 ms: 1.47x faster                                  |
| Geometric mean  | (ref)                                                  | 1.42x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 246 ms: 1.35x faster                                   |
| aiohttp                 | 1.34 ms                                                | 998 us: 1.34x faster                                   |
| async_tree_none         | 713 ms                                                 | 528 ms: 1.35x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 731 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 646 ms: 1.32x faster                                   |
| chameleon               | 8.86 ms                                                | 6.49 ms: 1.36x faster                                  |
| chaos                   | 104 ms                                                 | 67.0 ms: 1.55x faster                                  |
| coroutines              | 31.7 ms                                                | 24.1 ms: 1.31x faster                                  |
| coverage                | 75.3 ms                                                | 99.8 ms: 1.32x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 75.1 ms: 1.56x faster                                  |
| deepcopy                | 429 us                                                 | 332 us: 1.29x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.90 us: 1.29x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.0 us: 1.47x faster                                  |
| deltablue               | 7.39 ms                                                | 3.22 ms: 2.29x faster                                  |
| django_template         | 46.3 ms                                                | 32.5 ms: 1.42x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.1 ms: 1.24x faster                                  |
| fannkuch                | 477 ms                                                 | 374 ms: 1.28x faster                                   |
| float                   | 108 ms                                                 | 73.3 ms: 1.47x faster                                  |
| generators              | 75.8 ms                                                | 79.6 ms: 1.05x slower                                  |
| genshi_text             | 30.6 ms                                                | 21.3 ms: 1.44x faster                                  |
| genshi_xml              | 63.6 ms                                                | 46.8 ms: 1.36x faster                                  |
| go                      | 226 ms                                                 | 135 ms: 1.68x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.13 ms: 1.54x faster                                  |
| html5lib                | 85.8 ms                                                | 58.9 ms: 1.46x faster                                  |
| json                    | 5.35 ms                                                | 4.71 ms: 1.14x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.44 ms: 1.43x faster                                  |
| json_loads              | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.34 us: 1.41x faster                                  |
| logging_silent          | 173 ns                                                 | 91.8 ns: 1.89x faster                                  |
| logging_simple          | 8.06 us                                                | 5.77 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.70 ms: 1.47x faster                                  |
| mdp                     | 2.82 sec                                               | 2.47 sec: 1.14x faster                                 |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.09x faster                                   |
| mypy                    | 1.01 sec                                               | 798 ms: 1.27x faster                                   |
| nbody                   | 136 ms                                                 | 93.4 ms: 1.46x faster                                  |
| nqueens                 | 99.3 ms                                                | 81.1 ms: 1.22x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.5 ms: 1.14x faster                                  |
| pickle                  | 10.1 us                                                | 10.0 us: 1.01x faster                                  |
| pickle_dict             | 28.3 us                                                | 31.1 us: 1.10x slower                                  |
| pickle_list             | 4.50 us                                                | 4.14 us: 1.09x faster                                  |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.61x faster                                   |
| pidigits                | 190 ms                                                 | 197 ms: 1.04x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 688 ms: 1.37x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.41 sec: 1.39x faster                                 |
| pycparser               | 1.51 sec                                               | 1.11 sec: 1.36x faster                                 |
| pyflate                 | 675 ms                                                 | 402 ms: 1.68x faster                                   |
| python_startup          | 13.9 ms                                                | 8.52 ms: 1.64x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.24 ms: 1.08x slower                                  |
| raytrace                | 461 ms                                                 | 281 ms: 1.64x faster                                   |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna               | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.64 ms: 1.13x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.2 ms: 1.12x faster                                  |
| richards                | 71.4 ms                                                | 41.7 ms: 1.71x faster                                  |
| scimark_fft             | 414 ms                                                 | 309 ms: 1.34x faster                                   |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.47x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.5 ms: 1.60x faster                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.86x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.16 ms: 1.32x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.2 ms: 1.56x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.35 ms: 1.51x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.64 ms: 1.48x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.5 ms: 1.29x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.65 us: 1.10x faster                                  |
| sympy_expand            | 537 ms                                                 | 458 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 164 ms: 1.12x faster                                   |
| sympy_str               | 324 ms                                                 | 283 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.32 ms: 1.06x faster                                  |
| thrift                  | 1.03 ms                                                | 745 us: 1.38x faster                                   |
| tornado_http            | 128 ms                                                 | 92.5 ms: 1.39x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 44.2 ns: 1.34x faster                                  |
| unpickle                | 14.3 us                                                | 13.3 us: 1.07x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.91 us: 1.02x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 200 us: 1.48x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 149 ms: 1.09x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.8 ms: 1.21x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.0 ms: 1.41x faster                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                           |
Ignored benchmarks (8) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
