Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 246 ms: 1.05x faster                                   |
| chameleon      | 6.41 ms                                                | 6.38 ms: 1.00x faster                                  |
| html5lib       | 63.2 ms                                                | 59.3 ms: 1.07x faster                                  |
| tornado_http   | 96.6 ms                                                | 92.8 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.0 ms: 1.06x faster                                  |
| nbody          | 95.0 ms                                                | 96.2 ms: 1.01x slower                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.03x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna      | 203 ms                                                 | 204 ms: 1.01x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.32 ms: 1.01x faster                                  |
| regex_v8       | 22.3 ms                                                | 21.3 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.56 ms: 1.32x faster                                  |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                  |
| pickle               | 9.79 us                                                | 10.1 us: 1.03x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.9 us: 1.02x faster                                  |
| pickle_list          | 4.17 us                                                | 4.06 us: 1.03x faster                                  |
| pickle_pure_python   | 304 us                                                 | 285 us: 1.07x faster                                   |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 157 ms: 1.01x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.3 ms: 1.01x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 52.9 ms: 1.02x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (3): unpickle, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.35 ms: 1.00x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.05 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text    | 22.1 ms                                                | 20.7 ms: 1.07x faster                                  |
| genshi_xml     | 52.1 ms                                                | 48.4 ms: 1.08x faster                                  |
| mako           | 9.85 ms                                                | 9.35 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221002-linux-x86_64-python-main-3.12.0a1+-8baef8a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 246 ms: 1.05x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                  |
| async_tree_none         | 529 ms                                                 | 512 ms: 1.03x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 730 ms: 1.03x faster                                   |
| async_tree_memoization  | 625 ms                                                 | 640 ms: 1.02x slower                                   |
| chameleon               | 6.41 ms                                                | 6.38 ms: 1.00x faster                                  |
| chaos                   | 68.6 ms                                                | 66.4 ms: 1.03x faster                                  |
| coroutines              | 26.1 ms                                                | 23.9 ms: 1.09x faster                                  |
| coverage                | 101 ms                                                 | 96.6 ms: 1.04x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.8 ms: 1.01x faster                                  |
| deepcopy                | 344 us                                                 | 324 us: 1.06x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.86 us: 1.04x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 33.6 us: 1.09x faster                                  |
| deltablue               | 3.64 ms                                                | 3.26 ms: 1.12x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.3 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                   |
| float                   | 76.3 ms                                                | 72.0 ms: 1.06x faster                                  |
| genshi_text             | 22.1 ms                                                | 20.7 ms: 1.07x faster                                  |
| genshi_xml              | 52.1 ms                                                | 48.4 ms: 1.08x faster                                  |
| go                      | 143 ms                                                 | 132 ms: 1.09x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.00 ms: 1.06x faster                                  |
| html5lib                | 63.2 ms                                                | 59.3 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.51 ms: 1.10x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.56 ms: 1.32x faster                                  |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                  |
| logging_format          | 6.62 us                                                | 6.39 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 92.6 ns: 1.06x faster                                  |
| logging_simple          | 6.06 us                                                | 5.75 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.35 ms: 1.05x faster                                  |
| mdp                     | 2.62 sec                                               | 2.45 sec: 1.07x faster                                 |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.02x faster                                   |
| mypy                    | 669 ms                                                 | 635 ms: 1.05x faster                                   |
| nbody                   | 95.0 ms                                                | 96.2 ms: 1.01x slower                                  |
| nqueens                 | 85.0 ms                                                | 79.3 ms: 1.07x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.6 ms: 1.03x faster                                  |
| pickle                  | 9.79 us                                                | 10.1 us: 1.03x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.9 us: 1.02x faster                                  |
| pickle_list             | 4.17 us                                                | 4.06 us: 1.03x faster                                  |
| pickle_pure_python      | 304 us                                                 | 285 us: 1.07x faster                                   |
| pidigits                | 199 ms                                                 | 193 ms: 1.03x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 670 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.06x faster                                 |
| pyflate                 | 417 ms                                                 | 400 ms: 1.04x faster                                   |
| pylint                  | 463 ms                                                 | 447 ms: 1.03x faster                                   |
| python_startup          | 8.36 ms                                                | 8.35 ms: 1.00x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.05 ms: 1.01x slower                                  |
| raytrace                | 290 ms                                                 | 278 ms: 1.04x faster                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna               | 203 ms                                                 | 204 ms: 1.01x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.32 ms: 1.01x faster                                  |
| regex_v8                | 22.3 ms                                                | 21.3 ms: 1.04x faster                                  |
| richards                | 46.2 ms                                                | 44.2 ms: 1.04x faster                                  |
| scimark_fft             | 329 ms                                                 | 317 ms: 1.04x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.6 ms: 1.04x faster                                  |
| scimark_sor             | 115 ms                                                 | 105 ms: 1.10x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.17 ms: 1.06x faster                                  |
| spectral_norm           | 99.9 ms                                                | 92.3 ms: 1.08x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.32 ms: 1.03x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.61 ms: 1.03x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.6 ms: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.57 us: 1.03x slower                                  |
| sympy_expand            | 472 ms                                                 | 453 ms: 1.04x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 163 ms: 1.02x faster                                   |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.33 ms: 1.05x faster                                  |
| thrift                  | 752 us                                                 | 744 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 92.8 ms: 1.04x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 157 ms: 1.01x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.3 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 52.9 ms: 1.02x faster                                  |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (8): async_tree_io, django_template, generators, scimark_lu, unpack_sequence, unpickle, unpickle_list, xml_etree_iterparse
Ignored benchmarks (7) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
