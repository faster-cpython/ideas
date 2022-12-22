Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.45 ms: 1.37x faster                                  |
| html5lib       | 85.8 ms                                                | 62.0 ms: 1.38x faster                                  |
| tornado_http   | 128 ms                                                 | 92.1 ms: 1.39x faster                                  |
| Geometric mean | (ref)                                                  | 1.37x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 71.1 ms: 1.51x faster                                  |
| nbody          | 136 ms                                                 | 94.8 ms: 1.44x faster                                  |
| pidigits       | 190 ms                                                 | 194 ms: 1.02x slower                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna      | 214 ms                                                 | 208 ms: 1.03x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.61 ms: 1.12x slower                                  |
| regex_v8       | 25.0 ms                                                | 21.3 ms: 1.17x faster                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.0 ms: 1.12x faster                                  |
| json_loads           | 28.9 us                                                | 24.5 us: 1.18x faster                                  |
| pickle_dict          | 28.3 us                                                | 30.1 us: 1.06x slower                                  |
| pickle_list          | 4.50 us                                                | 4.15 us: 1.08x faster                                  |
| pickle_pure_python   | 453 us                                                 | 294 us: 1.54x faster                                   |
| unpickle             | 14.3 us                                                | 13.4 us: 1.06x faster                                  |
| unpickle_list        | 4.99 us                                                | 4.91 us: 1.02x faster                                  |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 155 ms: 1.05x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.0 ms: 1.24x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 52.0 ms: 1.43x faster                                  |
| Geometric mean       | (ref)                                                  | 1.16x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.26 ms: 1.69x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.10 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 31.6 ms: 1.46x faster                                  |
| mako            | 14.3 ms                                                | 9.46 ms: 1.51x faster                                  |
| Geometric mean  | (ref)                                                  | 1.49x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220626-linux-x86_64-python-main-3.12.0a1+-38612a0 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon               | 8.86 ms                                                | 6.45 ms: 1.37x faster                                  |
| chaos                   | 104 ms                                                 | 63.8 ms: 1.63x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 73.7 ms: 1.59x faster                                  |
| deltablue               | 7.39 ms                                                | 3.24 ms: 2.29x faster                                  |
| django_template         | 46.3 ms                                                | 31.6 ms: 1.46x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.7 ms: 1.22x faster                                  |
| fannkuch                | 477 ms                                                 | 376 ms: 1.27x faster                                   |
| float                   | 108 ms                                                 | 71.1 ms: 1.51x faster                                  |
| go                      | 226 ms                                                 | 128 ms: 1.76x faster                                   |
| hexiom                  | 9.42 ms                                                | 5.94 ms: 1.58x faster                                  |
| html5lib                | 85.8 ms                                                | 62.0 ms: 1.38x faster                                  |
| json                    | 5.35 ms                                                | 4.72 ms: 1.13x faster                                  |
| json_dumps              | 13.5 ms                                                | 12.0 ms: 1.12x faster                                  |
| json_loads              | 28.9 us                                                | 24.5 us: 1.18x faster                                  |
| logging_format          | 8.92 us                                                | 6.40 us: 1.40x faster                                  |
| logging_silent          | 173 ns                                                 | 89.6 ns: 1.93x faster                                  |
| logging_simple          | 8.06 us                                                | 5.77 us: 1.40x faster                                  |
| mako                    | 14.3 ms                                                | 9.46 ms: 1.51x faster                                  |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.11x faster                                   |
| nbody                   | 136 ms                                                 | 94.8 ms: 1.44x faster                                  |
| nqueens                 | 99.3 ms                                                | 82.2 ms: 1.21x faster                                  |
| pathlib                 | 20.0 ms                                                | 18.1 ms: 1.10x faster                                  |
| pickle_dict             | 28.3 us                                                | 30.1 us: 1.06x slower                                  |
| pickle_list             | 4.50 us                                                | 4.15 us: 1.08x faster                                  |
| pickle_pure_python      | 453 us                                                 | 294 us: 1.54x faster                                   |
| pidigits                | 190 ms                                                 | 194 ms: 1.02x slower                                   |
| pycparser               | 1.51 sec                                               | 1.05 sec: 1.44x faster                                 |
| pyflate                 | 675 ms                                                 | 400 ms: 1.69x faster                                   |
| python_startup          | 13.9 ms                                                | 8.26 ms: 1.69x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.10 ms: 1.06x slower                                  |
| raytrace                | 461 ms                                                 | 279 ms: 1.66x faster                                   |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna               | 214 ms                                                 | 208 ms: 1.03x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.61 ms: 1.12x slower                                  |
| regex_v8                | 25.0 ms                                                | 21.3 ms: 1.17x faster                                  |
| richards                | 71.4 ms                                                | 45.4 ms: 1.57x faster                                  |
| scimark_fft             | 414 ms                                                 | 304 ms: 1.36x faster                                   |
| scimark_lu              | 158 ms                                                 | 104 ms: 1.53x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 62.4 ms: 1.68x faster                                  |
| scimark_sor             | 193 ms                                                 | 110 ms: 1.76x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.89 ms: 1.41x faster                                  |
| spectral_norm           | 148 ms                                                 | 92.8 ms: 1.60x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.57 us: 1.13x faster                                  |
| sympy_expand            | 537 ms                                                 | 451 ms: 1.19x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.2 ms: 1.19x faster                                  |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                   |
| sympy_str               | 324 ms                                                 | 277 ms: 1.17x faster                                   |
| telco                   | 6.68 ms                                                | 6.44 ms: 1.04x faster                                  |
| thrift                  | 1.03 ms                                                | 745 us: 1.38x faster                                   |
| tornado_http            | 128 ms                                                 | 92.1 ms: 1.39x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 42.8 ns: 1.39x faster                                  |
| unpickle                | 14.3 us                                                | 13.4 us: 1.06x faster                                  |
| unpickle_list           | 4.99 us                                                | 4.91 us: 1.02x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.50x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 155 ms: 1.05x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.0 ms: 1.24x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 52.0 ms: 1.43x faster                                  |
| Geometric mean          | (ref)                                                  | 1.32x faster                                           |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
