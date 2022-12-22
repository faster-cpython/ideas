Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.03x faster                                   |
| chameleon      | 6.41 ms                                                | 6.28 ms: 1.02x faster                                  |
| tornado_http   | 96.6 ms                                                | 91.3 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.0 ms: 1.06x faster                                  |
| nbody          | 95.0 ms                                                | 88.8 ms: 1.07x faster                                  |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna      | 203 ms                                                 | 197 ms: 1.03x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.47 ms: 1.03x slower                                  |
| regex_v8       | 22.3 ms                                                | 20.9 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 11.9 ms: 1.07x faster                                  |
| json_loads           | 26.2 us                                                | 24.3 us: 1.08x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.06x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.6 us: 1.03x faster                                  |
| pickle_list          | 4.17 us                                                | 4.24 us: 1.02x slower                                  |
| pickle_pure_python   | 304 us                                                 | 286 us: 1.06x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.08 us: 1.02x slower                                  |
| unpickle_pure_python | 225 us                                                 | 202 us: 1.12x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 106 ms: 1.03x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.2 ms: 1.01x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 52.2 ms: 1.03x faster                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.17 ms: 1.02x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.02 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.1 ms: 1.01x faster                                  |
| mako            | 9.85 ms                                                | 9.33 ms: 1.06x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 249 ms: 1.03x faster                                   |
| chameleon               | 6.41 ms                                                | 6.28 ms: 1.02x faster                                  |
| chaos                   | 68.6 ms                                                | 66.2 ms: 1.04x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.9 ms: 1.01x faster                                  |
| deltablue               | 3.64 ms                                                | 3.21 ms: 1.13x faster                                  |
| django_template         | 32.5 ms                                                | 32.1 ms: 1.01x faster                                  |
| dulwich_log             | 63.9 ms                                                | 60.8 ms: 1.05x faster                                  |
| fannkuch                | 388 ms                                                 | 373 ms: 1.04x faster                                   |
| float                   | 76.3 ms                                                | 72.0 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.05 ms: 1.05x faster                                  |
| json                    | 4.95 ms                                                | 4.61 ms: 1.07x faster                                  |
| json_dumps              | 12.7 ms                                                | 11.9 ms: 1.07x faster                                  |
| json_loads              | 26.2 us                                                | 24.3 us: 1.08x faster                                  |
| logging_format          | 6.62 us                                                | 6.22 us: 1.06x faster                                  |
| logging_silent          | 98.5 ns                                                | 91.9 ns: 1.07x faster                                  |
| logging_simple          | 6.06 us                                                | 5.61 us: 1.08x faster                                  |
| mako                    | 9.85 ms                                                | 9.33 ms: 1.06x faster                                  |
| meteor_contest          | 105 ms                                                 | 101 ms: 1.03x faster                                   |
| nbody                   | 95.0 ms                                                | 88.8 ms: 1.07x faster                                  |
| nqueens                 | 85.0 ms                                                | 78.8 ms: 1.08x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.06x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.6 us: 1.03x faster                                  |
| pickle_list             | 4.17 us                                                | 4.24 us: 1.02x slower                                  |
| pickle_pure_python      | 304 us                                                 | 286 us: 1.06x faster                                   |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| pycparser               | 1.17 sec                                               | 1.05 sec: 1.12x faster                                 |
| pyflate                 | 417 ms                                                 | 401 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.17 ms: 1.02x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.02 ms: 1.01x slower                                  |
| raytrace                | 290 ms                                                 | 285 ms: 1.02x faster                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna               | 203 ms                                                 | 197 ms: 1.03x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.47 ms: 1.03x slower                                  |
| regex_v8                | 22.3 ms                                                | 20.9 ms: 1.07x faster                                  |
| richards                | 46.2 ms                                                | 44.7 ms: 1.03x faster                                  |
| scimark_fft             | 329 ms                                                 | 313 ms: 1.05x faster                                   |
| scimark_lu              | 107 ms                                                 | 105 ms: 1.02x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.1 ms: 1.05x faster                                  |
| scimark_sor             | 115 ms                                                 | 117 ms: 1.02x slower                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.04 ms: 1.09x faster                                  |
| spectral_norm           | 99.9 ms                                                | 93.4 ms: 1.07x faster                                  |
| sqlite_synth            | 2.49 us                                                | 2.60 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 452 ms: 1.04x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.1 ms: 1.04x faster                                  |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                   |
| sympy_str               | 287 ms                                                 | 278 ms: 1.04x faster                                   |
| telco                   | 6.62 ms                                                | 6.50 ms: 1.02x faster                                  |
| thrift                  | 752 us                                                 | 739 us: 1.02x faster                                   |
| tornado_http            | 96.6 ms                                                | 91.3 ms: 1.06x faster                                  |
| unpickle_list           | 4.95 us                                                | 5.08 us: 1.02x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 202 us: 1.12x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 106 ms: 1.03x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.2 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 52.2 ms: 1.03x faster                                  |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (4): html5lib, unpack_sequence, unpickle, xml_etree_parse
Ignored benchmarks (30) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
