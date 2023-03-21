
# Results vs. 3.11.0

- fork: iritkatriel
- ref: remove_JUMP_IF_FALSE
- machine: linux-x86_64
- commit hash: 12595f6
- commit date: 2023-03-21
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.04x faster                                                        |
| chameleon      | 6.41 ms                                                | 6.56 ms: 1.02x slower                                                       |
| docutils       | 2.60 sec                                               | 2.54 sec: 1.02x faster                                                      |
| html5lib       | 63.2 ms                                                | 60.8 ms: 1.04x faster                                                       |
| tornado_http   | 96.6 ms                                                | 91.5 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 95.0 ms                                                | 87.2 ms: 1.09x faster                                                       |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                                        |
| float          | 76.3 ms                                                | 73.2 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 134 ms: 1.02x faster                                                        |
| regex_v8       | 22.3 ms                                                | 22.0 ms: 1.02x faster                                                       |
| regex_dna      | 203 ms                                                 | 201 ms: 1.01x faster                                                        |
| regex_effbot   | 3.36 ms                                                | 3.59 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.51 ms: 1.33x faster                                                       |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                                        |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                                       |
| pickle_pure_python   | 304 us                                                 | 287 us: 1.06x faster                                                        |
| xml_etree_parse      | 158 ms                                                 | 150 ms: 1.05x faster                                                        |
| pickle_list          | 4.17 us                                                | 4.08 us: 1.02x faster                                                       |
| pickle_dict          | 31.4 us                                                | 30.8 us: 1.02x faster                                                       |
| unpickle_list        | 4.95 us                                                | 5.01 us: 1.01x slower                                                       |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                                       |
| unpickle             | 13.3 us                                                | 14.0 us: 1.05x slower                                                       |
| xml_etree_process    | 53.8 ms                                                | 56.8 ms: 1.06x slower                                                       |
| xml_etree_generate   | 76.2 ms                                                | 81.6 ms: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.87 ms: 1.06x slower                                                       |
| python_startup_no_site | 5.96 ms                                                | 6.50 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 46.8 ms: 1.11x faster                                                       |
| genshi_text     | 22.1 ms                                                | 21.8 ms: 1.02x faster                                                       |
| mako            | 9.85 ms                                                | 10.0 ms: 1.02x slower                                                       |
| django_template | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.2 ms: 2.47x faster                                                       |
| json_dumps              | 12.7 ms                                                | 9.51 ms: 1.33x faster                                                       |
| coroutines              | 26.1 ms                                                | 22.0 ms: 1.19x faster                                                       |
| deltablue               | 3.64 ms                                                | 3.18 ms: 1.14x faster                                                       |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                                        |
| spectral_norm           | 99.9 ms                                                | 88.6 ms: 1.13x faster                                                       |
| genshi_xml              | 52.1 ms                                                | 46.8 ms: 1.11x faster                                                       |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.10x faster                                                        |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                                       |
| nbody                   | 95.0 ms                                                | 87.2 ms: 1.09x faster                                                       |
| mdp                     | 2.62 sec                                               | 2.43 sec: 1.08x faster                                                      |
| json                    | 4.95 ms                                                | 4.61 ms: 1.07x faster                                                       |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                                        |
| scimark_fft             | 329 ms                                                 | 309 ms: 1.07x faster                                                        |
| richards                | 46.2 ms                                                | 43.5 ms: 1.06x faster                                                       |
| pickle_pure_python      | 304 us                                                 | 287 us: 1.06x faster                                                        |
| coverage                | 101 ms                                                 | 94.9 ms: 1.06x faster                                                       |
| tornado_http            | 96.6 ms                                                | 91.5 ms: 1.06x faster                                                       |
| xml_etree_parse         | 158 ms                                                 | 150 ms: 1.05x faster                                                        |
| deepcopy_memo           | 36.4 us                                                | 34.6 us: 1.05x faster                                                       |
| nqueens                 | 85.0 ms                                                | 80.8 ms: 1.05x faster                                                       |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                                        |
| logging_simple          | 6.06 us                                                | 5.78 us: 1.05x faster                                                       |
| logging_format          | 6.62 us                                                | 6.32 us: 1.05x faster                                                       |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                                        |
| float                   | 76.3 ms                                                | 73.2 ms: 1.04x faster                                                       |
| pycparser               | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                      |
| deepcopy                | 344 us                                                 | 330 us: 1.04x faster                                                        |
| html5lib                | 63.2 ms                                                | 60.8 ms: 1.04x faster                                                       |
| hexiom                  | 6.35 ms                                                | 6.11 ms: 1.04x faster                                                       |
| 2to3                    | 257 ms                                                 | 249 ms: 1.04x faster                                                        |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.03x faster                                                       |
| scimark_monte_carlo     | 68.3 ms                                                | 66.2 ms: 1.03x faster                                                       |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                                       |
| chaos                   | 68.6 ms                                                | 66.6 ms: 1.03x faster                                                       |
| sqlglot_optimize        | 53.0 ms                                                | 51.5 ms: 1.03x faster                                                       |
| sympy_expand            | 472 ms                                                 | 459 ms: 1.03x faster                                                        |
| bench_thread_pool       | 810 us                                                 | 788 us: 1.03x faster                                                        |
| raytrace                | 290 ms                                                 | 283 ms: 1.03x faster                                                        |
| pyflate                 | 417 ms                                                 | 407 ms: 1.02x faster                                                        |
| pickle_list             | 4.17 us                                                | 4.08 us: 1.02x faster                                                       |
| docutils                | 2.60 sec                                               | 2.54 sec: 1.02x faster                                                      |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                       |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                                       |
| pickle_dict             | 31.4 us                                                | 30.8 us: 1.02x faster                                                       |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.32 ms: 1.02x faster                                                       |
| sqlglot_normalize       | 108 ms                                                 | 106 ms: 1.02x faster                                                        |
| sqlalchemy_declarative  | 139 ms                                                 | 136 ms: 1.02x faster                                                        |
| regex_compile           | 136 ms                                                 | 134 ms: 1.02x faster                                                        |
| telco                   | 6.62 ms                                                | 6.51 ms: 1.02x faster                                                       |
| sympy_str               | 287 ms                                                 | 283 ms: 1.02x faster                                                        |
| genshi_text             | 22.1 ms                                                | 21.8 ms: 1.02x faster                                                       |
| regex_v8                | 22.3 ms                                                | 22.0 ms: 1.02x faster                                                       |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                                        |
| dulwich_log             | 63.9 ms                                                | 63.3 ms: 1.01x faster                                                       |
| regex_dna               | 203 ms                                                 | 201 ms: 1.01x faster                                                        |
| crypto_pyaes            | 73.9 ms                                                | 73.4 ms: 1.01x faster                                                       |
| pprint_pformat          | 1.44 sec                                               | 1.45 sec: 1.00x slower                                                      |
| scimark_lu              | 107 ms                                                 | 109 ms: 1.01x slower                                                        |
| unpickle_list           | 4.95 us                                                | 5.01 us: 1.01x slower                                                       |
| unpack_sequence         | 43.4 ns                                                | 44.2 ns: 1.02x slower                                                       |
| mako                    | 9.85 ms                                                | 10.0 ms: 1.02x slower                                                       |
| chameleon               | 6.41 ms                                                | 6.56 ms: 1.02x slower                                                       |
| django_template         | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                       |
| thrift                  | 752 us                                                 | 773 us: 1.03x slower                                                        |
| pprint_safe_repr        | 691 ms                                                 | 711 ms: 1.03x slower                                                        |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                                       |
| sqlite_synth            | 2.49 us                                                | 2.61 us: 1.05x slower                                                       |
| sqlglot_transpile       | 1.66 ms                                                | 1.74 ms: 1.05x slower                                                       |
| unpickle                | 13.3 us                                                | 14.0 us: 1.05x slower                                                       |
| xml_etree_process       | 53.8 ms                                                | 56.8 ms: 1.06x slower                                                       |
| sqlglot_parse           | 1.37 ms                                                | 1.45 ms: 1.06x slower                                                       |
| python_startup          | 8.36 ms                                                | 8.87 ms: 1.06x slower                                                       |
| async_tree_memoization  | 625 ms                                                 | 666 ms: 1.07x slower                                                        |
| regex_effbot            | 3.36 ms                                                | 3.59 ms: 1.07x slower                                                       |
| xml_etree_generate      | 76.2 ms                                                | 81.6 ms: 1.07x slower                                                       |
| python_startup_no_site  | 5.96 ms                                                | 6.50 ms: 1.09x slower                                                       |
| async_generators        | 359 ms                                                 | 411 ms: 1.14x slower                                                        |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                                |

Benchmark hidden because not significant (9): async_tree_cpu_io_mixed, sqlalchemy_imperative, async_tree_io, async_tree_none, logging_silent, bench_mp_pool, sympy_sum, xml_etree_iterparse, deepcopy_reduce
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230321-3.12.0a6+-12595f6/bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
