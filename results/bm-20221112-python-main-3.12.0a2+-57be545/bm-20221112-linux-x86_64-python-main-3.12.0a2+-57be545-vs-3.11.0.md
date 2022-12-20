Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 246 ms: 1.05x faster                                   |
| chameleon      | 6.41 ms                                                | 6.49 ms: 1.01x slower                                  |
| html5lib       | 63.2 ms                                                | 58.9 ms: 1.07x faster                                  |
| tornado_http   | 96.6 ms                                                | 92.5 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 73.3 ms: 1.04x faster                                  |
| nbody          | 95.0 ms                                                | 93.4 ms: 1.02x faster                                  |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.07x faster                                   |
| regex_dna      | 203 ms                                                 | 205 ms: 1.01x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.64 ms: 1.08x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.2 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.44 ms: 1.34x faster                                  |
| json_loads           | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| pickle               | 9.79 us                                                | 10.0 us: 1.03x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.1 us: 1.01x faster                                  |
| pickle_list          | 4.17 us                                                | 4.14 us: 1.01x faster                                  |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                   |
| unpickle_list        | 4.95 us                                                | 4.91 us: 1.01x faster                                  |
| unpickle_pure_python | 225 us                                                 | 200 us: 1.13x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 149 ms: 1.06x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 103 ms: 1.01x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 76.8 ms: 1.01x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 53.0 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.52 ms: 1.02x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.24 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text    | 22.1 ms                                                | 21.3 ms: 1.04x faster                                  |
| genshi_xml     | 52.1 ms                                                | 46.8 ms: 1.11x faster                                  |
| mako           | 9.85 ms                                                | 9.70 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221112-linux-x86_64-python-main-3.12.0a2+-57be545 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 246 ms: 1.05x faster                                   |
| aiohttp                 | 1.05 ms                                                | 998 us: 1.05x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 731 ms: 1.03x faster                                   |
| async_tree_memoization  | 625 ms                                                 | 646 ms: 1.03x slower                                   |
| chameleon               | 6.41 ms                                                | 6.49 ms: 1.01x slower                                  |
| chaos                   | 68.6 ms                                                | 67.0 ms: 1.02x faster                                  |
| coroutines              | 26.1 ms                                                | 24.1 ms: 1.08x faster                                  |
| coverage                | 101 ms                                                 | 99.8 ms: 1.01x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 75.1 ms: 1.02x slower                                  |
| deepcopy                | 344 us                                                 | 332 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.90 us: 1.02x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.0 us: 1.07x faster                                  |
| deltablue               | 3.64 ms                                                | 3.22 ms: 1.13x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.1 ms: 1.05x faster                                  |
| fannkuch                | 388 ms                                                 | 374 ms: 1.04x faster                                   |
| float                   | 76.3 ms                                                | 73.3 ms: 1.04x faster                                  |
| generators              | 72.2 ms                                                | 79.6 ms: 1.10x slower                                  |
| genshi_text             | 22.1 ms                                                | 21.3 ms: 1.04x faster                                  |
| genshi_xml              | 52.1 ms                                                | 46.8 ms: 1.11x faster                                  |
| go                      | 143 ms                                                 | 135 ms: 1.06x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.13 ms: 1.04x faster                                  |
| html5lib                | 63.2 ms                                                | 58.9 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.71 ms: 1.05x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.44 ms: 1.34x faster                                  |
| json_loads              | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| logging_format          | 6.62 us                                                | 6.34 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 91.8 ns: 1.07x faster                                  |
| logging_simple          | 6.06 us                                                | 5.77 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.70 ms: 1.02x faster                                  |
| mdp                     | 2.62 sec                                               | 2.47 sec: 1.06x faster                                 |
| mypy                    | 669 ms                                                 | 798 ms: 1.19x slower                                   |
| nbody                   | 95.0 ms                                                | 93.4 ms: 1.02x faster                                  |
| nqueens                 | 85.0 ms                                                | 81.1 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.5 ms: 1.04x faster                                  |
| pickle                  | 9.79 us                                                | 10.0 us: 1.03x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.1 us: 1.01x faster                                  |
| pickle_list             | 4.17 us                                                | 4.14 us: 1.01x faster                                  |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                   |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 688 ms: 1.00x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.02x faster                                 |
| pycparser               | 1.17 sec                                               | 1.11 sec: 1.05x faster                                 |
| pyflate                 | 417 ms                                                 | 402 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.52 ms: 1.02x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.24 ms: 1.05x slower                                  |
| raytrace                | 290 ms                                                 | 281 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 128 ms: 1.07x faster                                   |
| regex_dna               | 203 ms                                                 | 205 ms: 1.01x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.64 ms: 1.08x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.2 ms: 1.00x faster                                  |
| richards                | 46.2 ms                                                | 41.7 ms: 1.11x faster                                  |
| scimark_fft             | 329 ms                                                 | 309 ms: 1.06x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.5 ms: 1.04x faster                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.11x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.16 ms: 1.06x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.2 ms: 1.05x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.35 ms: 1.02x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.64 ms: 1.02x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.5 ms: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.65 us: 1.06x slower                                  |
| sympy_expand            | 472 ms                                                 | 458 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 164 ms: 1.01x faster                                   |
| sympy_str               | 287 ms                                                 | 283 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.32 ms: 1.05x faster                                  |
| thrift                  | 752 us                                                 | 745 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 92.5 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 44.2 ns: 1.02x slower                                  |
| unpickle_list           | 4.95 us                                                | 4.91 us: 1.01x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 200 us: 1.13x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 149 ms: 1.06x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 103 ms: 1.01x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 76.8 ms: 1.01x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 53.0 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (6): async_tree_none, async_tree_io, django_template, meteor_contest, scimark_lu, unpickle
Ignored benchmarks (8) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
