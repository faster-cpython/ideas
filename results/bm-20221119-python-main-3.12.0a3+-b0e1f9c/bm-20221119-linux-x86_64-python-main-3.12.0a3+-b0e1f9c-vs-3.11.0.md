Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 245 ms: 1.05x faster                                   |
| chameleon      | 6.41 ms                                                | 6.49 ms: 1.01x slower                                  |
| html5lib       | 63.2 ms                                                | 59.1 ms: 1.07x faster                                  |
| tornado_http   | 96.6 ms                                                | 92.7 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.6 ms: 1.07x faster                                  |
| nbody          | 95.0 ms                                                | 94.1 ms: 1.01x faster                                  |
| pidigits       | 199 ms                                                 | 192 ms: 1.04x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna      | 203 ms                                                 | 213 ms: 1.05x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.77 ms: 1.12x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.2 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.42 ms: 1.34x faster                                  |
| json_loads           | 26.2 us                                                | 24.2 us: 1.09x faster                                  |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.0 us: 1.01x faster                                  |
| pickle_list          | 4.17 us                                                | 4.11 us: 1.02x faster                                  |
| pickle_pure_python   | 304 us                                                 | 283 us: 1.07x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.10 us: 1.03x slower                                  |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| xml_etree_process    | 53.8 ms                                                | 52.9 ms: 1.02x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (3): unpickle, xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.51 ms: 1.02x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.25 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.6 ms: 1.01x slower                                  |
| genshi_text     | 22.1 ms                                                | 20.4 ms: 1.08x faster                                  |
| genshi_xml      | 52.1 ms                                                | 46.2 ms: 1.13x faster                                  |
| mako            | 9.85 ms                                                | 9.94 ms: 1.01x slower                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221119-linux-x86_64-python-main-3.12.0a3+-b0e1f9c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 245 ms: 1.05x faster                                   |
| aiohttp                 | 1.05 ms                                                | 999 us: 1.05x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 729 ms: 1.03x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 665 ms: 1.06x slower                                   |
| chameleon               | 6.41 ms                                                | 6.49 ms: 1.01x slower                                  |
| chaos                   | 68.6 ms                                                | 66.0 ms: 1.04x faster                                  |
| coroutines              | 26.1 ms                                                | 24.8 ms: 1.05x faster                                  |
| coverage                | 101 ms                                                 | 98.2 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.3 ms: 1.01x slower                                  |
| deepcopy                | 344 us                                                 | 330 us: 1.04x faster                                   |
| deepcopy_memo           | 36.4 us                                                | 34.2 us: 1.06x faster                                  |
| deltablue               | 3.64 ms                                                | 3.23 ms: 1.13x faster                                  |
| django_template         | 32.5 ms                                                | 32.6 ms: 1.01x slower                                  |
| dulwich_log             | 63.9 ms                                                | 60.6 ms: 1.05x faster                                  |
| fannkuch                | 388 ms                                                 | 369 ms: 1.05x faster                                   |
| float                   | 76.3 ms                                                | 71.6 ms: 1.07x faster                                  |
| generators              | 72.2 ms                                                | 78.0 ms: 1.08x slower                                  |
| genshi_text             | 22.1 ms                                                | 20.4 ms: 1.08x faster                                  |
| genshi_xml              | 52.1 ms                                                | 46.2 ms: 1.13x faster                                  |
| go                      | 143 ms                                                 | 135 ms: 1.06x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.21 ms: 1.02x faster                                  |
| html5lib                | 63.2 ms                                                | 59.1 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.67 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.42 ms: 1.34x faster                                  |
| json_loads              | 26.2 us                                                | 24.2 us: 1.09x faster                                  |
| logging_format          | 6.62 us                                                | 6.35 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 91.1 ns: 1.08x faster                                  |
| logging_simple          | 6.06 us                                                | 5.77 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.94 ms: 1.01x slower                                  |
| mdp                     | 2.62 sec                                               | 2.65 sec: 1.01x slower                                 |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                   |
| mypy                    | 669 ms                                                 | 795 ms: 1.19x slower                                   |
| nbody                   | 95.0 ms                                                | 94.1 ms: 1.01x faster                                  |
| nqueens                 | 85.0 ms                                                | 81.5 ms: 1.04x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.5 ms: 1.04x faster                                  |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.0 us: 1.01x faster                                  |
| pickle_list             | 4.17 us                                                | 4.11 us: 1.02x faster                                  |
| pickle_pure_python      | 304 us                                                 | 283 us: 1.07x faster                                   |
| pidigits                | 199 ms                                                 | 192 ms: 1.04x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 673 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.12 sec: 1.05x faster                                 |
| pyflate                 | 417 ms                                                 | 403 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.51 ms: 1.02x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.25 ms: 1.05x slower                                  |
| raytrace                | 290 ms                                                 | 278 ms: 1.04x faster                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna               | 203 ms                                                 | 213 ms: 1.05x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.77 ms: 1.12x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.2 ms: 1.01x faster                                  |
| richards                | 46.2 ms                                                | 41.6 ms: 1.11x faster                                  |
| scimark_fft             | 329 ms                                                 | 303 ms: 1.09x faster                                   |
| scimark_lu              | 107 ms                                                 | 104 ms: 1.03x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.0 ms: 1.07x faster                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.10x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.96 ms: 1.11x faster                                  |
| spectral_norm           | 99.9 ms                                                | 97.6 ms: 1.02x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.33 ms: 1.03x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.61 ms: 1.03x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.7 ms: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.64 us: 1.06x slower                                  |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| sympy_sum               | 166 ms                                                 | 165 ms: 1.01x faster                                   |
| sympy_str               | 287 ms                                                 | 283 ms: 1.01x faster                                   |
| telco                   | 6.62 ms                                                | 6.27 ms: 1.06x faster                                  |
| thrift                  | 752 us                                                 | 746 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 92.7 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 42.9 ns: 1.01x faster                                  |
| unpickle_list           | 4.95 us                                                | 5.10 us: 1.03x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| xml_etree_process       | 53.8 ms                                                | 52.9 ms: 1.02x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (5): async_tree_none, deepcopy_reduce, unpickle, xml_etree_iterparse, xml_etree_generate
Ignored benchmarks (8) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
