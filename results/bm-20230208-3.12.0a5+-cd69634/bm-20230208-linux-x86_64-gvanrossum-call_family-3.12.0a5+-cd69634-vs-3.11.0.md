
# Results vs. 3.11.0

- fork: gvanrossum
- ref: call_family
- machine: linux-x86_64
- commit hash: cd69634
- commit date: 2023-02-08
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 251 ms: 1.03x faster                                              |
| chameleon      | 6.41 ms                                                | 6.44 ms: 1.00x slower                                             |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                            |
| html5lib       | 63.2 ms                                                | 60.7 ms: 1.04x faster                                             |
| tornado_http   | 96.6 ms                                                | 94.3 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                  | 1.02x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                              |
| float          | 76.3 ms                                                | 74.0 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                | 21.0 ms: 1.06x faster                                             |
| regex_compile  | 136 ms                                                 | 129 ms: 1.05x faster                                              |
| regex_dna      | 203 ms                                                 | 206 ms: 1.01x slower                                              |
| regex_effbot   | 3.36 ms                                                | 3.64 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.44 ms: 1.34x faster                                             |
| unpickle_pure_python | 225 us                                                 | 199 us: 1.13x faster                                              |
| json_loads           | 26.2 us                                                | 23.8 us: 1.10x faster                                             |
| xml_etree_parse      | 158 ms                                                 | 146 ms: 1.08x faster                                              |
| pickle_pure_python   | 304 us                                                 | 286 us: 1.06x faster                                              |
| pickle_list          | 4.17 us                                                | 4.03 us: 1.04x faster                                             |
| pickle_dict          | 31.4 us                                                | 30.3 us: 1.04x faster                                             |
| unpickle             | 13.3 us                                                | 13.0 us: 1.02x faster                                             |
| xml_etree_process    | 53.8 ms                                                | 53.2 ms: 1.01x faster                                             |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                              |
| xml_etree_generate   | 76.2 ms                                                | 77.1 ms: 1.01x slower                                             |
| pickle               | 9.79 us                                                | 10.1 us: 1.04x slower                                             |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                      |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.91 ms: 1.07x slower                                             |
| python_startup_no_site | 5.96 ms                                                | 6.47 ms: 1.08x slower                                             |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.11x faster                                             |
| genshi_text     | 22.1 ms                                                | 20.5 ms: 1.08x faster                                             |
| mako            | 9.85 ms                                                | 9.97 ms: 1.01x slower                                             |
| django_template | 32.5 ms                                                | 33.2 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                      |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.44 ms: 1.34x faster                                             |
| deltablue               | 3.64 ms                                                | 3.17 ms: 1.15x faster                                             |
| unpickle_pure_python    | 225 us                                                 | 199 us: 1.13x faster                                              |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.11x faster                                             |
| json_loads              | 26.2 us                                                | 23.8 us: 1.10x faster                                             |
| scimark_sor             | 115 ms                                                 | 105 ms: 1.10x faster                                              |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.01 ms: 1.10x faster                                             |
| richards                | 46.2 ms                                                | 42.3 ms: 1.09x faster                                             |
| fannkuch                | 388 ms                                                 | 356 ms: 1.09x faster                                              |
| xml_etree_parse         | 158 ms                                                 | 146 ms: 1.08x faster                                              |
| scimark_fft             | 329 ms                                                 | 305 ms: 1.08x faster                                              |
| genshi_text             | 22.1 ms                                                | 20.5 ms: 1.08x faster                                             |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.08x faster                                            |
| nqueens                 | 85.0 ms                                                | 79.2 ms: 1.07x faster                                             |
| coroutines              | 26.1 ms                                                | 24.3 ms: 1.07x faster                                             |
| json                    | 4.95 ms                                                | 4.64 ms: 1.07x faster                                             |
| regex_v8                | 22.3 ms                                                | 21.0 ms: 1.06x faster                                             |
| sympy_str               | 287 ms                                                 | 270 ms: 1.06x faster                                              |
| pickle_pure_python      | 304 us                                                 | 286 us: 1.06x faster                                              |
| sympy_sum               | 166 ms                                                 | 156 ms: 1.06x faster                                              |
| mdp                     | 2.62 sec                                               | 2.48 sec: 1.06x faster                                            |
| hexiom                  | 6.35 ms                                                | 6.02 ms: 1.05x faster                                             |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                              |
| sympy_integrate         | 20.9 ms                                                | 19.8 ms: 1.05x faster                                             |
| regex_compile           | 136 ms                                                 | 129 ms: 1.05x faster                                              |
| deepcopy_memo           | 36.4 us                                                | 34.9 us: 1.04x faster                                             |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.04x faster                                             |
| telco                   | 6.62 ms                                                | 6.36 ms: 1.04x faster                                             |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                             |
| go                      | 143 ms                                                 | 138 ms: 1.04x faster                                              |
| sympy_expand            | 472 ms                                                 | 454 ms: 1.04x faster                                              |
| html5lib                | 63.2 ms                                                | 60.7 ms: 1.04x faster                                             |
| spectral_norm           | 99.9 ms                                                | 96.1 ms: 1.04x faster                                             |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                            |
| scimark_monte_carlo     | 68.3 ms                                                | 65.8 ms: 1.04x faster                                             |
| async_generators        | 359 ms                                                 | 346 ms: 1.04x faster                                              |
| pickle_list             | 4.17 us                                                | 4.03 us: 1.04x faster                                             |
| pickle_dict             | 31.4 us                                                | 30.3 us: 1.04x faster                                             |
| deepcopy                | 344 us                                                 | 332 us: 1.03x faster                                              |
| bench_thread_pool       | 810 us                                                 | 783 us: 1.03x faster                                              |
| logging_simple          | 6.06 us                                                | 5.88 us: 1.03x faster                                             |
| float                   | 76.3 ms                                                | 74.0 ms: 1.03x faster                                             |
| sqlglot_optimize        | 53.0 ms                                                | 51.4 ms: 1.03x faster                                             |
| chaos                   | 68.6 ms                                                | 66.7 ms: 1.03x faster                                             |
| 2to3                    | 257 ms                                                 | 251 ms: 1.03x faster                                              |
| logging_format          | 6.62 us                                                | 6.46 us: 1.03x faster                                             |
| tornado_http            | 96.6 ms                                                | 94.3 ms: 1.02x faster                                             |
| pyflate                 | 417 ms                                                 | 407 ms: 1.02x faster                                              |
| logging_silent          | 98.5 ns                                                | 96.3 ns: 1.02x faster                                             |
| sqlglot_normalize       | 108 ms                                                 | 106 ms: 1.02x faster                                              |
| unpickle                | 13.3 us                                                | 13.0 us: 1.02x faster                                             |
| coverage                | 101 ms                                                 | 98.8 ms: 1.02x faster                                             |
| crypto_pyaes            | 73.9 ms                                                | 72.7 ms: 1.02x faster                                             |
| thrift                  | 752 us                                                 | 740 us: 1.02x faster                                              |
| sqlalchemy_declarative  | 139 ms                                                 | 137 ms: 1.01x faster                                              |
| xml_etree_process       | 53.8 ms                                                | 53.2 ms: 1.01x faster                                             |
| async_tree_none         | 529 ms                                                 | 524 ms: 1.01x faster                                              |
| pathlib                 | 18.2 ms                                                | 18.0 ms: 1.01x faster                                             |
| pprint_pformat          | 1.44 sec                                               | 1.43 sec: 1.01x faster                                            |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                              |
| dulwich_log             | 63.9 ms                                                | 63.4 ms: 1.01x faster                                             |
| raytrace                | 290 ms                                                 | 288 ms: 1.01x faster                                              |
| chameleon               | 6.41 ms                                                | 6.44 ms: 1.00x slower                                             |
| pprint_safe_repr        | 691 ms                                                 | 697 ms: 1.01x slower                                              |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                            |
| xml_etree_generate      | 76.2 ms                                                | 77.1 ms: 1.01x slower                                             |
| mako                    | 9.85 ms                                                | 9.97 ms: 1.01x slower                                             |
| regex_dna               | 203 ms                                                 | 206 ms: 1.01x slower                                              |
| async_tree_memoization  | 625 ms                                                 | 637 ms: 1.02x slower                                              |
| meteor_contest          | 105 ms                                                 | 107 ms: 1.02x slower                                              |
| django_template         | 32.5 ms                                                | 33.2 ms: 1.02x slower                                             |
| pickle                  | 9.79 us                                                | 10.1 us: 1.04x slower                                             |
| sqlite_synth            | 2.49 us                                                | 2.60 us: 1.04x slower                                             |
| sqlglot_transpile       | 1.66 ms                                                | 1.74 ms: 1.05x slower                                             |
| sqlglot_parse           | 1.37 ms                                                | 1.44 ms: 1.05x slower                                             |
| python_startup          | 8.36 ms                                                | 8.91 ms: 1.07x slower                                             |
| regex_effbot            | 3.36 ms                                                | 3.64 ms: 1.08x slower                                             |
| python_startup_no_site  | 5.96 ms                                                | 6.47 ms: 1.08x slower                                             |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (9): nbody, deepcopy_reduce, bench_mp_pool, generators, async_tree_cpu_io_mixed, unpickle_list, sqlalchemy_imperative, scimark_lu, unpack_sequence
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230208-3.12.0a5+-cd69634/bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5+-cd69634.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
