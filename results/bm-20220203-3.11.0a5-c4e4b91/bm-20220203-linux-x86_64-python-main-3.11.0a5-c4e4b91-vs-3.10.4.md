Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 267 ms: 1.25x faster                                  |
| chameleon      | 8.86 ms                                                | 6.95 ms: 1.27x faster                                 |
| html5lib       | 85.8 ms                                                | 67.9 ms: 1.26x faster                                 |
| tornado_http   | 128 ms                                                 | 106 ms: 1.21x faster                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 77.5 ms: 1.39x faster                                 |
| nbody          | 136 ms                                                 | 94.7 ms: 1.44x faster                                 |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 140 ms: 1.24x faster                                  |
| regex_dna      | 214 ms                                                 | 213 ms: 1.01x faster                                  |
| regex_effbot   | 3.21 ms                                                | 3.14 ms: 1.02x faster                                 |
| regex_v8       | 25.0 ms                                                | 24.0 ms: 1.04x faster                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.2 ms: 1.10x faster                                 |
| json_loads           | 28.9 us                                                | 26.7 us: 1.08x faster                                 |
| pickle               | 10.1 us                                                | 9.93 us: 1.02x faster                                 |
| pickle_dict          | 28.3 us                                                | 28.1 us: 1.01x faster                                 |
| pickle_list          | 4.50 us                                                | 4.47 us: 1.01x faster                                 |
| pickle_pure_python   | 453 us                                                 | 334 us: 1.36x faster                                  |
| unpickle             | 14.3 us                                                | 13.4 us: 1.06x faster                                 |
| unpickle_list        | 4.99 us                                                | 5.26 us: 1.05x slower                                 |
| unpickle_pure_python | 297 us                                                 | 249 us: 1.19x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 153 ms: 1.07x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 106 ms: 1.04x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 79.6 ms: 1.17x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 57.0 ms: 1.31x faster                                 |
| Geometric mean       | (ref)                                                  | 1.10x faster                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.13 ms: 1.71x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 5.92 ms: 1.03x slower                                 |
| Geometric mean         | (ref)                                                  | 1.29x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 35.4 ms: 1.31x faster                                 |
| mako            | 14.3 ms                                                | 10.5 ms: 1.36x faster                                 |
| Geometric mean  | (ref)                                                  | 1.33x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 267 ms: 1.25x faster                                  |
| chameleon               | 8.86 ms                                                | 6.95 ms: 1.27x faster                                 |
| chaos                   | 104 ms                                                 | 74.9 ms: 1.39x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 83.8 ms: 1.40x faster                                 |
| deltablue               | 7.39 ms                                                | 4.13 ms: 1.79x faster                                 |
| django_template         | 46.3 ms                                                | 35.4 ms: 1.31x faster                                 |
| dulwich_log             | 75.5 ms                                                | 65.7 ms: 1.15x faster                                 |
| fannkuch                | 477 ms                                                 | 400 ms: 1.19x faster                                  |
| float                   | 108 ms                                                 | 77.5 ms: 1.39x faster                                 |
| go                      | 226 ms                                                 | 147 ms: 1.54x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.76 ms: 1.39x faster                                 |
| html5lib                | 85.8 ms                                                | 67.9 ms: 1.26x faster                                 |
| json                    | 5.35 ms                                                | 4.84 ms: 1.11x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.2 ms: 1.10x faster                                 |
| json_loads              | 28.9 us                                                | 26.7 us: 1.08x faster                                 |
| logging_format          | 8.92 us                                                | 6.37 us: 1.40x faster                                 |
| logging_silent          | 173 ns                                                 | 113 ns: 1.53x faster                                  |
| logging_simple          | 8.06 us                                                | 5.84 us: 1.38x faster                                 |
| mako                    | 14.3 ms                                                | 10.5 ms: 1.36x faster                                 |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.08x faster                                  |
| nbody                   | 136 ms                                                 | 94.7 ms: 1.44x faster                                 |
| nqueens                 | 99.3 ms                                                | 87.2 ms: 1.14x faster                                 |
| pathlib                 | 20.0 ms                                                | 18.5 ms: 1.08x faster                                 |
| pickle                  | 10.1 us                                                | 9.93 us: 1.02x faster                                 |
| pickle_dict             | 28.3 us                                                | 28.1 us: 1.01x faster                                 |
| pickle_list             | 4.50 us                                                | 4.47 us: 1.01x faster                                 |
| pickle_pure_python      | 453 us                                                 | 334 us: 1.36x faster                                  |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                  |
| pycparser               | 1.51 sec                                               | 1.19 sec: 1.27x faster                                |
| pyflate                 | 675 ms                                                 | 459 ms: 1.47x faster                                  |
| python_startup          | 13.9 ms                                                | 8.13 ms: 1.71x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 5.92 ms: 1.03x slower                                 |
| raytrace                | 461 ms                                                 | 321 ms: 1.44x faster                                  |
| regex_compile           | 174 ms                                                 | 140 ms: 1.24x faster                                  |
| regex_dna               | 214 ms                                                 | 213 ms: 1.01x faster                                  |
| regex_effbot            | 3.21 ms                                                | 3.14 ms: 1.02x faster                                 |
| regex_v8                | 25.0 ms                                                | 24.0 ms: 1.04x faster                                 |
| richards                | 71.4 ms                                                | 50.8 ms: 1.40x faster                                 |
| scimark_fft             | 414 ms                                                 | 347 ms: 1.19x faster                                  |
| scimark_lu              | 158 ms                                                 | 120 ms: 1.32x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 72.6 ms: 1.44x faster                                 |
| scimark_sor             | 193 ms                                                 | 129 ms: 1.50x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 5.14 ms: 1.07x faster                                 |
| spectral_norm           | 148 ms                                                 | 104 ms: 1.42x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.71 us: 1.07x faster                                 |
| sympy_expand            | 537 ms                                                 | 503 ms: 1.07x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 21.3 ms: 1.13x faster                                 |
| sympy_sum               | 183 ms                                                 | 170 ms: 1.08x faster                                  |
| sympy_str               | 324 ms                                                 | 304 ms: 1.07x faster                                  |
| thrift                  | 1.03 ms                                                | 815 us: 1.27x faster                                  |
| tornado_http            | 128 ms                                                 | 106 ms: 1.21x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 46.0 ns: 1.29x faster                                 |
| unpickle                | 14.3 us                                                | 13.4 us: 1.06x faster                                 |
| unpickle_list           | 4.99 us                                                | 5.26 us: 1.05x slower                                 |
| unpickle_pure_python    | 297 us                                                 | 249 us: 1.19x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 153 ms: 1.07x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 106 ms: 1.04x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 79.6 ms: 1.17x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 57.0 ms: 1.31x faster                                 |
| Geometric mean          | (ref)                                                  | 1.22x faster                                          |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
