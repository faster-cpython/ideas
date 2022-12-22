Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 267 ms: 1.04x slower                                  |
| chameleon      | 6.41 ms                                                | 6.95 ms: 1.09x slower                                 |
| html5lib       | 63.2 ms                                                | 67.9 ms: 1.08x slower                                 |
| tornado_http   | 96.6 ms                                                | 106 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 77.5 ms: 1.02x slower                                 |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 140 ms: 1.03x slower                                  |
| regex_dna      | 203 ms                                                 | 213 ms: 1.05x slower                                  |
| regex_effbot   | 3.36 ms                                                | 3.14 ms: 1.07x faster                                 |
| regex_v8       | 22.3 ms                                                | 24.0 ms: 1.08x slower                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.2 ms: 1.04x faster                                 |
| json_loads           | 26.2 us                                                | 26.7 us: 1.02x slower                                 |
| pickle               | 9.79 us                                                | 9.93 us: 1.01x slower                                 |
| pickle_dict          | 31.4 us                                                | 28.1 us: 1.12x faster                                 |
| pickle_list          | 4.17 us                                                | 4.47 us: 1.07x slower                                 |
| pickle_pure_python   | 304 us                                                 | 334 us: 1.10x slower                                  |
| unpickle_list        | 4.95 us                                                | 5.26 us: 1.06x slower                                 |
| unpickle_pure_python | 225 us                                                 | 249 us: 1.11x slower                                  |
| xml_etree_parse      | 158 ms                                                 | 153 ms: 1.04x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 106 ms: 1.03x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 79.6 ms: 1.04x slower                                 |
| xml_etree_process    | 53.8 ms                                                | 57.0 ms: 1.06x slower                                 |
| Geometric mean       | (ref)                                                  | 1.03x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.13 ms: 1.03x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 5.92 ms: 1.01x faster                                 |
| Geometric mean         | (ref)                                                  | 1.02x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 32.5 ms                                                | 35.4 ms: 1.09x slower                                 |
| mako            | 9.85 ms                                                | 10.5 ms: 1.06x slower                                 |
| Geometric mean  | (ref)                                                  | 1.08x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 267 ms: 1.04x slower                                  |
| chameleon               | 6.41 ms                                                | 6.95 ms: 1.09x slower                                 |
| chaos                   | 68.6 ms                                                | 74.9 ms: 1.09x slower                                 |
| crypto_pyaes            | 73.9 ms                                                | 83.8 ms: 1.13x slower                                 |
| deltablue               | 3.64 ms                                                | 4.13 ms: 1.13x slower                                 |
| django_template         | 32.5 ms                                                | 35.4 ms: 1.09x slower                                 |
| dulwich_log             | 63.9 ms                                                | 65.7 ms: 1.03x slower                                 |
| fannkuch                | 388 ms                                                 | 400 ms: 1.03x slower                                  |
| float                   | 76.3 ms                                                | 77.5 ms: 1.02x slower                                 |
| go                      | 143 ms                                                 | 147 ms: 1.03x slower                                  |
| hexiom                  | 6.35 ms                                                | 6.76 ms: 1.06x slower                                 |
| html5lib                | 63.2 ms                                                | 67.9 ms: 1.08x slower                                 |
| json                    | 4.95 ms                                                | 4.84 ms: 1.02x faster                                 |
| json_dumps              | 12.7 ms                                                | 12.2 ms: 1.04x faster                                 |
| json_loads              | 26.2 us                                                | 26.7 us: 1.02x slower                                 |
| logging_format          | 6.62 us                                                | 6.37 us: 1.04x faster                                 |
| logging_silent          | 98.5 ns                                                | 113 ns: 1.15x slower                                  |
| logging_simple          | 6.06 us                                                | 5.84 us: 1.04x faster                                 |
| mako                    | 9.85 ms                                                | 10.5 ms: 1.06x slower                                 |
| nqueens                 | 85.0 ms                                                | 87.2 ms: 1.03x slower                                 |
| pathlib                 | 18.2 ms                                                | 18.5 ms: 1.02x slower                                 |
| pickle                  | 9.79 us                                                | 9.93 us: 1.01x slower                                 |
| pickle_dict             | 31.4 us                                                | 28.1 us: 1.12x faster                                 |
| pickle_list             | 4.17 us                                                | 4.47 us: 1.07x slower                                 |
| pickle_pure_python      | 304 us                                                 | 334 us: 1.10x slower                                  |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                  |
| pycparser               | 1.17 sec                                               | 1.19 sec: 1.02x slower                                |
| pyflate                 | 417 ms                                                 | 459 ms: 1.10x slower                                  |
| python_startup          | 8.36 ms                                                | 8.13 ms: 1.03x faster                                 |
| python_startup_no_site  | 5.96 ms                                                | 5.92 ms: 1.01x faster                                 |
| raytrace                | 290 ms                                                 | 321 ms: 1.10x slower                                  |
| regex_compile           | 136 ms                                                 | 140 ms: 1.03x slower                                  |
| regex_dna               | 203 ms                                                 | 213 ms: 1.05x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.14 ms: 1.07x faster                                 |
| regex_v8                | 22.3 ms                                                | 24.0 ms: 1.08x slower                                 |
| richards                | 46.2 ms                                                | 50.8 ms: 1.10x slower                                 |
| scimark_fft             | 329 ms                                                 | 347 ms: 1.05x slower                                  |
| scimark_lu              | 107 ms                                                 | 120 ms: 1.12x slower                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 72.6 ms: 1.06x slower                                 |
| scimark_sor             | 115 ms                                                 | 129 ms: 1.12x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 5.14 ms: 1.17x slower                                 |
| spectral_norm           | 99.9 ms                                                | 104 ms: 1.04x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.71 us: 1.09x slower                                 |
| sympy_expand            | 472 ms                                                 | 503 ms: 1.07x slower                                  |
| sympy_integrate         | 20.9 ms                                                | 21.3 ms: 1.02x slower                                 |
| sympy_sum               | 166 ms                                                 | 170 ms: 1.02x slower                                  |
| sympy_str               | 287 ms                                                 | 304 ms: 1.06x slower                                  |
| telco                   | 6.62 ms                                                | 6.70 ms: 1.01x slower                                 |
| thrift                  | 752 us                                                 | 815 us: 1.08x slower                                  |
| tornado_http            | 96.6 ms                                                | 106 ms: 1.09x slower                                  |
| unpack_sequence         | 43.4 ns                                                | 46.0 ns: 1.06x slower                                 |
| unpickle_list           | 4.95 us                                                | 5.26 us: 1.06x slower                                 |
| unpickle_pure_python    | 225 us                                                 | 249 us: 1.11x slower                                  |
| xml_etree_parse         | 158 ms                                                 | 153 ms: 1.04x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 106 ms: 1.03x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 79.6 ms: 1.04x slower                                 |
| xml_etree_process       | 53.8 ms                                                | 57.0 ms: 1.06x slower                                 |
| Geometric mean          | (ref)                                                  | 1.04x slower                                          |

Benchmark hidden because not significant (3): meteor_contest, nbody, unpickle
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
