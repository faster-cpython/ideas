Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.37 ms: 1.39x faster                                  |
| html5lib       | 85.8 ms                                                | 59.5 ms: 1.44x faster                                  |
| tornado_http   | 128 ms                                                 | 93.1 ms: 1.38x faster                                  |
| Geometric mean | (ref)                                                  | 1.39x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.9 ms: 1.48x faster                                  |
| nbody          | 136 ms                                                 | 98.1 ms: 1.39x faster                                  |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_dna      | 214 ms                                                 | 210 ms: 1.02x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.69 ms: 1.15x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.9 ms: 1.09x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.31 ms: 1.45x faster                                  |
| json_loads           | 28.9 us                                                | 23.5 us: 1.23x faster                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.6 us: 1.12x slower                                  |
| pickle_list          | 4.50 us                                                | 4.16 us: 1.08x faster                                  |
| pickle_pure_python   | 453 us                                                 | 287 us: 1.58x faster                                   |
| unpickle             | 14.3 us                                                | 12.9 us: 1.10x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.97 us: 1.01x faster                                  |
| unpickle_pure_python | 297 us                                                 | 205 us: 1.44x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.1 ms: 1.23x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.1 ms: 1.40x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.37 ms: 1.66x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.08 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.0 ms: 1.45x faster                                  |
| genshi_text     | 30.6 ms                                                | 21.1 ms: 1.45x faster                                  |
| genshi_xml      | 63.6 ms                                                | 49.2 ms: 1.29x faster                                  |
| mako            | 14.3 ms                                                | 9.72 ms: 1.47x faster                                  |
| Geometric mean  | (ref)                                                  | 1.41x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                  |
| async_tree_none         | 713 ms                                                 | 536 ms: 1.33x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 737 ms: 1.29x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 638 ms: 1.34x faster                                   |
| chameleon               | 8.86 ms                                                | 6.37 ms: 1.39x faster                                  |
| chaos                   | 104 ms                                                 | 67.4 ms: 1.54x faster                                  |
| coroutines              | 31.7 ms                                                | 24.4 ms: 1.30x faster                                  |
| coverage                | 75.3 ms                                                | 97.3 ms: 1.29x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 74.7 ms: 1.57x faster                                  |
| deepcopy                | 429 us                                                 | 328 us: 1.31x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.91 us: 1.29x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.3 us: 1.46x faster                                  |
| deltablue               | 7.39 ms                                                | 3.30 ms: 2.24x faster                                  |
| django_template         | 46.3 ms                                                | 32.0 ms: 1.45x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.6 ms: 1.22x faster                                  |
| fannkuch                | 477 ms                                                 | 373 ms: 1.28x faster                                   |
| float                   | 108 ms                                                 | 72.9 ms: 1.48x faster                                  |
| generators              | 75.8 ms                                                | 72.6 ms: 1.04x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.1 ms: 1.45x faster                                  |
| genshi_xml              | 63.6 ms                                                | 49.2 ms: 1.29x faster                                  |
| go                      | 226 ms                                                 | 137 ms: 1.65x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.22 ms: 1.51x faster                                  |
| html5lib                | 85.8 ms                                                | 59.5 ms: 1.44x faster                                  |
| json                    | 5.35 ms                                                | 4.67 ms: 1.15x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.31 ms: 1.45x faster                                  |
| json_loads              | 28.9 us                                                | 23.5 us: 1.23x faster                                  |
| logging_format          | 8.92 us                                                | 6.41 us: 1.39x faster                                  |
| logging_silent          | 173 ns                                                 | 94.4 ns: 1.84x faster                                  |
| logging_simple          | 8.06 us                                                | 5.78 us: 1.39x faster                                  |
| mako                    | 14.3 ms                                                | 9.72 ms: 1.47x faster                                  |
| mdp                     | 2.82 sec                                               | 2.54 sec: 1.11x faster                                 |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                   |
| mypy                    | 1.01 sec                                               | 802 ms: 1.26x faster                                   |
| nbody                   | 136 ms                                                 | 98.1 ms: 1.39x faster                                  |
| nqueens                 | 99.3 ms                                                | 80.7 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.6 ms: 1.14x faster                                  |
| pickle                  | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.6 us: 1.12x slower                                  |
| pickle_list             | 4.50 us                                                | 4.16 us: 1.08x faster                                  |
| pickle_pure_python      | 453 us                                                 | 287 us: 1.58x faster                                   |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| pprint_safe_repr        | 943 ms                                                 | 670 ms: 1.41x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                 |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.38x faster                                 |
| pyflate                 | 675 ms                                                 | 399 ms: 1.69x faster                                   |
| pylint                  | 519 ms                                                 | 459 ms: 1.13x faster                                   |
| python_startup          | 13.9 ms                                                | 8.37 ms: 1.66x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.08 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 285 ms: 1.62x faster                                   |
| regex_compile           | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_dna               | 214 ms                                                 | 210 ms: 1.02x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.69 ms: 1.15x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.9 ms: 1.09x faster                                  |
| richards                | 71.4 ms                                                | 43.4 ms: 1.65x faster                                  |
| scimark_fft             | 414 ms                                                 | 318 ms: 1.30x faster                                   |
| scimark_lu              | 158 ms                                                 | 110 ms: 1.44x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.6 ms: 1.60x faster                                  |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.80x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.27 ms: 1.28x faster                                  |
| spectral_norm           | 148 ms                                                 | 94.1 ms: 1.57x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.34 ms: 1.52x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.63 ms: 1.48x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.5 ms: 1.27x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 106 ms: 1.28x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.64 us: 1.10x faster                                  |
| sympy_expand            | 537 ms                                                 | 457 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                  |
| sympy_sum               | 183 ms                                                 | 164 ms: 1.12x faster                                   |
| sympy_str               | 324 ms                                                 | 282 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.31 ms: 1.06x faster                                  |
| thrift                  | 1.03 ms                                                | 736 us: 1.40x faster                                   |
| tornado_http            | 128 ms                                                 | 93.1 ms: 1.38x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 46.0 ns: 1.29x faster                                  |
| unpickle                | 14.3 us                                                | 12.9 us: 1.10x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.97 us: 1.01x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 205 us: 1.44x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 147 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.1 ms: 1.23x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.1 ms: 1.40x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |
Ignored benchmarks (7) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
