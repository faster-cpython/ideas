Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.03x faster                                   |
| chameleon      | 6.41 ms                                                | 6.30 ms: 1.02x faster                                  |
| tornado_http   | 96.6 ms                                                | 91.3 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.4 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 90.5 ms: 1.05x faster                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.03x faster                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 126 ms: 1.08x faster                                   |
| regex_dna      | 203 ms                                                 | 207 ms: 1.02x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.54 ms: 1.05x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.1 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 11.8 ms: 1.07x faster                                  |
| json_loads           | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| pickle               | 9.79 us                                                | 10.5 us: 1.07x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.6 us: 1.01x slower                                  |
| pickle_list          | 4.17 us                                                | 4.12 us: 1.01x faster                                  |
| pickle_pure_python   | 304 us                                                 | 286 us: 1.06x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.04 us: 1.02x slower                                  |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 156 ms: 1.01x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 104 ms: 1.01x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.9 ms: 1.00x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.16 ms: 1.02x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.01 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 31.5 ms: 1.03x faster                                  |
| mako            | 9.85 ms                                                | 9.45 ms: 1.04x faster                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220710-linux-x86_64-python-main-3.12.0a1+-264b3dd |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 249 ms: 1.03x faster                                   |
| chameleon               | 6.41 ms                                                | 6.30 ms: 1.02x faster                                  |
| chaos                   | 68.6 ms                                                | 65.0 ms: 1.06x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.3 ms: 1.01x slower                                  |
| deltablue               | 3.64 ms                                                | 3.24 ms: 1.13x faster                                  |
| django_template         | 32.5 ms                                                | 31.5 ms: 1.03x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.2 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 378 ms: 1.03x faster                                   |
| float                   | 76.3 ms                                                | 72.4 ms: 1.05x faster                                  |
| go                      | 143 ms                                                 | 130 ms: 1.10x faster                                   |
| hexiom                  | 6.35 ms                                                | 5.92 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.69 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 11.8 ms: 1.07x faster                                  |
| json_loads              | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| logging_format          | 6.62 us                                                | 6.35 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 92.5 ns: 1.06x faster                                  |
| logging_simple          | 6.06 us                                                | 5.67 us: 1.07x faster                                  |
| mako                    | 9.85 ms                                                | 9.45 ms: 1.04x faster                                  |
| meteor_contest          | 105 ms                                                 | 101 ms: 1.04x faster                                   |
| nbody                   | 95.0 ms                                                | 90.5 ms: 1.05x faster                                  |
| nqueens                 | 85.0 ms                                                | 80.8 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 18.0 ms: 1.01x faster                                  |
| pickle                  | 9.79 us                                                | 10.5 us: 1.07x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.6 us: 1.01x slower                                  |
| pickle_list             | 4.17 us                                                | 4.12 us: 1.01x faster                                  |
| pickle_pure_python      | 304 us                                                 | 286 us: 1.06x faster                                   |
| pidigits                | 199 ms                                                 | 193 ms: 1.03x faster                                   |
| pycparser               | 1.17 sec                                               | 1.06 sec: 1.10x faster                                 |
| pyflate                 | 417 ms                                                 | 398 ms: 1.05x faster                                   |
| python_startup          | 8.36 ms                                                | 8.16 ms: 1.02x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.01 ms: 1.01x slower                                  |
| raytrace                | 290 ms                                                 | 286 ms: 1.01x faster                                   |
| regex_compile           | 136 ms                                                 | 126 ms: 1.08x faster                                   |
| regex_dna               | 203 ms                                                 | 207 ms: 1.02x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.54 ms: 1.05x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.1 ms: 1.01x faster                                  |
| richards                | 46.2 ms                                                | 45.0 ms: 1.03x faster                                  |
| scimark_fft             | 329 ms                                                 | 313 ms: 1.05x faster                                   |
| scimark_lu              | 107 ms                                                 | 104 ms: 1.03x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.6 ms: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 111 ms: 1.04x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.18 ms: 1.05x faster                                  |
| spectral_norm           | 99.9 ms                                                | 97.7 ms: 1.02x faster                                  |
| sqlite_synth            | 2.49 us                                                | 2.62 us: 1.05x slower                                  |
| sympy_expand            | 472 ms                                                 | 450 ms: 1.05x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.1 ms: 1.04x faster                                  |
| sympy_sum               | 166 ms                                                 | 158 ms: 1.05x faster                                   |
| sympy_str               | 287 ms                                                 | 279 ms: 1.03x faster                                   |
| telco                   | 6.62 ms                                                | 6.51 ms: 1.02x faster                                  |
| thrift                  | 752 us                                                 | 720 us: 1.04x faster                                   |
| tornado_http            | 96.6 ms                                                | 91.3 ms: 1.06x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 46.4 ns: 1.07x slower                                  |
| unpickle_list           | 4.95 us                                                | 5.04 us: 1.02x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 156 ms: 1.01x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 104 ms: 1.01x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.9 ms: 1.00x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (2): html5lib, unpickle
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
