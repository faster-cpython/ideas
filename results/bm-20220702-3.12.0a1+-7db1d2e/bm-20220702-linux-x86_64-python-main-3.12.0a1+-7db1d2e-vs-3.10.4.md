Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.39 ms: 1.39x faster                                  |
| html5lib       | 85.8 ms                                                | 62.0 ms: 1.38x faster                                  |
| tornado_http   | 128 ms                                                 | 91.4 ms: 1.40x faster                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 69.9 ms: 1.54x faster                                  |
| nbody          | 136 ms                                                 | 89.9 ms: 1.52x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.33x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 125 ms: 1.40x faster                                   |
| regex_dna      | 214 ms                                                 | 197 ms: 1.09x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.49 ms: 1.09x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.0 ms: 1.13x faster                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 11.9 ms: 1.13x faster                                  |
| json_loads           | 28.9 us                                                | 24.3 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.5 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 30.7 us: 1.08x slower                                  |
| pickle_list          | 4.50 us                                                | 4.28 us: 1.05x faster                                  |
| pickle_pure_python   | 453 us                                                 | 282 us: 1.60x faster                                   |
| unpickle             | 14.3 us                                                | 13.4 us: 1.07x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.93 us: 1.01x faster                                  |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 156 ms: 1.04x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.0 ms: 1.24x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 52.0 ms: 1.43x faster                                  |
| Geometric mean       | (ref)                                                  | 1.16x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.22 ms: 1.70x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.07 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.0 ms: 1.44x faster                                  |
| mako            | 14.3 ms                                                | 9.55 ms: 1.49x faster                                  |
| Geometric mean  | (ref)                                                  | 1.47x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220702-linux-x86_64-python-main-3.12.0a1+-7db1d2e |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon               | 8.86 ms                                                | 6.39 ms: 1.39x faster                                  |
| chaos                   | 104 ms                                                 | 65.2 ms: 1.60x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 73.3 ms: 1.60x faster                                  |
| deltablue               | 7.39 ms                                                | 3.20 ms: 2.31x faster                                  |
| django_template         | 46.3 ms                                                | 32.0 ms: 1.44x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.2 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 373 ms: 1.28x faster                                   |
| float                   | 108 ms                                                 | 69.9 ms: 1.54x faster                                  |
| go                      | 226 ms                                                 | 130 ms: 1.74x faster                                   |
| hexiom                  | 9.42 ms                                                | 5.88 ms: 1.60x faster                                  |
| html5lib                | 85.8 ms                                                | 62.0 ms: 1.38x faster                                  |
| json                    | 5.35 ms                                                | 4.70 ms: 1.14x faster                                  |
| json_dumps              | 13.5 ms                                                | 11.9 ms: 1.13x faster                                  |
| json_loads              | 28.9 us                                                | 24.3 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.26 us: 1.43x faster                                  |
| logging_silent          | 173 ns                                                 | 91.7 ns: 1.89x faster                                  |
| logging_simple          | 8.06 us                                                | 5.74 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.55 ms: 1.49x faster                                  |
| meteor_contest          | 114 ms                                                 | 101 ms: 1.12x faster                                   |
| nbody                   | 136 ms                                                 | 89.9 ms: 1.52x faster                                  |
| nqueens                 | 99.3 ms                                                | 81.0 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.5 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 30.7 us: 1.08x slower                                  |
| pickle_list             | 4.50 us                                                | 4.28 us: 1.05x faster                                  |
| pickle_pure_python      | 453 us                                                 | 282 us: 1.60x faster                                   |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| pycparser               | 1.51 sec                                               | 1.08 sec: 1.40x faster                                 |
| pyflate                 | 675 ms                                                 | 389 ms: 1.74x faster                                   |
| python_startup          | 13.9 ms                                                | 8.22 ms: 1.70x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.07 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 282 ms: 1.63x faster                                   |
| regex_compile           | 174 ms                                                 | 125 ms: 1.40x faster                                   |
| regex_dna               | 214 ms                                                 | 197 ms: 1.09x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.49 ms: 1.09x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.0 ms: 1.13x faster                                  |
| richards                | 71.4 ms                                                | 44.6 ms: 1.60x faster                                  |
| scimark_fft             | 414 ms                                                 | 309 ms: 1.34x faster                                   |
| scimark_lu              | 158 ms                                                 | 105 ms: 1.51x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 62.8 ms: 1.67x faster                                  |
| scimark_sor             | 193 ms                                                 | 111 ms: 1.74x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.21 ms: 1.30x faster                                  |
| spectral_norm           | 148 ms                                                 | 94.3 ms: 1.57x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 450 ms: 1.19x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.1 ms: 1.19x faster                                  |
| sympy_sum               | 183 ms                                                 | 158 ms: 1.16x faster                                   |
| sympy_str               | 324 ms                                                 | 276 ms: 1.17x faster                                   |
| telco                   | 6.68 ms                                                | 6.59 ms: 1.01x faster                                  |
| thrift                  | 1.03 ms                                                | 744 us: 1.39x faster                                   |
| tornado_http            | 128 ms                                                 | 91.4 ms: 1.40x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 45.5 ns: 1.31x faster                                  |
| unpickle                | 14.3 us                                                | 13.4 us: 1.07x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.93 us: 1.01x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 156 ms: 1.04x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.0 ms: 1.24x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 52.0 ms: 1.43x faster                                  |
| Geometric mean          | (ref)                                                  | 1.32x faster                                           |
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
