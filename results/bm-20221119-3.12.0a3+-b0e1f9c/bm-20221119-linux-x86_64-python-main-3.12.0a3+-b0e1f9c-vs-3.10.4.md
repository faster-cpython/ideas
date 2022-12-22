Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 245 ms: 1.36x faster                                   |
| chameleon      | 8.86 ms                                                | 6.49 ms: 1.36x faster                                  |
| html5lib       | 85.8 ms                                                | 59.1 ms: 1.45x faster                                  |
| tornado_http   | 128 ms                                                 | 92.7 ms: 1.38x faster                                  |
| Geometric mean | (ref)                                                  | 1.39x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 71.6 ms: 1.50x faster                                  |
| nbody          | 136 ms                                                 | 94.1 ms: 1.45x faster                                  |
| pidigits       | 190 ms                                                 | 192 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna      | 214 ms                                                 | 213 ms: 1.01x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.77 ms: 1.18x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.2 ms: 1.13x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.42 ms: 1.43x faster                                  |
| json_loads           | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.2 us: 1.01x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.0 us: 1.09x slower                                  |
| pickle_list          | 4.50 us                                                | 4.11 us: 1.09x faster                                  |
| pickle_pure_python   | 453 us                                                 | 283 us: 1.60x faster                                   |
| unpickle             | 14.3 us                                                | 13.6 us: 1.05x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.10 us: 1.02x slower                                  |
| unpickle_pure_python | 297 us                                                 | 201 us: 1.48x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.4 ms: 1.22x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 52.9 ms: 1.41x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.51 ms: 1.64x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.25 ms: 1.08x slower                                  |
| Geometric mean         | (ref)                                                  | 1.23x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.6 ms: 1.42x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.4 ms: 1.50x faster                                  |
| genshi_xml      | 63.6 ms                                                | 46.2 ms: 1.38x faster                                  |
| mako            | 14.3 ms                                                | 9.94 ms: 1.43x faster                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 245 ms: 1.36x faster                                   |
| aiohttp                 | 1.34 ms                                                | 999 us: 1.34x faster                                   |
| async_tree_none         | 713 ms                                                 | 527 ms: 1.35x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 729 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 665 ms: 1.28x faster                                   |
| chameleon               | 8.86 ms                                                | 6.49 ms: 1.36x faster                                  |
| chaos                   | 104 ms                                                 | 66.0 ms: 1.58x faster                                  |
| coroutines              | 31.7 ms                                                | 24.8 ms: 1.28x faster                                  |
| coverage                | 75.3 ms                                                | 98.2 ms: 1.30x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 74.3 ms: 1.58x faster                                  |
| deepcopy                | 429 us                                                 | 330 us: 1.30x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.98 us: 1.26x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.2 us: 1.46x faster                                  |
| deltablue               | 7.39 ms                                                | 3.23 ms: 2.29x faster                                  |
| django_template         | 46.3 ms                                                | 32.6 ms: 1.42x faster                                  |
| dulwich_log             | 75.5 ms                                                | 60.6 ms: 1.25x faster                                  |
| fannkuch                | 477 ms                                                 | 369 ms: 1.29x faster                                   |
| float                   | 108 ms                                                 | 71.6 ms: 1.50x faster                                  |
| generators              | 75.8 ms                                                | 78.0 ms: 1.03x slower                                  |
| genshi_text             | 30.6 ms                                                | 20.4 ms: 1.50x faster                                  |
| genshi_xml              | 63.6 ms                                                | 46.2 ms: 1.38x faster                                  |
| go                      | 226 ms                                                 | 135 ms: 1.67x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.21 ms: 1.52x faster                                  |
| html5lib                | 85.8 ms                                                | 59.1 ms: 1.45x faster                                  |
| json                    | 5.35 ms                                                | 4.67 ms: 1.15x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.42 ms: 1.43x faster                                  |
| json_loads              | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.35 us: 1.41x faster                                  |
| logging_silent          | 173 ns                                                 | 91.1 ns: 1.90x faster                                  |
| logging_simple          | 8.06 us                                                | 5.77 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.94 ms: 1.43x faster                                  |
| mdp                     | 2.82 sec                                               | 2.65 sec: 1.07x faster                                 |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.10x faster                                   |
| mypy                    | 1.01 sec                                               | 795 ms: 1.28x faster                                   |
| nbody                   | 136 ms                                                 | 94.1 ms: 1.45x faster                                  |
| nqueens                 | 99.3 ms                                                | 81.5 ms: 1.22x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.5 ms: 1.14x faster                                  |
| pickle                  | 10.1 us                                                | 10.2 us: 1.01x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.0 us: 1.09x slower                                  |
| pickle_list             | 4.50 us                                                | 4.11 us: 1.09x faster                                  |
| pickle_pure_python      | 453 us                                                 | 283 us: 1.60x faster                                   |
| pidigits                | 190 ms                                                 | 192 ms: 1.01x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 673 ms: 1.40x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.38 sec: 1.43x faster                                 |
| pycparser               | 1.51 sec                                               | 1.12 sec: 1.35x faster                                 |
| pyflate                 | 675 ms                                                 | 403 ms: 1.68x faster                                   |
| python_startup          | 13.9 ms                                                | 8.51 ms: 1.64x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.25 ms: 1.08x slower                                  |
| raytrace                | 461 ms                                                 | 278 ms: 1.66x faster                                   |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna               | 214 ms                                                 | 213 ms: 1.01x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.77 ms: 1.18x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.2 ms: 1.13x faster                                  |
| richards                | 71.4 ms                                                | 41.6 ms: 1.72x faster                                  |
| scimark_fft             | 414 ms                                                 | 303 ms: 1.37x faster                                   |
| scimark_lu              | 158 ms                                                 | 104 ms: 1.52x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.0 ms: 1.64x faster                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.85x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.96 ms: 1.38x faster                                  |
| spectral_norm           | 148 ms                                                 | 97.6 ms: 1.52x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.33 ms: 1.53x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.61 ms: 1.50x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 50.7 ms: 1.29x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.64 us: 1.10x faster                                  |
| sympy_expand            | 537 ms                                                 | 457 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 165 ms: 1.11x faster                                   |
| sympy_str               | 324 ms                                                 | 283 ms: 1.14x faster                                   |
| telco                   | 6.68 ms                                                | 6.27 ms: 1.07x faster                                  |
| thrift                  | 1.03 ms                                                | 746 us: 1.38x faster                                   |
| tornado_http            | 128 ms                                                 | 92.7 ms: 1.38x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 42.9 ns: 1.39x faster                                  |
| unpickle                | 14.3 us                                                | 13.6 us: 1.05x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.10 us: 1.02x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 201 us: 1.48x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.4 ms: 1.22x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 52.9 ms: 1.41x faster                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                           |
Ignored benchmarks (8) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
