Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| chameleon      | 6.41 ms                                                | 6.38 ms: 1.00x faster                                  |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                 |
| html5lib       | 63.2 ms                                                | 60.2 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.1 ms: 1.06x faster                                  |
| nbody          | 95.0 ms                                                | 96.5 ms: 1.02x slower                                  |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 130 ms: 1.05x faster                                   |
| regex_dna      | 203 ms                                                 | 206 ms: 1.01x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.40 ms: 1.01x slower                                  |
| regex_v8       | 22.3 ms                                                | 21.9 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.42 ms: 1.34x faster                                  |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.06x slower                                  |
| pickle_dict          | 31.4 us                                                | 32.4 us: 1.03x slower                                  |
| pickle_list          | 4.17 us                                                | 4.25 us: 1.02x slower                                  |
| pickle_pure_python   | 304 us                                                 | 282 us: 1.08x faster                                   |
| unpickle             | 13.3 us                                                | 13.0 us: 1.02x faster                                  |
| unpickle_list        | 4.95 us                                                | 4.91 us: 1.01x faster                                  |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.08x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.9 ms: 1.00x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.49 ms: 1.02x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.08 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 33.0 ms: 1.02x slower                                  |
| genshi_text     | 22.1 ms                                                | 20.9 ms: 1.06x faster                                  |
| genshi_xml      | 52.1 ms                                                | 49.0 ms: 1.06x faster                                  |
| mako            | 9.85 ms                                                | 9.59 ms: 1.03x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| async_generators        | 359 ms                                                 | 353 ms: 1.02x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 759 ms: 1.01x slower                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| chameleon               | 6.41 ms                                                | 6.38 ms: 1.00x faster                                  |
| chaos                   | 68.6 ms                                                | 69.6 ms: 1.01x slower                                  |
| bench_thread_pool       | 810 us                                                 | 781 us: 1.04x faster                                   |
| coroutines              | 26.1 ms                                                | 24.8 ms: 1.05x faster                                  |
| coverage                | 101 ms                                                 | 98.1 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 75.2 ms: 1.02x slower                                  |
| deepcopy                | 344 us                                                 | 330 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.95 us: 1.01x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 33.4 us: 1.09x faster                                  |
| deltablue               | 3.64 ms                                                | 3.27 ms: 1.12x faster                                  |
| django_template         | 32.5 ms                                                | 33.0 ms: 1.02x slower                                  |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.3 ms: 1.03x faster                                  |
| fannkuch                | 388 ms                                                 | 375 ms: 1.03x faster                                   |
| float                   | 76.3 ms                                                | 72.1 ms: 1.06x faster                                  |
| generators              | 72.2 ms                                                | 77.6 ms: 1.08x slower                                  |
| genshi_text             | 22.1 ms                                                | 20.9 ms: 1.06x faster                                  |
| genshi_xml              | 52.1 ms                                                | 49.0 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 138 ms: 1.04x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.09 ms: 1.04x faster                                  |
| html5lib                | 63.2 ms                                                | 60.2 ms: 1.05x faster                                  |
| json                    | 4.95 ms                                                | 4.74 ms: 1.04x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.42 ms: 1.34x faster                                  |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| logging_format          | 6.62 us                                                | 6.29 us: 1.05x faster                                  |
| logging_silent          | 98.5 ns                                                | 94.8 ns: 1.04x faster                                  |
| logging_simple          | 6.06 us                                                | 5.67 us: 1.07x faster                                  |
| mako                    | 9.85 ms                                                | 9.59 ms: 1.03x faster                                  |
| mdp                     | 2.62 sec                                               | 2.54 sec: 1.03x faster                                 |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                   |
| mypy                    | 669 ms                                                 | 810 ms: 1.21x slower                                   |
| nbody                   | 95.0 ms                                                | 96.5 ms: 1.02x slower                                  |
| nqueens                 | 85.0 ms                                                | 79.1 ms: 1.08x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.06x slower                                  |
| pickle_dict             | 31.4 us                                                | 32.4 us: 1.03x slower                                  |
| pickle_list             | 4.17 us                                                | 4.25 us: 1.02x slower                                  |
| pickle_pure_python      | 304 us                                                 | 282 us: 1.08x faster                                   |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 671 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.07x faster                                 |
| pyflate                 | 417 ms                                                 | 403 ms: 1.03x faster                                   |
| python_startup          | 8.36 ms                                                | 8.49 ms: 1.02x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.08 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 282 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 130 ms: 1.05x faster                                   |
| regex_dna               | 203 ms                                                 | 206 ms: 1.01x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.40 ms: 1.01x slower                                  |
| regex_v8                | 22.3 ms                                                | 21.9 ms: 1.02x faster                                  |
| richards                | 46.2 ms                                                | 41.8 ms: 1.11x faster                                  |
| scimark_fft             | 329 ms                                                 | 316 ms: 1.04x faster                                   |
| scimark_lu              | 107 ms                                                 | 109 ms: 1.01x slower                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.6 ms: 1.04x faster                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.10x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.25 ms: 1.03x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.4 ms: 1.05x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.40 ms: 1.02x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.70 ms: 1.02x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.9 ms: 1.04x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.56 us: 1.03x slower                                  |
| sympy_expand            | 472 ms                                                 | 456 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 162 ms: 1.02x faster                                   |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.25 ms: 1.06x faster                                  |
| unpickle                | 13.3 us                                                | 13.0 us: 1.02x faster                                  |
| unpickle_list           | 4.95 us                                                | 4.91 us: 1.01x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.08x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.9 ms: 1.00x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (6): async_tree_none, async_tree_memoization, bench_mp_pool, thrift, unpack_sequence, xml_etree_iterparse
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20221224-3.12.0a3+-b9aa14a/bm-20221224-linux-x86_64-python-main-3.12.0a3+-b9aa14a.json: djangocms
