Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.33x faster                                   |
| chameleon      | 8.86 ms                                                | 6.30 ms: 1.41x faster                                  |
| html5lib       | 85.8 ms                                                | 62.6 ms: 1.37x faster                                  |
| tornado_http   | 128 ms                                                 | 91.3 ms: 1.40x faster                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.4 ms: 1.49x faster                                  |
| nbody          | 136 ms                                                 | 90.5 ms: 1.51x faster                                  |
| pidigits       | 190 ms                                                 | 193 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 126 ms: 1.38x faster                                   |
| regex_dna      | 214 ms                                                 | 207 ms: 1.03x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.54 ms: 1.10x slower                                  |
| regex_v8       | 25.0 ms                                                | 22.1 ms: 1.13x faster                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 11.8 ms: 1.14x faster                                  |
| json_loads           | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.5 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.6 us: 1.12x slower                                  |
| pickle_list          | 4.50 us                                                | 4.12 us: 1.09x faster                                  |
| pickle_pure_python   | 453 us                                                 | 286 us: 1.59x faster                                   |
| unpickle             | 14.3 us                                                | 13.1 us: 1.09x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.04 us: 1.01x slower                                  |
| unpickle_pure_python | 297 us                                                 | 201 us: 1.48x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 156 ms: 1.05x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 104 ms: 1.07x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.9 ms: 1.23x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean       | (ref)                                                  | 1.15x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.16 ms: 1.71x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.01 ms: 1.04x slower                                  |
| Geometric mean         | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 31.5 ms: 1.47x faster                                  |
| mako            | 14.3 ms                                                | 9.45 ms: 1.51x faster                                  |
| Geometric mean  | (ref)                                                  | 1.49x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 249 ms: 1.33x faster                                   |
| chameleon               | 8.86 ms                                                | 6.30 ms: 1.41x faster                                  |
| chaos                   | 104 ms                                                 | 65.0 ms: 1.60x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 74.3 ms: 1.58x faster                                  |
| deltablue               | 7.39 ms                                                | 3.24 ms: 2.28x faster                                  |
| django_template         | 46.3 ms                                                | 31.5 ms: 1.47x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.2 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 378 ms: 1.26x faster                                   |
| float                   | 108 ms                                                 | 72.4 ms: 1.49x faster                                  |
| go                      | 226 ms                                                 | 130 ms: 1.74x faster                                   |
| hexiom                  | 9.42 ms                                                | 5.92 ms: 1.59x faster                                  |
| html5lib                | 85.8 ms                                                | 62.6 ms: 1.37x faster                                  |
| json                    | 5.35 ms                                                | 4.69 ms: 1.14x faster                                  |
| json_dumps              | 13.5 ms                                                | 11.8 ms: 1.14x faster                                  |
| json_loads              | 28.9 us                                                | 24.2 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.35 us: 1.41x faster                                  |
| logging_silent          | 173 ns                                                 | 92.5 ns: 1.87x faster                                  |
| logging_simple          | 8.06 us                                                | 5.67 us: 1.42x faster                                  |
| mako                    | 14.3 ms                                                | 9.45 ms: 1.51x faster                                  |
| meteor_contest          | 114 ms                                                 | 101 ms: 1.13x faster                                   |
| nbody                   | 136 ms                                                 | 90.5 ms: 1.51x faster                                  |
| nqueens                 | 99.3 ms                                                | 80.8 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 18.0 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.5 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.6 us: 1.12x slower                                  |
| pickle_list             | 4.50 us                                                | 4.12 us: 1.09x faster                                  |
| pickle_pure_python      | 453 us                                                 | 286 us: 1.59x faster                                   |
| pidigits                | 190 ms                                                 | 193 ms: 1.01x slower                                   |
| pycparser               | 1.51 sec                                               | 1.06 sec: 1.42x faster                                 |
| pyflate                 | 675 ms                                                 | 398 ms: 1.70x faster                                   |
| python_startup          | 13.9 ms                                                | 8.16 ms: 1.71x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.01 ms: 1.04x slower                                  |
| raytrace                | 461 ms                                                 | 286 ms: 1.61x faster                                   |
| regex_compile           | 174 ms                                                 | 126 ms: 1.38x faster                                   |
| regex_dna               | 214 ms                                                 | 207 ms: 1.03x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.54 ms: 1.10x slower                                  |
| regex_v8                | 25.0 ms                                                | 22.1 ms: 1.13x faster                                  |
| richards                | 71.4 ms                                                | 45.0 ms: 1.59x faster                                  |
| scimark_fft             | 414 ms                                                 | 313 ms: 1.32x faster                                   |
| scimark_lu              | 158 ms                                                 | 104 ms: 1.52x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.6 ms: 1.62x faster                                  |
| scimark_sor             | 193 ms                                                 | 111 ms: 1.75x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.18 ms: 1.31x faster                                  |
| spectral_norm           | 148 ms                                                 | 97.7 ms: 1.51x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.62 us: 1.11x faster                                  |
| sympy_expand            | 537 ms                                                 | 450 ms: 1.19x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.1 ms: 1.19x faster                                  |
| sympy_sum               | 183 ms                                                 | 158 ms: 1.16x faster                                   |
| sympy_str               | 324 ms                                                 | 279 ms: 1.16x faster                                   |
| telco                   | 6.68 ms                                                | 6.51 ms: 1.03x faster                                  |
| thrift                  | 1.03 ms                                                | 720 us: 1.43x faster                                   |
| tornado_http            | 128 ms                                                 | 91.3 ms: 1.40x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 46.4 ns: 1.28x faster                                  |
| unpickle                | 14.3 us                                                | 13.1 us: 1.09x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.04 us: 1.01x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 201 us: 1.48x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 156 ms: 1.05x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 104 ms: 1.07x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.9 ms: 1.23x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                           |
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
