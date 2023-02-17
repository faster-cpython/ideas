
# Results vs. 3.11.0

- fork: faster-cpython
- ref: restrict_for_iter_sp
- machine: linux-x86_64
- commit hash: fb5f321
- commit date: 2023-02-17
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 247 ms: 1.04x faster                                                             |
| docutils       | 2.60 sec                                               | 2.53 sec: 1.03x faster                                                           |
| html5lib       | 63.2 ms                                                | 61.2 ms: 1.03x faster                                                            |
| tornado_http   | 96.6 ms                                                | 94.8 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 73.7 ms: 1.04x faster                                                            |
| pidigits       | 199 ms                                                 | 198 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 132 ms: 1.03x faster                                                             |
| regex_dna      | 203 ms                                                 | 199 ms: 1.02x faster                                                             |
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                            |
| regex_effbot   | 3.36 ms                                                | 3.65 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.50 ms: 1.33x faster                                                            |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.15x faster                                                             |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                                            |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                                             |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| pickle_list          | 4.17 us                                                | 4.01 us: 1.04x faster                                                            |
| pickle_dict          | 31.4 us                                                | 30.2 us: 1.04x faster                                                            |
| xml_etree_iterparse  | 103 ms                                                 | 99.7 ms: 1.03x faster                                                            |
| unpickle_list        | 4.95 us                                                | 5.04 us: 1.02x slower                                                            |
| pickle               | 9.79 us                                                | 9.98 us: 1.02x slower                                                            |
| xml_etree_process    | 53.8 ms                                                | 55.7 ms: 1.04x slower                                                            |
| xml_etree_generate   | 76.2 ms                                                | 81.2 ms: 1.07x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.92 ms: 1.07x slower                                                            |
| python_startup_no_site | 5.96 ms                                                | 6.47 ms: 1.08x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 48.4 ms: 1.08x faster                                                            |
| genshi_text     | 22.1 ms                                                | 21.2 ms: 1.04x faster                                                            |
| mako            | 9.85 ms                                                | 9.89 ms: 1.00x slower                                                            |
| django_template | 32.5 ms                                                | 33.0 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 30.6 ms: 2.36x faster                                                            |
| json_dumps              | 12.7 ms                                                | 9.50 ms: 1.33x faster                                                            |
| coroutines              | 26.1 ms                                                | 22.1 ms: 1.18x faster                                                            |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.15x faster                                                             |
| deltablue               | 3.64 ms                                                | 3.19 ms: 1.14x faster                                                            |
| richards                | 46.2 ms                                                | 42.2 ms: 1.09x faster                                                            |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                                            |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                                             |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| genshi_xml              | 52.1 ms                                                | 48.4 ms: 1.08x faster                                                            |
| json                    | 4.95 ms                                                | 4.60 ms: 1.07x faster                                                            |
| fannkuch                | 388 ms                                                 | 362 ms: 1.07x faster                                                             |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                           |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                                             |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| spectral_norm           | 99.9 ms                                                | 94.1 ms: 1.06x faster                                                            |
| logging_simple          | 6.06 us                                                | 5.74 us: 1.06x faster                                                            |
| sympy_str               | 287 ms                                                 | 273 ms: 1.05x faster                                                             |
| deepcopy_memo           | 36.4 us                                                | 34.6 us: 1.05x faster                                                            |
| scimark_fft             | 329 ms                                                 | 314 ms: 1.05x faster                                                             |
| genshi_text             | 22.1 ms                                                | 21.2 ms: 1.04x faster                                                            |
| sympy_integrate         | 20.9 ms                                                | 20.0 ms: 1.04x faster                                                            |
| pickle_list             | 4.17 us                                                | 4.01 us: 1.04x faster                                                            |
| nqueens                 | 85.0 ms                                                | 81.7 ms: 1.04x faster                                                            |
| 2to3                    | 257 ms                                                 | 247 ms: 1.04x faster                                                             |
| pickle_dict             | 31.4 us                                                | 30.2 us: 1.04x faster                                                            |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                                             |
| logging_format          | 6.62 us                                                | 6.37 us: 1.04x faster                                                            |
| pyflate                 | 417 ms                                                 | 402 ms: 1.04x faster                                                             |
| sqlglot_optimize        | 53.0 ms                                                | 51.1 ms: 1.04x faster                                                            |
| sympy_expand            | 472 ms                                                 | 455 ms: 1.04x faster                                                             |
| unpack_sequence         | 43.4 ns                                                | 41.9 ns: 1.04x faster                                                            |
| float                   | 76.3 ms                                                | 73.7 ms: 1.04x faster                                                            |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.03x faster                                                            |
| html5lib                | 63.2 ms                                                | 61.2 ms: 1.03x faster                                                            |
| deepcopy                | 344 us                                                 | 333 us: 1.03x faster                                                             |
| xml_etree_iterparse     | 103 ms                                                 | 99.7 ms: 1.03x faster                                                            |
| logging_silent          | 98.5 ns                                                | 95.7 ns: 1.03x faster                                                            |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                                             |
| regex_compile           | 136 ms                                                 | 132 ms: 1.03x faster                                                             |
| docutils                | 2.60 sec                                               | 2.53 sec: 1.03x faster                                                           |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.03x faster                                                           |
| coverage                | 101 ms                                                 | 97.9 ms: 1.03x faster                                                            |
| gunicorn                | 1.12 ms                                                | 1.10 ms: 1.02x faster                                                            |
| bench_thread_pool       | 810 us                                                 | 791 us: 1.02x faster                                                             |
| regex_dna               | 203 ms                                                 | 199 ms: 1.02x faster                                                             |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                            |
| tornado_http            | 96.6 ms                                                | 94.8 ms: 1.02x faster                                                            |
| dulwich_log             | 63.9 ms                                                | 62.8 ms: 1.02x faster                                                            |
| scimark_monte_carlo     | 68.3 ms                                                | 67.1 ms: 1.02x faster                                                            |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                                             |
| pprint_safe_repr        | 691 ms                                                 | 680 ms: 1.02x faster                                                             |
| sqlalchemy_declarative  | 139 ms                                                 | 137 ms: 1.01x faster                                                             |
| hexiom                  | 6.35 ms                                                | 6.27 ms: 1.01x faster                                                            |
| pidigits                | 199 ms                                                 | 198 ms: 1.01x faster                                                             |
| chaos                   | 68.6 ms                                                | 68.0 ms: 1.01x faster                                                            |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                                            |
| crypto_pyaes            | 73.9 ms                                                | 74.2 ms: 1.00x slower                                                            |
| mako                    | 9.85 ms                                                | 9.89 ms: 1.00x slower                                                            |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                                           |
| mdp                     | 2.62 sec                                               | 2.66 sec: 1.01x slower                                                           |
| unpickle_list           | 4.95 us                                                | 5.04 us: 1.02x slower                                                            |
| django_template         | 32.5 ms                                                | 33.0 ms: 1.02x slower                                                            |
| pickle                  | 9.79 us                                                | 9.98 us: 1.02x slower                                                            |
| thrift                  | 752 us                                                 | 769 us: 1.02x slower                                                             |
| scimark_lu              | 107 ms                                                 | 110 ms: 1.02x slower                                                             |
| xml_etree_process       | 53.8 ms                                                | 55.7 ms: 1.04x slower                                                            |
| sqlglot_transpile       | 1.66 ms                                                | 1.73 ms: 1.04x slower                                                            |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.60 ms: 1.05x slower                                                            |
| sqlglot_parse           | 1.37 ms                                                | 1.44 ms: 1.05x slower                                                            |
| xml_etree_generate      | 76.2 ms                                                | 81.2 ms: 1.07x slower                                                            |
| sqlite_synth            | 2.49 us                                                | 2.66 us: 1.07x slower                                                            |
| python_startup          | 8.36 ms                                                | 8.92 ms: 1.07x slower                                                            |
| async_tree_memoization  | 625 ms                                                 | 677 ms: 1.08x slower                                                             |
| python_startup_no_site  | 5.96 ms                                                | 6.47 ms: 1.08x slower                                                            |
| regex_effbot            | 3.36 ms                                                | 3.65 ms: 1.09x slower                                                            |
| async_generators        | 359 ms                                                 | 410 ms: 1.14x slower                                                             |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (10): telco, chameleon, pathlib, sqlalchemy_imperative, bench_mp_pool, async_tree_none, raytrace, async_tree_cpu_io_mixed, nbody, unpickle
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230217-3.12.0a5+-fb5f321/bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
