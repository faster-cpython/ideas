Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 264 ms: 1.03x slower                                  |
| chameleon      | 6.41 ms                                                | 6.87 ms: 1.07x slower                                 |
| html5lib       | 63.2 ms                                                | 65.3 ms: 1.03x slower                                 |
| tornado_http   | 96.6 ms                                                | 95.4 ms: 1.01x faster                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 74.4 ms: 1.03x faster                                 |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 137 ms: 1.01x slower                                  |
| regex_dna      | 203 ms                                                 | 231 ms: 1.14x slower                                  |
| regex_effbot   | 3.36 ms                                                | 3.34 ms: 1.01x faster                                 |
| regex_v8       | 22.3 ms                                                | 25.9 ms: 1.16x slower                                 |
| Geometric mean | (ref)                                                  | 1.07x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.5 ms: 1.01x faster                                 |
| json_loads           | 26.2 us                                                | 28.1 us: 1.07x slower                                 |
| pickle               | 9.79 us                                                | 9.55 us: 1.02x faster                                 |
| pickle_dict          | 31.4 us                                                | 27.6 us: 1.14x faster                                 |
| pickle_list          | 4.17 us                                                | 4.57 us: 1.09x slower                                 |
| pickle_pure_python   | 304 us                                                 | 311 us: 1.02x slower                                  |
| unpickle             | 13.3 us                                                | 14.1 us: 1.06x slower                                 |
| unpickle_pure_python | 225 us                                                 | 231 us: 1.02x slower                                  |
| xml_etree_parse      | 158 ms                                                 | 157 ms: 1.01x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 104 ms: 1.01x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 78.5 ms: 1.03x slower                                 |
| xml_etree_process    | 53.8 ms                                                | 55.2 ms: 1.03x slower                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                          |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.07 ms: 1.04x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 5.98 ms: 1.00x slower                                 |
| Geometric mean         | (ref)                                                  | 1.02x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 32.5 ms                                                | 34.3 ms: 1.06x slower                                 |
| mako            | 9.85 ms                                                | 10.2 ms: 1.03x slower                                 |
| Geometric mean  | (ref)                                                  | 1.04x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 264 ms: 1.03x slower                                  |
| chameleon               | 6.41 ms                                                | 6.87 ms: 1.07x slower                                 |
| chaos                   | 68.6 ms                                                | 70.2 ms: 1.02x slower                                 |
| crypto_pyaes            | 73.9 ms                                                | 82.7 ms: 1.12x slower                                 |
| deltablue               | 3.64 ms                                                | 3.70 ms: 1.01x slower                                 |
| django_template         | 32.5 ms                                                | 34.3 ms: 1.06x slower                                 |
| fannkuch                | 388 ms                                                 | 401 ms: 1.03x slower                                  |
| float                   | 76.3 ms                                                | 74.4 ms: 1.03x faster                                 |
| go                      | 143 ms                                                 | 143 ms: 1.01x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.84 ms: 1.08x slower                                 |
| html5lib                | 63.2 ms                                                | 65.3 ms: 1.03x slower                                 |
| json                    | 4.95 ms                                                | 5.07 ms: 1.02x slower                                 |
| json_dumps              | 12.7 ms                                                | 12.5 ms: 1.01x faster                                 |
| json_loads              | 26.2 us                                                | 28.1 us: 1.07x slower                                 |
| logging_format          | 6.62 us                                                | 6.35 us: 1.04x faster                                 |
| logging_silent          | 98.5 ns                                                | 104 ns: 1.05x slower                                  |
| logging_simple          | 6.06 us                                                | 5.80 us: 1.04x faster                                 |
| mako                    | 9.85 ms                                                | 10.2 ms: 1.03x slower                                 |
| meteor_contest          | 105 ms                                                 | 107 ms: 1.02x slower                                  |
| pathlib                 | 18.2 ms                                                | 18.5 ms: 1.02x slower                                 |
| pickle                  | 9.79 us                                                | 9.55 us: 1.02x faster                                 |
| pickle_dict             | 31.4 us                                                | 27.6 us: 1.14x faster                                 |
| pickle_list             | 4.17 us                                                | 4.57 us: 1.09x slower                                 |
| pickle_pure_python      | 304 us                                                 | 311 us: 1.02x slower                                  |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                  |
| pycparser               | 1.17 sec                                               | 1.24 sec: 1.06x slower                                |
| pyflate                 | 417 ms                                                 | 438 ms: 1.05x slower                                  |
| python_startup          | 8.36 ms                                                | 8.07 ms: 1.04x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 5.98 ms: 1.00x slower                                 |
| raytrace                | 290 ms                                                 | 306 ms: 1.05x slower                                  |
| regex_compile           | 136 ms                                                 | 137 ms: 1.01x slower                                  |
| regex_dna               | 203 ms                                                 | 231 ms: 1.14x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.34 ms: 1.01x faster                                 |
| regex_v8                | 22.3 ms                                                | 25.9 ms: 1.16x slower                                 |
| richards                | 46.2 ms                                                | 47.5 ms: 1.03x slower                                 |
| scimark_fft             | 329 ms                                                 | 335 ms: 1.02x slower                                  |
| scimark_lu              | 107 ms                                                 | 108 ms: 1.01x slower                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 70.8 ms: 1.04x slower                                 |
| scimark_sor             | 115 ms                                                 | 123 ms: 1.07x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.85 ms: 1.10x slower                                 |
| spectral_norm           | 99.9 ms                                                | 105 ms: 1.05x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.51 us: 1.01x slower                                 |
| sympy_expand            | 472 ms                                                 | 476 ms: 1.01x slower                                  |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                 |
| sympy_sum               | 166 ms                                                 | 160 ms: 1.04x faster                                  |
| thrift                  | 752 us                                                 | 762 us: 1.01x slower                                  |
| tornado_http            | 96.6 ms                                                | 95.4 ms: 1.01x faster                                 |
| unpack_sequence         | 43.4 ns                                                | 44.9 ns: 1.04x slower                                 |
| unpickle                | 13.3 us                                                | 14.1 us: 1.06x slower                                 |
| unpickle_pure_python    | 225 us                                                 | 231 us: 1.02x slower                                  |
| xml_etree_parse         | 158 ms                                                 | 157 ms: 1.01x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 104 ms: 1.01x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 78.5 ms: 1.03x slower                                 |
| xml_etree_process       | 53.8 ms                                                | 55.2 ms: 1.03x slower                                 |
| Geometric mean          | (ref)                                                  | 1.02x slower                                          |

Benchmark hidden because not significant (6): dulwich_log, nbody, nqueens, sympy_str, telco, unpickle_list
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
