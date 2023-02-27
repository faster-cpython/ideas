
# Results vs. 3.11.0

- fork: faster-cpython
- ref: check_refcnt_in_bina
- machine: linux-x86_64
- commit hash: c29d369
- commit date: 2023-02-27
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                                             |
| chameleon      | 6.41 ms                                                | 6.51 ms: 1.02x slower                                                            |
| docutils       | 2.60 sec                                               | 2.53 sec: 1.02x faster                                                           |
| html5lib       | 63.2 ms                                                | 61.4 ms: 1.03x faster                                                            |
| tornado_http   | 96.6 ms                                                | 94.3 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 95.0 ms                                                | 89.7 ms: 1.06x faster                                                            |
| float          | 76.3 ms                                                | 72.2 ms: 1.06x faster                                                            |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 132 ms: 1.03x faster                                                             |
| regex_v8       | 22.3 ms                                                | 22.2 ms: 1.00x faster                                                            |
| regex_dna      | 203 ms                                                 | 209 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.62 ms: 1.32x faster                                                            |
| unpickle_pure_python | 225 us                                                 | 196 us: 1.15x faster                                                             |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                                            |
| pickle_pure_python   | 304 us                                                 | 284 us: 1.07x faster                                                             |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| xml_etree_iterparse  | 103 ms                                                 | 98.7 ms: 1.04x faster                                                            |
| pickle_dict          | 31.4 us                                                | 30.7 us: 1.02x faster                                                            |
| pickle_list          | 4.17 us                                                | 4.12 us: 1.01x faster                                                            |
| xml_etree_process    | 53.8 ms                                                | 54.9 ms: 1.02x slower                                                            |
| xml_etree_generate   | 76.2 ms                                                | 79.7 ms: 1.05x slower                                                            |
| pickle               | 9.79 us                                                | 10.3 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (2): unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.98 ms: 1.07x slower                                                            |
| python_startup_no_site | 5.96 ms                                                | 6.51 ms: 1.09x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 46.8 ms: 1.11x faster                                                            |
| genshi_text     | 22.1 ms                                                | 20.9 ms: 1.06x faster                                                            |
| mako            | 9.85 ms                                                | 9.92 ms: 1.01x slower                                                            |
| django_template | 32.5 ms                                                | 33.1 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.7 ms: 2.43x faster                                                            |
| json_dumps              | 12.7 ms                                                | 9.62 ms: 1.32x faster                                                            |
| deltablue               | 3.64 ms                                                | 3.11 ms: 1.17x faster                                                            |
| unpickle_pure_python    | 225 us                                                 | 196 us: 1.15x faster                                                             |
| coroutines              | 26.1 ms                                                | 22.7 ms: 1.15x faster                                                            |
| spectral_norm           | 99.9 ms                                                | 87.7 ms: 1.14x faster                                                            |
| richards                | 46.2 ms                                                | 40.9 ms: 1.13x faster                                                            |
| scimark_sor             | 115 ms                                                 | 103 ms: 1.12x faster                                                             |
| genshi_xml              | 52.1 ms                                                | 46.8 ms: 1.11x faster                                                            |
| scimark_fft             | 329 ms                                                 | 300 ms: 1.10x faster                                                             |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                                            |
| json                    | 4.95 ms                                                | 4.57 ms: 1.08x faster                                                            |
| nqueens                 | 85.0 ms                                                | 78.6 ms: 1.08x faster                                                            |
| fannkuch                | 388 ms                                                 | 361 ms: 1.07x faster                                                             |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                           |
| pickle_pure_python      | 304 us                                                 | 284 us: 1.07x faster                                                             |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                                             |
| logging_silent          | 98.5 ns                                                | 92.6 ns: 1.06x faster                                                            |
| nbody                   | 95.0 ms                                                | 89.7 ms: 1.06x faster                                                            |
| deepcopy_memo           | 36.4 us                                                | 34.4 us: 1.06x faster                                                            |
| float                   | 76.3 ms                                                | 72.2 ms: 1.06x faster                                                            |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.17 ms: 1.06x faster                                                            |
| genshi_text             | 22.1 ms                                                | 20.9 ms: 1.06x faster                                                            |
| sqlglot_optimize        | 53.0 ms                                                | 50.5 ms: 1.05x faster                                                            |
| raytrace                | 290 ms                                                 | 278 ms: 1.05x faster                                                             |
| logging_simple          | 6.06 us                                                | 5.81 us: 1.04x faster                                                            |
| hexiom                  | 6.35 ms                                                | 6.08 ms: 1.04x faster                                                            |
| logging_format          | 6.62 us                                                | 6.34 us: 1.04x faster                                                            |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.04x faster                                                             |
| xml_etree_iterparse     | 103 ms                                                 | 98.7 ms: 1.04x faster                                                            |
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                                             |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                            |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                                            |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                                             |
| bench_thread_pool       | 810 us                                                 | 784 us: 1.03x faster                                                             |
| deepcopy                | 344 us                                                 | 333 us: 1.03x faster                                                             |
| coverage                | 101 ms                                                 | 97.5 ms: 1.03x faster                                                            |
| regex_compile           | 136 ms                                                 | 132 ms: 1.03x faster                                                             |
| async_tree_io           | 1.31 sec                                               | 1.27 sec: 1.03x faster                                                           |
| html5lib                | 63.2 ms                                                | 61.4 ms: 1.03x faster                                                            |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.03x faster                                                            |
| async_tree_cpu_io_mixed | 752 ms                                                 | 732 ms: 1.03x faster                                                             |
| pyflate                 | 417 ms                                                 | 407 ms: 1.03x faster                                                             |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.03x faster                                                           |
| docutils                | 2.60 sec                                               | 2.53 sec: 1.02x faster                                                           |
| tornado_http            | 96.6 ms                                                | 94.3 ms: 1.02x faster                                                            |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.02x faster                                                             |
| pickle_dict             | 31.4 us                                                | 30.7 us: 1.02x faster                                                            |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                                            |
| sympy_str               | 287 ms                                                 | 283 ms: 1.02x faster                                                             |
| async_tree_none         | 529 ms                                                 | 521 ms: 1.02x faster                                                             |
| telco                   | 6.62 ms                                                | 6.53 ms: 1.01x faster                                                            |
| pickle_list             | 4.17 us                                                | 4.12 us: 1.01x faster                                                            |
| dulwich_log             | 63.9 ms                                                | 63.2 ms: 1.01x faster                                                            |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                                             |
| pprint_safe_repr        | 691 ms                                                 | 685 ms: 1.01x faster                                                             |
| crypto_pyaes            | 73.9 ms                                                | 73.5 ms: 1.01x faster                                                            |
| mdp                     | 2.62 sec                                               | 2.61 sec: 1.01x faster                                                           |
| regex_v8                | 22.3 ms                                                | 22.2 ms: 1.00x faster                                                            |
| sympy_sum               | 166 ms                                                 | 167 ms: 1.00x slower                                                             |
| thrift                  | 752 us                                                 | 756 us: 1.01x slower                                                             |
| mako                    | 9.85 ms                                                | 9.92 ms: 1.01x slower                                                            |
| chameleon               | 6.41 ms                                                | 6.51 ms: 1.02x slower                                                            |
| django_template         | 32.5 ms                                                | 33.1 ms: 1.02x slower                                                            |
| xml_etree_process       | 53.8 ms                                                | 54.9 ms: 1.02x slower                                                            |
| unpack_sequence         | 43.4 ns                                                | 44.3 ns: 1.02x slower                                                            |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                                            |
| regex_dna               | 203 ms                                                 | 209 ms: 1.03x slower                                                             |
| sqlglot_parse           | 1.37 ms                                                | 1.41 ms: 1.03x slower                                                            |
| async_tree_memoization  | 625 ms                                                 | 645 ms: 1.03x slower                                                             |
| xml_etree_generate      | 76.2 ms                                                | 79.7 ms: 1.05x slower                                                            |
| sqlite_synth            | 2.49 us                                                | 2.61 us: 1.05x slower                                                            |
| pickle                  | 9.79 us                                                | 10.3 us: 1.05x slower                                                            |
| python_startup          | 8.36 ms                                                | 8.98 ms: 1.07x slower                                                            |
| python_startup_no_site  | 5.96 ms                                                | 6.51 ms: 1.09x slower                                                            |
| async_generators        | 359 ms                                                 | 410 ms: 1.14x slower                                                             |
| Geometric mean          | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (10): scimark_monte_carlo, chaos, unpickle_list, sqlalchemy_imperative, bench_mp_pool, sqlalchemy_declarative, regex_effbot, deepcopy_reduce, scimark_lu, unpickle
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230227-3.12.0a5+-c29d369/bm-20230227-linux-x86_64-faster%2dcpython-check_refcnt_in_bina-3.12.0a5+-c29d369.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
