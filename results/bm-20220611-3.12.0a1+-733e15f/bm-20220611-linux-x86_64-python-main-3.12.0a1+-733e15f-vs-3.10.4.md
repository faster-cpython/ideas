Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 251 ms: 1.33x faster                                   |
| chameleon      | 8.86 ms                                                | 6.40 ms: 1.38x faster                                  |
| html5lib       | 85.8 ms                                                | 63.4 ms: 1.35x faster                                  |
| tornado_http   | 128 ms                                                 | 91.3 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                  | 1.37x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 71.0 ms: 1.52x faster                                  |
| nbody          | 136 ms                                                 | 91.3 ms: 1.49x faster                                  |
| pidigits       | 190 ms                                                 | 197 ms: 1.03x slower                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 132 ms: 1.31x faster                                   |
| regex_dna      | 214 ms                                                 | 198 ms: 1.08x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.01 ms: 1.07x faster                                  |
| regex_v8       | 25.0 ms                                                | 21.3 ms: 1.17x faster                                  |
| Geometric mean | (ref)                                                  | 1.15x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.0 ms: 1.12x faster                                  |
| json_loads           | 28.9 us                                                | 25.1 us: 1.15x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.01x slower                                  |
| pickle_dict          | 28.3 us                                                | 30.6 us: 1.08x slower                                  |
| pickle_list          | 4.50 us                                                | 4.11 us: 1.10x faster                                  |
| pickle_pure_python   | 453 us                                                 | 293 us: 1.55x faster                                   |
| unpickle_list        | 4.99 us                                                | 4.89 us: 1.02x faster                                  |
| unpickle_pure_python | 297 us                                                 | 212 us: 1.40x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 159 ms: 1.02x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 104 ms: 1.06x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.4 ms: 1.24x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 52.1 ms: 1.43x faster                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.26 ms: 1.69x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.11 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 31.2 ms: 1.48x faster                                  |
| mako            | 14.3 ms                                                | 9.74 ms: 1.46x faster                                  |
| Geometric mean  | (ref)                                                  | 1.47x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220611-linux-x86_64-python-main-3.12.0a1+-733e15f |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 251 ms: 1.33x faster                                   |
| chameleon               | 8.86 ms                                                | 6.40 ms: 1.38x faster                                  |
| chaos                   | 104 ms                                                 | 68.0 ms: 1.53x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 74.0 ms: 1.59x faster                                  |
| deltablue               | 7.39 ms                                                | 3.51 ms: 2.11x faster                                  |
| django_template         | 46.3 ms                                                | 31.2 ms: 1.48x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.9 ms: 1.22x faster                                  |
| fannkuch                | 477 ms                                                 | 382 ms: 1.25x faster                                   |
| float                   | 108 ms                                                 | 71.0 ms: 1.52x faster                                  |
| go                      | 226 ms                                                 | 131 ms: 1.72x faster                                   |
| hexiom                  | 9.42 ms                                                | 6.17 ms: 1.52x faster                                  |
| html5lib                | 85.8 ms                                                | 63.4 ms: 1.35x faster                                  |
| json                    | 5.35 ms                                                | 4.78 ms: 1.12x faster                                  |
| json_dumps              | 13.5 ms                                                | 12.0 ms: 1.12x faster                                  |
| json_loads              | 28.9 us                                                | 25.1 us: 1.15x faster                                  |
| logging_format          | 8.92 us                                                | 6.36 us: 1.40x faster                                  |
| logging_silent          | 173 ns                                                 | 99.2 ns: 1.75x faster                                  |
| logging_simple          | 8.06 us                                                | 5.84 us: 1.38x faster                                  |
| mako                    | 14.3 ms                                                | 9.74 ms: 1.46x faster                                  |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.12x faster                                   |
| nbody                   | 136 ms                                                 | 91.3 ms: 1.49x faster                                  |
| nqueens                 | 99.3 ms                                                | 83.4 ms: 1.19x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.12x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.01x slower                                  |
| pickle_dict             | 28.3 us                                                | 30.6 us: 1.08x slower                                  |
| pickle_list             | 4.50 us                                                | 4.11 us: 1.10x faster                                  |
| pickle_pure_python      | 453 us                                                 | 293 us: 1.55x faster                                   |
| pidigits                | 190 ms                                                 | 197 ms: 1.03x slower                                   |
| pycparser               | 1.51 sec                                               | 1.07 sec: 1.42x faster                                 |
| pyflate                 | 675 ms                                                 | 400 ms: 1.69x faster                                   |
| python_startup          | 13.9 ms                                                | 8.26 ms: 1.69x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.11 ms: 1.06x slower                                  |
| raytrace                | 461 ms                                                 | 281 ms: 1.64x faster                                   |
| regex_compile           | 174 ms                                                 | 132 ms: 1.31x faster                                   |
| regex_dna               | 214 ms                                                 | 198 ms: 1.08x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.01 ms: 1.07x faster                                  |
| regex_v8                | 25.0 ms                                                | 21.3 ms: 1.17x faster                                  |
| richards                | 71.4 ms                                                | 43.6 ms: 1.64x faster                                  |
| scimark_fft             | 414 ms                                                 | 315 ms: 1.32x faster                                   |
| scimark_lu              | 158 ms                                                 | 102 ms: 1.56x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 66.7 ms: 1.57x faster                                  |
| scimark_sor             | 193 ms                                                 | 110 ms: 1.75x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.36 ms: 1.26x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.3 ms: 1.55x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.50 us: 1.16x faster                                  |
| sympy_expand            | 537 ms                                                 | 457 ms: 1.17x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.2 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                   |
| sympy_str               | 324 ms                                                 | 283 ms: 1.15x faster                                   |
| telco                   | 6.68 ms                                                | 6.46 ms: 1.03x faster                                  |
| thrift                  | 1.03 ms                                                | 741 us: 1.39x faster                                   |
| tornado_http            | 128 ms                                                 | 91.3 ms: 1.41x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 43.6 ns: 1.36x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.89 us: 1.02x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 212 us: 1.40x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 159 ms: 1.02x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 104 ms: 1.06x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.4 ms: 1.24x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 52.1 ms: 1.43x faster                                  |
| Geometric mean          | (ref)                                                  | 1.31x faster                                           |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
