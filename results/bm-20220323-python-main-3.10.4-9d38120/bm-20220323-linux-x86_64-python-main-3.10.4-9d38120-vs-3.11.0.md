Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------:|
| 2to3           | 257 ms                                                 | 332 ms: 1.29x slower                                |
| chameleon      | 6.41 ms                                                | 8.76 ms: 1.37x slower                               |
| html5lib       | 63.2 ms                                                | 85.1 ms: 1.35x slower                               |
| tornado_http   | 96.6 ms                                                | 127 ms: 1.32x slower                                |
| Geometric mean | (ref)                                                  | 1.33x slower                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------:|
| float          | 76.3 ms                                                | 107 ms: 1.41x slower                                |
| nbody          | 95.0 ms                                                | 135 ms: 1.42x slower                                |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                |
| Geometric mean | (ref)                                                  | 1.24x slower                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 178 ms: 1.31x slower                                |
| regex_dna      | 203 ms                                                 | 214 ms: 1.05x slower                                |
| regex_effbot   | 3.36 ms                                                | 3.24 ms: 1.04x faster                               |
| regex_v8       | 22.3 ms                                                | 25.7 ms: 1.15x slower                               |
| Geometric mean | (ref)                                                  | 1.11x slower                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 13.2 ms: 1.04x slower                               |
| json_loads           | 26.2 us                                                | 31.1 us: 1.19x slower                               |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                               |
| pickle_dict          | 31.4 us                                                | 27.2 us: 1.16x faster                               |
| pickle_list          | 4.17 us                                                | 4.40 us: 1.05x slower                               |
| pickle_pure_python   | 304 us                                                 | 449 us: 1.48x slower                                |
| unpickle             | 13.3 us                                                | 14.4 us: 1.08x slower                               |
| unpickle_list        | 4.95 us                                                | 4.90 us: 1.01x faster                               |
| unpickle_pure_python | 225 us                                                 | 298 us: 1.32x slower                                |
| xml_etree_parse      | 158 ms                                                 | 162 ms: 1.03x slower                                |
| xml_etree_iterparse  | 103 ms                                                 | 110 ms: 1.07x slower                                |
| xml_etree_generate   | 76.2 ms                                                | 92.4 ms: 1.21x slower                               |
| xml_etree_process    | 53.8 ms                                                | 72.6 ms: 1.35x slower                               |
| Geometric mean       | (ref)                                                  | 1.12x slower                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.21 ms: 1.10x slower                               |
| python_startup_no_site | 5.96 ms                                                | 5.97 ms: 1.00x slower                               |
| Geometric mean         | (ref)                                                  | 1.05x slower                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------:|
| django_template | 32.5 ms                                                | 45.7 ms: 1.41x slower                               |
| genshi_text     | 22.1 ms                                                | 30.6 ms: 1.38x slower                               |
| genshi_xml      | 52.1 ms                                                | 64.1 ms: 1.23x slower                               |
| mako            | 9.85 ms                                                | 14.7 ms: 1.50x slower                               |
| Geometric mean  | (ref)                                                  | 1.38x slower                                        |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 332 ms: 1.29x slower                                |
| chameleon               | 6.41 ms                                                | 8.76 ms: 1.37x slower                               |
| chaos                   | 68.6 ms                                                | 107 ms: 1.56x slower                                |
| crypto_pyaes            | 73.9 ms                                                | 116 ms: 1.58x slower                                |
| deltablue               | 3.64 ms                                                | 7.32 ms: 2.01x slower                               |
| django_template         | 32.5 ms                                                | 45.7 ms: 1.41x slower                               |
| dulwich_log             | 63.9 ms                                                | 75.2 ms: 1.18x slower                               |
| fannkuch                | 388 ms                                                 | 483 ms: 1.24x slower                                |
| float                   | 76.3 ms                                                | 107 ms: 1.41x slower                                |
| genshi_text             | 22.1 ms                                                | 30.6 ms: 1.38x slower                               |
| genshi_xml              | 52.1 ms                                                | 64.1 ms: 1.23x slower                               |
| go                      | 143 ms                                                 | 227 ms: 1.58x slower                                |
| hexiom                  | 6.35 ms                                                | 9.29 ms: 1.46x slower                               |
| html5lib                | 63.2 ms                                                | 85.1 ms: 1.35x slower                               |
| json                    | 4.95 ms                                                | 5.55 ms: 1.12x slower                               |
| json_dumps              | 12.7 ms                                                | 13.2 ms: 1.04x slower                               |
| json_loads              | 26.2 us                                                | 31.1 us: 1.19x slower                               |
| logging_format          | 6.62 us                                                | 8.78 us: 1.33x slower                               |
| logging_silent          | 98.5 ns                                                | 168 ns: 1.70x slower                                |
| logging_simple          | 6.06 us                                                | 8.07 us: 1.33x slower                               |
| mako                    | 9.85 ms                                                | 14.7 ms: 1.50x slower                               |
| meteor_contest          | 105 ms                                                 | 114 ms: 1.09x slower                                |
| nbody                   | 95.0 ms                                                | 135 ms: 1.42x slower                                |
| nqueens                 | 85.0 ms                                                | 98.4 ms: 1.16x slower                               |
| pathlib                 | 18.2 ms                                                | 20.1 ms: 1.11x slower                               |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                               |
| pickle_dict             | 31.4 us                                                | 27.2 us: 1.16x faster                               |
| pickle_list             | 4.17 us                                                | 4.40 us: 1.05x slower                               |
| pickle_pure_python      | 304 us                                                 | 449 us: 1.48x slower                                |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                |
| pycparser               | 1.17 sec                                               | 1.52 sec: 1.30x slower                              |
| pyflate                 | 417 ms                                                 | 664 ms: 1.59x slower                                |
| pylint                  | 463 ms                                                 | 512 ms: 1.11x slower                                |
| python_startup          | 8.36 ms                                                | 9.21 ms: 1.10x slower                               |
| python_startup_no_site  | 5.96 ms                                                | 5.97 ms: 1.00x slower                               |
| raytrace                | 290 ms                                                 | 463 ms: 1.59x slower                                |
| regex_compile           | 136 ms                                                 | 178 ms: 1.31x slower                                |
| regex_dna               | 203 ms                                                 | 214 ms: 1.05x slower                                |
| regex_effbot            | 3.36 ms                                                | 3.24 ms: 1.04x faster                               |
| regex_v8                | 22.3 ms                                                | 25.7 ms: 1.15x slower                               |
| richards                | 46.2 ms                                                | 68.9 ms: 1.49x slower                               |
| scimark_fft             | 329 ms                                                 | 419 ms: 1.27x slower                                |
| scimark_lu              | 107 ms                                                 | 160 ms: 1.49x slower                                |
| scimark_monte_carlo     | 68.3 ms                                                | 107 ms: 1.57x slower                                |
| scimark_sor             | 115 ms                                                 | 196 ms: 1.70x slower                                |
| scimark_sparse_mat_mult | 4.40 ms                                                | 5.45 ms: 1.24x slower                               |
| spectral_norm           | 99.9 ms                                                | 144 ms: 1.44x slower                                |
| sqlite_synth            | 2.49 us                                                | 2.92 us: 1.17x slower                               |
| sympy_expand            | 472 ms                                                 | 538 ms: 1.14x slower                                |
| sympy_integrate         | 20.9 ms                                                | 24.1 ms: 1.15x slower                               |
| sympy_sum               | 166 ms                                                 | 184 ms: 1.11x slower                                |
| sympy_str               | 287 ms                                                 | 325 ms: 1.13x slower                                |
| thrift                  | 752 us                                                 | 1.01 ms: 1.35x slower                               |
| tornado_http            | 96.6 ms                                                | 127 ms: 1.32x slower                                |
| unpack_sequence         | 43.4 ns                                                | 56.1 ns: 1.29x slower                               |
| unpickle                | 13.3 us                                                | 14.4 us: 1.08x slower                               |
| unpickle_list           | 4.95 us                                                | 4.90 us: 1.01x faster                               |
| unpickle_pure_python    | 225 us                                                 | 298 us: 1.32x slower                                |
| xml_etree_parse         | 158 ms                                                 | 162 ms: 1.03x slower                                |
| xml_etree_iterparse     | 103 ms                                                 | 110 ms: 1.07x slower                                |
| xml_etree_generate      | 76.2 ms                                                | 92.4 ms: 1.21x slower                               |
| xml_etree_process       | 53.8 ms                                                | 72.6 ms: 1.35x slower                               |
| Geometric mean          | (ref)                                                  | 1.26x slower                                        |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (27) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
