Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.04x faster                                   |
| chameleon      | 6.41 ms                                                | 6.71 ms: 1.05x slower                                  |
| html5lib       | 63.2 ms                                                | 59.2 ms: 1.07x faster                                  |
| tornado_http   | 96.6 ms                                                | 92.6 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.2 ms: 1.06x faster                                  |
| nbody          | 95.0 ms                                                | 94.2 ms: 1.01x faster                                  |
| pidigits       | 199 ms                                                 | 199 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 129 ms: 1.05x faster                                   |
| regex_dna      | 203 ms                                                 | 200 ms: 1.01x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.60 ms: 1.07x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.2 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.60 ms: 1.32x faster                                  |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.1 us: 1.01x faster                                  |
| pickle_list          | 4.17 us                                                | 4.14 us: 1.01x faster                                  |
| pickle_pure_python   | 304 us                                                 | 293 us: 1.04x faster                                   |
| unpickle             | 13.3 us                                                | 12.9 us: 1.03x faster                                  |
| unpickle_pure_python | 225 us                                                 | 202 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 145 ms: 1.09x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 76.9 ms: 1.01x slower                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (3): unpickle_list, xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.41 ms: 1.01x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.09 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.6 ms: 1.01x slower                                  |
| genshi_text     | 22.1 ms                                                | 21.0 ms: 1.05x faster                                  |
| genshi_xml      | 52.1 ms                                                | 49.2 ms: 1.06x faster                                  |
| mako            | 9.85 ms                                                | 9.82 ms: 1.00x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221015-linux-x86_64-python-main-3.12.0a1+-660f102 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 249 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                | 997 us: 1.05x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 730 ms: 1.03x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 647 ms: 1.04x slower                                   |
| chameleon               | 6.41 ms                                                | 6.71 ms: 1.05x slower                                  |
| chaos                   | 68.6 ms                                                | 66.1 ms: 1.04x faster                                  |
| coroutines              | 26.1 ms                                                | 24.6 ms: 1.06x faster                                  |
| coverage                | 101 ms                                                 | 98.4 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 75.2 ms: 1.02x slower                                  |
| deepcopy                | 344 us                                                 | 332 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.91 us: 1.02x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.6 us: 1.05x faster                                  |
| deltablue               | 3.64 ms                                                | 3.31 ms: 1.10x faster                                  |
| django_template         | 32.5 ms                                                | 32.6 ms: 1.01x slower                                  |
| dulwich_log             | 63.9 ms                                                | 60.9 ms: 1.05x faster                                  |
| fannkuch                | 388 ms                                                 | 368 ms: 1.05x faster                                   |
| float                   | 76.3 ms                                                | 72.2 ms: 1.06x faster                                  |
| generators              | 72.2 ms                                                | 71.8 ms: 1.00x faster                                  |
| genshi_text             | 22.1 ms                                                | 21.0 ms: 1.05x faster                                  |
| genshi_xml              | 52.1 ms                                                | 49.2 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.05 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 59.2 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.78 ms: 1.04x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.60 ms: 1.32x faster                                  |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| logging_format          | 6.62 us                                                | 6.38 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 92.9 ns: 1.06x faster                                  |
| logging_simple          | 6.06 us                                                | 5.73 us: 1.06x faster                                  |
| mako                    | 9.85 ms                                                | 9.82 ms: 1.00x faster                                  |
| mdp                     | 2.62 sec                                               | 2.54 sec: 1.03x faster                                 |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                   |
| mypy                    | 669 ms                                                 | 801 ms: 1.20x slower                                   |
| nbody                   | 95.0 ms                                                | 94.2 ms: 1.01x faster                                  |
| nqueens                 | 85.0 ms                                                | 79.5 ms: 1.07x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.1 us: 1.01x faster                                  |
| pickle_list             | 4.17 us                                                | 4.14 us: 1.01x faster                                  |
| pickle_pure_python      | 304 us                                                 | 293 us: 1.04x faster                                   |
| pidigits                | 199 ms                                                 | 199 ms: 1.00x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 669 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.07x faster                                 |
| pyflate                 | 417 ms                                                 | 402 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.41 ms: 1.01x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.09 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 285 ms: 1.02x faster                                   |
| regex_compile           | 136 ms                                                 | 129 ms: 1.05x faster                                   |
| regex_dna               | 203 ms                                                 | 200 ms: 1.01x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.60 ms: 1.07x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.2 ms: 1.00x faster                                  |
| richards                | 46.2 ms                                                | 43.0 ms: 1.07x faster                                  |
| scimark_fft             | 329 ms                                                 | 315 ms: 1.04x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.6 ms: 1.04x faster                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.11x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.16 ms: 1.06x faster                                  |
| spectral_norm           | 99.9 ms                                                | 96.7 ms: 1.03x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.34 ms: 1.02x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.63 ms: 1.02x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.5 ms: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.62 us: 1.05x slower                                  |
| sympy_expand            | 472 ms                                                 | 458 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| sympy_sum               | 166 ms                                                 | 163 ms: 1.02x faster                                   |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.46 ms: 1.02x faster                                  |
| thrift                  | 752 us                                                 | 742 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 92.6 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 44.1 ns: 1.02x slower                                  |
| unpickle                | 13.3 us                                                | 12.9 us: 1.03x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 202 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 145 ms: 1.09x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 76.9 ms: 1.01x slower                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (6): async_tree_none, pylint, scimark_lu, unpickle_list, xml_etree_iterparse, xml_etree_process
Ignored benchmarks (7) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
