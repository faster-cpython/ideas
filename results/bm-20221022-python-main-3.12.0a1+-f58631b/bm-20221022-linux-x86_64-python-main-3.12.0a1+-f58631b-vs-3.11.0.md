Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| chameleon      | 6.41 ms                                                | 6.60 ms: 1.03x slower                                  |
| html5lib       | 63.2 ms                                                | 59.1 ms: 1.07x faster                                  |
| tornado_http   | 96.6 ms                                                | 93.1 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.5 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 93.9 ms: 1.01x faster                                  |
| pidigits       | 199 ms                                                 | 199 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 130 ms: 1.04x faster                                   |
| regex_dna      | 203 ms                                                 | 209 ms: 1.03x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.66 ms: 1.09x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.7 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.49 ms: 1.33x faster                                  |
| json_loads           | 26.2 us                                                | 23.5 us: 1.12x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.06x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.0 us: 1.01x faster                                  |
| pickle_list          | 4.17 us                                                | 3.96 us: 1.05x faster                                  |
| pickle_pure_python   | 304 us                                                 | 289 us: 1.05x faster                                   |
| unpickle_list        | 4.95 us                                                | 4.98 us: 1.01x slower                                  |
| unpickle_pure_python | 225 us                                                 | 203 us: 1.11x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.08x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 75.5 ms: 1.01x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 53.1 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.37 ms: 1.00x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.06 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text    | 22.1 ms                                                | 21.0 ms: 1.05x faster                                  |
| genshi_xml     | 52.1 ms                                                | 49.7 ms: 1.05x faster                                  |
| mako           | 9.85 ms                                                | 9.75 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221022-linux-x86_64-python-main-3.12.0a1+-f58631b |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                  |
| async_tree_cpu_io_mixed | 752 ms                                                 | 732 ms: 1.03x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.33 sec: 1.01x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 670 ms: 1.07x slower                                   |
| chameleon               | 6.41 ms                                                | 6.60 ms: 1.03x slower                                  |
| chaos                   | 68.6 ms                                                | 69.7 ms: 1.02x slower                                  |
| coroutines              | 26.1 ms                                                | 24.4 ms: 1.07x faster                                  |
| coverage                | 101 ms                                                 | 97.8 ms: 1.03x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 76.4 ms: 1.03x slower                                  |
| deepcopy                | 344 us                                                 | 331 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.89 us: 1.03x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.1 us: 1.07x faster                                  |
| deltablue               | 3.64 ms                                                | 3.30 ms: 1.10x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.3 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                   |
| float                   | 76.3 ms                                                | 72.5 ms: 1.05x faster                                  |
| generators              | 72.2 ms                                                | 70.6 ms: 1.02x faster                                  |
| genshi_text             | 22.1 ms                                                | 21.0 ms: 1.05x faster                                  |
| genshi_xml              | 52.1 ms                                                | 49.7 ms: 1.05x faster                                  |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.07 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 59.1 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.58 ms: 1.08x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.49 ms: 1.33x faster                                  |
| json_loads              | 26.2 us                                                | 23.5 us: 1.12x faster                                  |
| logging_format          | 6.62 us                                                | 6.47 us: 1.02x faster                                  |
| logging_silent          | 98.5 ns                                                | 90.5 ns: 1.09x faster                                  |
| logging_simple          | 6.06 us                                                | 5.84 us: 1.04x faster                                  |
| mako                    | 9.85 ms                                                | 9.75 ms: 1.01x faster                                  |
| mdp                     | 2.62 sec                                               | 2.48 sec: 1.06x faster                                 |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                   |
| mypy                    | 669 ms                                                 | 799 ms: 1.19x slower                                   |
| nbody                   | 95.0 ms                                                | 93.9 ms: 1.01x faster                                  |
| nqueens                 | 85.0 ms                                                | 80.3 ms: 1.06x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.06x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.0 us: 1.01x faster                                  |
| pickle_list             | 4.17 us                                                | 3.96 us: 1.05x faster                                  |
| pickle_pure_python      | 304 us                                                 | 289 us: 1.05x faster                                   |
| pidigits                | 199 ms                                                 | 199 ms: 1.00x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 678 ms: 1.02x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.04x faster                                 |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.08x faster                                 |
| pyflate                 | 417 ms                                                 | 400 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.37 ms: 1.00x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.06 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 287 ms: 1.01x faster                                   |
| regex_compile           | 136 ms                                                 | 130 ms: 1.04x faster                                   |
| regex_dna               | 203 ms                                                 | 209 ms: 1.03x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.66 ms: 1.09x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.7 ms: 1.02x slower                                  |
| richards                | 46.2 ms                                                | 43.5 ms: 1.06x faster                                  |
| scimark_fft             | 329 ms                                                 | 317 ms: 1.04x faster                                   |
| scimark_lu              | 107 ms                                                 | 109 ms: 1.01x slower                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 66.6 ms: 1.02x faster                                  |
| scimark_sor             | 115 ms                                                 | 105 ms: 1.10x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.22 ms: 1.04x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.1 ms: 1.05x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.33 ms: 1.03x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.63 ms: 1.02x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.6 ms: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.02x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.61 us: 1.05x slower                                  |
| sympy_expand            | 472 ms                                                 | 454 ms: 1.04x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 164 ms: 1.01x faster                                   |
| sympy_str               | 287 ms                                                 | 282 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.54 ms: 1.01x faster                                  |
| thrift                  | 752 us                                                 | 739 us: 1.02x faster                                   |
| tornado_http            | 96.6 ms                                                | 93.1 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 48.7 ns: 1.12x slower                                  |
| unpickle_list           | 4.95 us                                                | 4.98 us: 1.01x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 203 us: 1.11x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.08x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 75.5 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 53.1 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (4): async_tree_none, django_template, pylint, unpickle
Ignored benchmarks (7) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
