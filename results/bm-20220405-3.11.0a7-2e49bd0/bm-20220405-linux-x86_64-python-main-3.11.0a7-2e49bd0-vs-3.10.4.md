Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 264 ms: 1.26x faster                                  |
| chameleon      | 8.86 ms                                                | 6.87 ms: 1.29x faster                                 |
| html5lib       | 85.8 ms                                                | 65.3 ms: 1.31x faster                                 |
| tornado_http   | 128 ms                                                 | 95.4 ms: 1.35x faster                                 |
| Geometric mean | (ref)                                                  | 1.30x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 74.4 ms: 1.45x faster                                 |
| nbody          | 136 ms                                                 | 95.2 ms: 1.43x faster                                 |
| pidigits       | 190 ms                                                 | 197 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 137 ms: 1.26x faster                                  |
| regex_dna      | 214 ms                                                 | 231 ms: 1.08x slower                                  |
| regex_effbot   | 3.21 ms                                                | 3.34 ms: 1.04x slower                                 |
| regex_v8       | 25.0 ms                                                | 25.9 ms: 1.04x slower                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.5 ms: 1.08x faster                                 |
| json_loads           | 28.9 us                                                | 28.1 us: 1.03x faster                                 |
| pickle               | 10.1 us                                                | 9.55 us: 1.06x faster                                 |
| pickle_dict          | 28.3 us                                                | 27.6 us: 1.02x faster                                 |
| pickle_list          | 4.50 us                                                | 4.57 us: 1.01x slower                                 |
| pickle_pure_python   | 453 us                                                 | 311 us: 1.46x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.97 us: 1.01x faster                                 |
| unpickle_pure_python | 297 us                                                 | 231 us: 1.29x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 157 ms: 1.04x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 104 ms: 1.07x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 78.5 ms: 1.19x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 55.2 ms: 1.35x faster                                 |
| Geometric mean       | (ref)                                                  | 1.11x faster                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.07 ms: 1.73x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 5.98 ms: 1.04x slower                                 |
| Geometric mean         | (ref)                                                  | 1.29x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 34.3 ms: 1.35x faster                                 |
| mako            | 14.3 ms                                                | 10.2 ms: 1.40x faster                                 |
| Geometric mean  | (ref)                                                  | 1.38x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 264 ms: 1.26x faster                                  |
| chameleon               | 8.86 ms                                                | 6.87 ms: 1.29x faster                                 |
| chaos                   | 104 ms                                                 | 70.2 ms: 1.48x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 82.7 ms: 1.42x faster                                 |
| deltablue               | 7.39 ms                                                | 3.70 ms: 2.00x faster                                 |
| django_template         | 46.3 ms                                                | 34.3 ms: 1.35x faster                                 |
| dulwich_log             | 75.5 ms                                                | 63.8 ms: 1.18x faster                                 |
| fannkuch                | 477 ms                                                 | 401 ms: 1.19x faster                                  |
| float                   | 108 ms                                                 | 74.4 ms: 1.45x faster                                 |
| go                      | 226 ms                                                 | 143 ms: 1.59x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.84 ms: 1.38x faster                                 |
| html5lib                | 85.8 ms                                                | 65.3 ms: 1.31x faster                                 |
| json                    | 5.35 ms                                                | 5.07 ms: 1.06x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.5 ms: 1.08x faster                                 |
| json_loads              | 28.9 us                                                | 28.1 us: 1.03x faster                                 |
| logging_format          | 8.92 us                                                | 6.35 us: 1.40x faster                                 |
| logging_silent          | 173 ns                                                 | 104 ns: 1.67x faster                                  |
| logging_simple          | 8.06 us                                                | 5.80 us: 1.39x faster                                 |
| mako                    | 14.3 ms                                                | 10.2 ms: 1.40x faster                                 |
| meteor_contest          | 114 ms                                                 | 107 ms: 1.07x faster                                  |
| nbody                   | 136 ms                                                 | 95.2 ms: 1.43x faster                                 |
| nqueens                 | 99.3 ms                                                | 85.2 ms: 1.17x faster                                 |
| pathlib                 | 20.0 ms                                                | 18.5 ms: 1.08x faster                                 |
| pickle                  | 10.1 us                                                | 9.55 us: 1.06x faster                                 |
| pickle_dict             | 28.3 us                                                | 27.6 us: 1.02x faster                                 |
| pickle_list             | 4.50 us                                                | 4.57 us: 1.01x slower                                 |
| pickle_pure_python      | 453 us                                                 | 311 us: 1.46x faster                                  |
| pidigits                | 190 ms                                                 | 197 ms: 1.04x slower                                  |
| pycparser               | 1.51 sec                                               | 1.24 sec: 1.22x faster                                |
| pyflate                 | 675 ms                                                 | 438 ms: 1.54x faster                                  |
| python_startup          | 13.9 ms                                                | 8.07 ms: 1.73x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 5.98 ms: 1.04x slower                                 |
| raytrace                | 461 ms                                                 | 306 ms: 1.51x faster                                  |
| regex_compile           | 174 ms                                                 | 137 ms: 1.26x faster                                  |
| regex_dna               | 214 ms                                                 | 231 ms: 1.08x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.34 ms: 1.04x slower                                 |
| regex_v8                | 25.0 ms                                                | 25.9 ms: 1.04x slower                                 |
| richards                | 71.4 ms                                                | 47.5 ms: 1.50x faster                                 |
| scimark_fft             | 414 ms                                                 | 335 ms: 1.24x faster                                  |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.46x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 70.8 ms: 1.48x faster                                 |
| scimark_sor             | 193 ms                                                 | 123 ms: 1.57x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.85 ms: 1.13x faster                                 |
| spectral_norm           | 148 ms                                                 | 105 ms: 1.42x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.51 us: 1.16x faster                                 |
| sympy_expand            | 537 ms                                                 | 476 ms: 1.13x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                 |
| sympy_sum               | 183 ms                                                 | 160 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 287 ms: 1.13x faster                                  |
| telco                   | 6.68 ms                                                | 6.59 ms: 1.01x faster                                 |
| thrift                  | 1.03 ms                                                | 762 us: 1.35x faster                                  |
| tornado_http            | 128 ms                                                 | 95.4 ms: 1.35x faster                                 |
| unpack_sequence         | 59.5 ns                                                | 44.9 ns: 1.32x faster                                 |
| unpickle_list           | 4.99 us                                                | 4.97 us: 1.01x faster                                 |
| unpickle_pure_python    | 297 us                                                 | 231 us: 1.29x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 157 ms: 1.04x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 104 ms: 1.07x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 78.5 ms: 1.19x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 55.2 ms: 1.35x faster                                 |
| Geometric mean          | (ref)                                                  | 1.24x faster                                          |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
