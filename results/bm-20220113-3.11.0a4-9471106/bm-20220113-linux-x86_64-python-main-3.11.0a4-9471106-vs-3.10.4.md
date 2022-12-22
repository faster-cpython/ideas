Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 264 ms: 1.26x faster                                  |
| chameleon      | 8.86 ms                                                | 7.55 ms: 1.17x faster                                 |
| html5lib       | 85.8 ms                                                | 68.1 ms: 1.26x faster                                 |
| tornado_http   | 128 ms                                                 | 107 ms: 1.20x faster                                  |
| Geometric mean | (ref)                                                  | 1.22x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 78.0 ms: 1.38x faster                                 |
| nbody          | 136 ms                                                 | 95.1 ms: 1.43x faster                                 |
| pidigits       | 190 ms                                                 | 194 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 138 ms: 1.26x faster                                  |
| regex_dna      | 214 ms                                                 | 212 ms: 1.01x faster                                  |
| regex_effbot   | 3.21 ms                                                | 3.25 ms: 1.01x slower                                 |
| regex_v8       | 25.0 ms                                                | 24.8 ms: 1.00x faster                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.4 ms: 1.09x faster                                 |
| json_loads           | 28.9 us                                                | 25.1 us: 1.15x faster                                 |
| pickle               | 10.1 us                                                | 9.95 us: 1.02x faster                                 |
| pickle_dict          | 28.3 us                                                | 26.8 us: 1.06x faster                                 |
| pickle_list          | 4.50 us                                                | 4.37 us: 1.03x faster                                 |
| pickle_pure_python   | 453 us                                                 | 329 us: 1.38x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.20 us: 1.04x slower                                 |
| unpickle_pure_python | 297 us                                                 | 254 us: 1.17x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 155 ms: 1.06x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 107 ms: 1.03x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.2 ms: 1.16x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 56.9 ms: 1.31x faster                                 |
| Geometric mean       | (ref)                                                  | 1.10x faster                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.07 ms: 1.73x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 5.85 ms: 1.01x slower                                 |
| Geometric mean         | (ref)                                                  | 1.30x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 35.2 ms: 1.31x faster                                 |
| mako            | 14.3 ms                                                | 11.5 ms: 1.24x faster                                 |
| Geometric mean  | (ref)                                                  | 1.27x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 264 ms: 1.26x faster                                  |
| chameleon               | 8.86 ms                                                | 7.55 ms: 1.17x faster                                 |
| chaos                   | 104 ms                                                 | 72.7 ms: 1.43x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 83.8 ms: 1.40x faster                                 |
| deltablue               | 7.39 ms                                                | 4.16 ms: 1.78x faster                                 |
| django_template         | 46.3 ms                                                | 35.2 ms: 1.31x faster                                 |
| dulwich_log             | 75.5 ms                                                | 65.8 ms: 1.15x faster                                 |
| fannkuch                | 477 ms                                                 | 392 ms: 1.22x faster                                  |
| float                   | 108 ms                                                 | 78.0 ms: 1.38x faster                                 |
| go                      | 226 ms                                                 | 148 ms: 1.53x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.63 ms: 1.42x faster                                 |
| html5lib                | 85.8 ms                                                | 68.1 ms: 1.26x faster                                 |
| json                    | 5.35 ms                                                | 4.74 ms: 1.13x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.4 ms: 1.09x faster                                 |
| json_loads              | 28.9 us                                                | 25.1 us: 1.15x faster                                 |
| logging_format          | 8.92 us                                                | 6.51 us: 1.37x faster                                 |
| logging_silent          | 173 ns                                                 | 113 ns: 1.53x faster                                  |
| logging_simple          | 8.06 us                                                | 5.95 us: 1.35x faster                                 |
| mako                    | 14.3 ms                                                | 11.5 ms: 1.24x faster                                 |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.11x faster                                  |
| nbody                   | 136 ms                                                 | 95.1 ms: 1.43x faster                                 |
| nqueens                 | 99.3 ms                                                | 84.0 ms: 1.18x faster                                 |
| pathlib                 | 20.0 ms                                                | 19.1 ms: 1.05x faster                                 |
| pickle                  | 10.1 us                                                | 9.95 us: 1.02x faster                                 |
| pickle_dict             | 28.3 us                                                | 26.8 us: 1.06x faster                                 |
| pickle_list             | 4.50 us                                                | 4.37 us: 1.03x faster                                 |
| pickle_pure_python      | 453 us                                                 | 329 us: 1.38x faster                                  |
| pidigits                | 190 ms                                                 | 194 ms: 1.02x slower                                  |
| pycparser               | 1.51 sec                                               | 1.17 sec: 1.30x faster                                |
| pyflate                 | 675 ms                                                 | 444 ms: 1.52x faster                                  |
| python_startup          | 13.9 ms                                                | 8.07 ms: 1.73x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 5.85 ms: 1.01x slower                                 |
| raytrace                | 461 ms                                                 | 320 ms: 1.44x faster                                  |
| regex_compile           | 174 ms                                                 | 138 ms: 1.26x faster                                  |
| regex_dna               | 214 ms                                                 | 212 ms: 1.01x faster                                  |
| regex_effbot            | 3.21 ms                                                | 3.25 ms: 1.01x slower                                 |
| regex_v8                | 25.0 ms                                                | 24.8 ms: 1.00x faster                                 |
| richards                | 71.4 ms                                                | 51.5 ms: 1.38x faster                                 |
| scimark_fft             | 414 ms                                                 | 330 ms: 1.26x faster                                  |
| scimark_lu              | 158 ms                                                 | 114 ms: 1.39x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 72.7 ms: 1.44x faster                                 |
| scimark_sor             | 193 ms                                                 | 124 ms: 1.55x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.69 ms: 1.17x faster                                 |
| spectral_norm           | 148 ms                                                 | 99.0 ms: 1.50x faster                                 |
| sqlite_synth            | 2.90 us                                                | 2.73 us: 1.06x faster                                 |
| sympy_expand            | 537 ms                                                 | 506 ms: 1.06x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 21.4 ms: 1.12x faster                                 |
| sympy_sum               | 183 ms                                                 | 170 ms: 1.08x faster                                  |
| sympy_str               | 324 ms                                                 | 302 ms: 1.08x faster                                  |
| thrift                  | 1.03 ms                                                | 812 us: 1.27x faster                                  |
| tornado_http            | 128 ms                                                 | 107 ms: 1.20x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 44.8 ns: 1.33x faster                                 |
| unpickle_list           | 4.99 us                                                | 5.20 us: 1.04x slower                                 |
| unpickle_pure_python    | 297 us                                                 | 254 us: 1.17x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 155 ms: 1.06x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 107 ms: 1.03x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 80.2 ms: 1.16x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 56.9 ms: 1.31x faster                                 |
| Geometric mean          | (ref)                                                  | 1.22x faster                                          |

Benchmark hidden because not significant (2): telco, unpickle
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
