Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| chameleon      | 8.86 ms                                                | 6.30 ms: 1.41x faster                                  |
| html5lib       | 85.8 ms                                                | 62.9 ms: 1.36x faster                                  |
| tornado_http   | 128 ms                                                 | 91.6 ms: 1.40x faster                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.6 ms: 1.48x faster                                  |
| nbody          | 136 ms                                                 | 91.3 ms: 1.49x faster                                  |
| pidigits       | 190 ms                                                 | 201 ms: 1.06x slower                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna      | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.42 ms: 1.06x slower                                  |
| regex_v8       | 25.0 ms                                                | 20.9 ms: 1.19x faster                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.67 ms: 1.39x faster                                  |
| json_loads           | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.5 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.4 us: 1.11x slower                                  |
| pickle_list          | 4.50 us                                                | 4.25 us: 1.06x faster                                  |
| pickle_pure_python   | 453 us                                                 | 287 us: 1.58x faster                                   |
| unpickle             | 14.3 us                                                | 13.2 us: 1.08x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.94 us: 1.01x faster                                  |
| unpickle_pure_python | 297 us                                                 | 201 us: 1.48x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 155 ms: 1.06x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 105 ms: 1.06x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 74.3 ms: 1.26x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 51.3 ms: 1.45x faster                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.17 ms: 1.71x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.04 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.5 ms: 1.42x faster                                  |
| mako            | 14.3 ms                                                | 9.21 ms: 1.55x faster                                  |
| Geometric mean  | (ref)                                                  | 1.48x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220813-linux-x86_64-python-main-3.12.0a1+-32ac98e |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| chameleon               | 8.86 ms                                                | 6.30 ms: 1.41x faster                                  |
| chaos                   | 104 ms                                                 | 66.8 ms: 1.56x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 74.2 ms: 1.58x faster                                  |
| deltablue               | 7.39 ms                                                | 3.20 ms: 2.31x faster                                  |
| django_template         | 46.3 ms                                                | 32.5 ms: 1.42x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.6 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 375 ms: 1.27x faster                                   |
| float                   | 108 ms                                                 | 72.6 ms: 1.48x faster                                  |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                   |
| hexiom                  | 9.42 ms                                                | 5.97 ms: 1.58x faster                                  |
| html5lib                | 85.8 ms                                                | 62.9 ms: 1.36x faster                                  |
| json                    | 5.35 ms                                                | 4.68 ms: 1.14x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.67 ms: 1.39x faster                                  |
| json_loads              | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.39 us: 1.40x faster                                  |
| logging_silent          | 173 ns                                                 | 89.6 ns: 1.93x faster                                  |
| logging_simple          | 8.06 us                                                | 5.81 us: 1.39x faster                                  |
| mako                    | 14.3 ms                                                | 9.21 ms: 1.55x faster                                  |
| meteor_contest          | 114 ms                                                 | 101 ms: 1.13x faster                                   |
| nbody                   | 136 ms                                                 | 91.3 ms: 1.49x faster                                  |
| nqueens                 | 99.3 ms                                                | 80.9 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.5 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.4 us: 1.11x slower                                  |
| pickle_list             | 4.50 us                                                | 4.25 us: 1.06x faster                                  |
| pickle_pure_python      | 453 us                                                 | 287 us: 1.58x faster                                   |
| pidigits                | 190 ms                                                 | 201 ms: 1.06x slower                                   |
| pycparser               | 1.51 sec                                               | 1.05 sec: 1.44x faster                                 |
| pyflate                 | 675 ms                                                 | 397 ms: 1.70x faster                                   |
| python_startup          | 13.9 ms                                                | 8.17 ms: 1.71x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.04 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 293 ms: 1.57x faster                                   |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna               | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.42 ms: 1.06x slower                                  |
| regex_v8                | 25.0 ms                                                | 20.9 ms: 1.19x faster                                  |
| richards                | 71.4 ms                                                | 45.1 ms: 1.58x faster                                  |
| scimark_fft             | 414 ms                                                 | 308 ms: 1.34x faster                                   |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.48x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.7 ms: 1.62x faster                                  |
| scimark_sor             | 193 ms                                                 | 111 ms: 1.74x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.15 ms: 1.32x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.1 ms: 1.56x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.58 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 457 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.1 ms: 1.19x faster                                  |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                   |
| sympy_str               | 324 ms                                                 | 278 ms: 1.17x faster                                   |
| telco                   | 6.68 ms                                                | 6.47 ms: 1.03x faster                                  |
| thrift                  | 1.03 ms                                                | 728 us: 1.42x faster                                   |
| tornado_http            | 128 ms                                                 | 91.6 ms: 1.40x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 43.0 ns: 1.38x faster                                  |
| unpickle                | 14.3 us                                                | 13.2 us: 1.08x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.94 us: 1.01x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 201 us: 1.48x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 155 ms: 1.06x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 105 ms: 1.06x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 74.3 ms: 1.26x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 51.3 ms: 1.45x faster                                  |
| Geometric mean          | (ref)                                                  | 1.32x faster                                           |
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
