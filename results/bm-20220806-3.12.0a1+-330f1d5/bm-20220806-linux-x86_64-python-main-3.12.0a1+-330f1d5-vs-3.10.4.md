Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.50 ms: 1.36x faster                                  |
| html5lib       | 85.8 ms                                                | 62.6 ms: 1.37x faster                                  |
| tornado_http   | 128 ms                                                 | 91.7 ms: 1.40x faster                                  |
| Geometric mean | (ref)                                                  | 1.37x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 74.1 ms: 1.45x faster                                  |
| nbody          | 136 ms                                                 | 91.3 ms: 1.49x faster                                  |
| pidigits       | 190 ms                                                 | 194 ms: 1.02x slower                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna      | 214 ms                                                 | 203 ms: 1.05x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.50 ms: 1.09x slower                                  |
| regex_v8       | 25.0 ms                                                | 20.8 ms: 1.20x faster                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.51 ms: 1.42x faster                                  |
| json_loads           | 28.9 us                                                | 24.6 us: 1.17x faster                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.9 us: 1.13x slower                                  |
| pickle_list          | 4.50 us                                                | 4.26 us: 1.06x faster                                  |
| pickle_pure_python   | 453 us                                                 | 288 us: 1.57x faster                                   |
| unpickle             | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.06 us: 1.01x slower                                  |
| unpickle_pure_python | 297 us                                                 | 199 us: 1.49x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 156 ms: 1.05x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 105 ms: 1.05x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.0 ms: 1.24x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 52.2 ms: 1.43x faster                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.15 ms: 1.71x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.01 ms: 1.04x slower                                  |
| Geometric mean         | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.5 ms: 1.42x faster                                  |
| mako            | 14.3 ms                                                | 9.50 ms: 1.50x faster                                  |
| Geometric mean  | (ref)                                                  | 1.46x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220806-linux-x86_64-python-main-3.12.0a1+-330f1d5 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon               | 8.86 ms                                                | 6.50 ms: 1.36x faster                                  |
| chaos                   | 104 ms                                                 | 66.8 ms: 1.56x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 72.6 ms: 1.62x faster                                  |
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.30x faster                                  |
| django_template         | 46.3 ms                                                | 32.5 ms: 1.42x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.2 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 374 ms: 1.27x faster                                   |
| float                   | 108 ms                                                 | 74.1 ms: 1.45x faster                                  |
| go                      | 226 ms                                                 | 131 ms: 1.73x faster                                   |
| hexiom                  | 9.42 ms                                                | 5.98 ms: 1.57x faster                                  |
| html5lib                | 85.8 ms                                                | 62.6 ms: 1.37x faster                                  |
| json                    | 5.35 ms                                                | 4.70 ms: 1.14x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.51 ms: 1.42x faster                                  |
| json_loads              | 28.9 us                                                | 24.6 us: 1.17x faster                                  |
| logging_format          | 8.92 us                                                | 6.34 us: 1.41x faster                                  |
| logging_silent          | 173 ns                                                 | 89.9 ns: 1.93x faster                                  |
| logging_simple          | 8.06 us                                                | 5.72 us: 1.41x faster                                  |
| mako                    | 14.3 ms                                                | 9.50 ms: 1.50x faster                                  |
| meteor_contest          | 114 ms                                                 | 101 ms: 1.12x faster                                   |
| nbody                   | 136 ms                                                 | 91.3 ms: 1.49x faster                                  |
| nqueens                 | 99.3 ms                                                | 79.2 ms: 1.25x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.6 ms: 1.14x faster                                  |
| pickle                  | 10.1 us                                                | 10.4 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.9 us: 1.13x slower                                  |
| pickle_list             | 4.50 us                                                | 4.26 us: 1.06x faster                                  |
| pickle_pure_python      | 453 us                                                 | 288 us: 1.57x faster                                   |
| pidigits                | 190 ms                                                 | 194 ms: 1.02x slower                                   |
| pycparser               | 1.51 sec                                               | 1.04 sec: 1.45x faster                                 |
| pyflate                 | 675 ms                                                 | 393 ms: 1.72x faster                                   |
| python_startup          | 13.9 ms                                                | 8.15 ms: 1.71x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.01 ms: 1.04x slower                                  |
| raytrace                | 461 ms                                                 | 278 ms: 1.66x faster                                   |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                   |
| regex_dna               | 214 ms                                                 | 203 ms: 1.05x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.50 ms: 1.09x slower                                  |
| regex_v8                | 25.0 ms                                                | 20.8 ms: 1.20x faster                                  |
| richards                | 71.4 ms                                                | 44.5 ms: 1.60x faster                                  |
| scimark_fft             | 414 ms                                                 | 311 ms: 1.33x faster                                   |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.49x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 64.2 ms: 1.63x faster                                  |
| scimark_sor             | 193 ms                                                 | 110 ms: 1.75x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.91 ms: 1.40x faster                                  |
| spectral_norm           | 148 ms                                                 | 93.8 ms: 1.58x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 461 ms: 1.16x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 160 ms: 1.14x faster                                   |
| sympy_str               | 324 ms                                                 | 282 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.41 ms: 1.04x faster                                  |
| thrift                  | 1.03 ms                                                | 748 us: 1.38x faster                                   |
| tornado_http            | 128 ms                                                 | 91.7 ms: 1.40x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 45.9 ns: 1.29x faster                                  |
| unpickle                | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.06 us: 1.01x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 199 us: 1.49x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 156 ms: 1.05x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 105 ms: 1.05x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.0 ms: 1.24x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 52.2 ms: 1.43x faster                                  |
| Geometric mean          | (ref)                                                  | 1.32x faster                                           |
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
