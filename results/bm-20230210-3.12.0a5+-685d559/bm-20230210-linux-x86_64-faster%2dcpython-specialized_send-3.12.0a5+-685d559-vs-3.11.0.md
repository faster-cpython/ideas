
# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialized_send
- machine: linux-x86_64
- commit hash: 685d559
- commit date: 2023-02-10
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 246 ms: 1.05x faster                                                         |
| chameleon      | 6.41 ms                                                | 6.51 ms: 1.02x slower                                                        |
| docutils       | 2.60 sec                                               | 2.54 sec: 1.02x faster                                                       |
| html5lib       | 63.2 ms                                                | 61.3 ms: 1.03x faster                                                        |
| tornado_http   | 96.6 ms                                                | 95.1 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 73.9 ms: 1.03x faster                                                        |
| nbody          | 95.0 ms                                                | 93.0 ms: 1.02x faster                                                        |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 131 ms: 1.04x faster                                                         |
| regex_v8       | 22.3 ms                                                | 22.3 ms: 1.00x faster                                                        |
| regex_effbot   | 3.36 ms                                                | 3.38 ms: 1.01x slower                                                        |
| regex_dna      | 203 ms                                                 | 211 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.46 ms: 1.34x faster                                                        |
| unpickle_pure_python | 225 us                                                 | 199 us: 1.13x faster                                                         |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                                        |
| pickle_pure_python   | 304 us                                                 | 283 us: 1.07x faster                                                         |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.07x faster                                                         |
| pickle_dict          | 31.4 us                                                | 30.9 us: 1.02x faster                                                        |
| pickle_list          | 4.17 us                                                | 4.12 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                                         |
| pickle               | 9.79 us                                                | 10.1 us: 1.03x slower                                                        |
| unpickle             | 13.3 us                                                | 13.7 us: 1.03x slower                                                        |
| xml_etree_process    | 53.8 ms                                                | 55.9 ms: 1.04x slower                                                        |
| xml_etree_generate   | 76.2 ms                                                | 80.6 ms: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.96 ms: 1.07x slower                                                        |
| python_startup_no_site | 5.96 ms                                                | 6.49 ms: 1.09x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml     | 52.1 ms                                                | 48.1 ms: 1.08x faster                                                        |
| genshi_text    | 22.1 ms                                                | 20.8 ms: 1.06x faster                                                        |
| mako           | 9.85 ms                                                | 9.75 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 31.1 ms: 2.32x faster                                                        |
| json_dumps              | 12.7 ms                                                | 9.46 ms: 1.34x faster                                                        |
| coroutines              | 26.1 ms                                                | 22.3 ms: 1.17x faster                                                        |
| deltablue               | 3.64 ms                                                | 3.19 ms: 1.14x faster                                                        |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.87 ms: 1.14x faster                                                        |
| unpickle_pure_python    | 225 us                                                 | 199 us: 1.13x faster                                                         |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                                        |
| genshi_xml              | 52.1 ms                                                | 48.1 ms: 1.08x faster                                                        |
| richards                | 46.2 ms                                                | 42.9 ms: 1.07x faster                                                        |
| pickle_pure_python      | 304 us                                                 | 283 us: 1.07x faster                                                         |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.07x faster                                                         |
| json                    | 4.95 ms                                                | 4.61 ms: 1.07x faster                                                        |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                                         |
| logging_simple          | 6.06 us                                                | 5.67 us: 1.07x faster                                                        |
| sympy_str               | 287 ms                                                 | 270 ms: 1.06x faster                                                         |
| genshi_text             | 22.1 ms                                                | 20.8 ms: 1.06x faster                                                        |
| pycparser               | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                       |
| scimark_sor             | 115 ms                                                 | 109 ms: 1.06x faster                                                         |
| logging_format          | 6.62 us                                                | 6.26 us: 1.06x faster                                                        |
| deepcopy_memo           | 36.4 us                                                | 34.5 us: 1.06x faster                                                        |
| sympy_integrate         | 20.9 ms                                                | 19.8 ms: 1.05x faster                                                        |
| sympy_sum               | 166 ms                                                 | 158 ms: 1.05x faster                                                         |
| scimark_fft             | 329 ms                                                 | 313 ms: 1.05x faster                                                         |
| telco                   | 6.62 ms                                                | 6.32 ms: 1.05x faster                                                        |
| 2to3                    | 257 ms                                                 | 246 ms: 1.05x faster                                                         |
| logging_silent          | 98.5 ns                                                | 94.0 ns: 1.05x faster                                                        |
| sqlglot_optimize        | 53.0 ms                                                | 50.6 ms: 1.05x faster                                                        |
| nqueens                 | 85.0 ms                                                | 81.2 ms: 1.05x faster                                                        |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.05x faster                                                         |
| spectral_norm           | 99.9 ms                                                | 95.8 ms: 1.04x faster                                                        |
| regex_compile           | 136 ms                                                 | 131 ms: 1.04x faster                                                         |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                                        |
| chaos                   | 68.6 ms                                                | 66.1 ms: 1.04x faster                                                        |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                        |
| sympy_expand            | 472 ms                                                 | 456 ms: 1.04x faster                                                         |
| pyflate                 | 417 ms                                                 | 403 ms: 1.03x faster                                                         |
| hexiom                  | 6.35 ms                                                | 6.14 ms: 1.03x faster                                                        |
| deepcopy                | 344 us                                                 | 333 us: 1.03x faster                                                         |
| float                   | 76.3 ms                                                | 73.9 ms: 1.03x faster                                                        |
| scimark_monte_carlo     | 68.3 ms                                                | 66.1 ms: 1.03x faster                                                        |
| fannkuch                | 388 ms                                                 | 376 ms: 1.03x faster                                                         |
| html5lib                | 63.2 ms                                                | 61.3 ms: 1.03x faster                                                        |
| bench_thread_pool       | 810 us                                                 | 789 us: 1.03x faster                                                         |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.02x faster                                                       |
| coverage                | 101 ms                                                 | 98.1 ms: 1.02x faster                                                        |
| nbody                   | 95.0 ms                                                | 93.0 ms: 1.02x faster                                                        |
| docutils                | 2.60 sec                                               | 2.54 sec: 1.02x faster                                                       |
| raytrace                | 290 ms                                                 | 285 ms: 1.02x faster                                                         |
| tornado_http            | 96.6 ms                                                | 95.1 ms: 1.02x faster                                                        |
| deepcopy_reduce         | 2.97 us                                                | 2.92 us: 1.02x faster                                                        |
| pickle_dict             | 31.4 us                                                | 30.9 us: 1.02x faster                                                        |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.7 ms: 1.01x faster                                                        |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.01x faster                                                        |
| pickle_list             | 4.17 us                                                | 4.12 us: 1.01x faster                                                        |
| mako                    | 9.85 ms                                                | 9.75 ms: 1.01x faster                                                        |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                                         |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                                         |
| dulwich_log             | 63.9 ms                                                | 63.4 ms: 1.01x faster                                                        |
| scimark_lu              | 107 ms                                                 | 107 ms: 1.01x faster                                                         |
| crypto_pyaes            | 73.9 ms                                                | 73.7 ms: 1.00x faster                                                        |
| regex_v8                | 22.3 ms                                                | 22.3 ms: 1.00x faster                                                        |
| regex_effbot            | 3.36 ms                                                | 3.38 ms: 1.01x slower                                                        |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                                       |
| meteor_contest          | 105 ms                                                 | 106 ms: 1.01x slower                                                         |
| chameleon               | 6.41 ms                                                | 6.51 ms: 1.02x slower                                                        |
| thrift                  | 752 us                                                 | 766 us: 1.02x slower                                                         |
| pickle                  | 9.79 us                                                | 10.1 us: 1.03x slower                                                        |
| unpickle                | 13.3 us                                                | 13.7 us: 1.03x slower                                                        |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.03x slower                                                        |
| sqlglot_transpile       | 1.66 ms                                                | 1.72 ms: 1.04x slower                                                        |
| regex_dna               | 203 ms                                                 | 211 ms: 1.04x slower                                                         |
| xml_etree_process       | 53.8 ms                                                | 55.9 ms: 1.04x slower                                                        |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.04x slower                                                        |
| mdp                     | 2.62 sec                                               | 2.75 sec: 1.05x slower                                                       |
| xml_etree_generate      | 76.2 ms                                                | 80.6 ms: 1.06x slower                                                        |
| python_startup          | 8.36 ms                                                | 8.96 ms: 1.07x slower                                                        |
| python_startup_no_site  | 5.96 ms                                                | 6.49 ms: 1.09x slower                                                        |
| async_generators        | 359 ms                                                 | 410 ms: 1.14x slower                                                         |
| Geometric mean          | (ref)                                                  | 1.04x faster                                                                 |

Benchmark hidden because not significant (9): async_tree_none, sqlalchemy_declarative, async_tree_cpu_io_mixed, pprint_safe_repr, bench_mp_pool, unpack_sequence, django_template, unpickle_list, async_tree_memoization
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230210-3.12.0a5+-685d559/bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
