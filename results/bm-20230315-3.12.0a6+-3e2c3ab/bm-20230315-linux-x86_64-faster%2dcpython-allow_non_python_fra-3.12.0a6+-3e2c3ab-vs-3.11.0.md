
# Results vs. 3.11.0

- fork: faster-cpython
- ref: allow_non_python_fra
- machine: linux-x86_64
- commit hash: 3e2c3ab
- commit date: 2023-03-15
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                                             |
| docutils       | 2.60 sec                                               | 2.55 sec: 1.02x faster                                                           |
| html5lib       | 63.2 ms                                                | 62.1 ms: 1.02x faster                                                            |
| tornado_http   | 96.6 ms                                                | 95.2 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                                             |
| float          | 76.3 ms                                                | 75.2 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                            |
| regex_compile  | 136 ms                                                 | 134 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.55 ms: 1.33x faster                                                            |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                                             |
| json_loads           | 26.2 us                                                | 24.4 us: 1.07x faster                                                            |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| pickle_pure_python   | 304 us                                                 | 286 us: 1.06x faster                                                             |
| xml_etree_iterparse  | 103 ms                                                 | 99.4 ms: 1.03x faster                                                            |
| pickle_list          | 4.17 us                                                | 4.12 us: 1.01x faster                                                            |
| pickle_dict          | 31.4 us                                                | 31.1 us: 1.01x faster                                                            |
| unpickle_list        | 4.95 us                                                | 5.05 us: 1.02x slower                                                            |
| xml_etree_process    | 53.8 ms                                                | 55.2 ms: 1.03x slower                                                            |
| unpickle             | 13.3 us                                                | 13.8 us: 1.04x slower                                                            |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                                            |
| xml_etree_generate   | 76.2 ms                                                | 81.0 ms: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.02 ms: 1.08x slower                                                            |
| python_startup_no_site | 5.96 ms                                                | 6.54 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.7 ms: 1.09x faster                                                            |
| genshi_text     | 22.1 ms                                                | 21.5 ms: 1.03x faster                                                            |
| mako            | 9.85 ms                                                | 10.0 ms: 1.02x slower                                                            |
| django_template | 32.5 ms                                                | 33.5 ms: 1.03x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.3 ms: 2.46x faster                                                            |
| json_dumps              | 12.7 ms                                                | 9.55 ms: 1.33x faster                                                            |
| coroutines              | 26.1 ms                                                | 22.9 ms: 1.14x faster                                                            |
| deltablue               | 3.64 ms                                                | 3.21 ms: 1.13x faster                                                            |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                                             |
| genshi_xml              | 52.1 ms                                                | 47.7 ms: 1.09x faster                                                            |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| coverage                | 101 ms                                                 | 93.6 ms: 1.07x faster                                                            |
| json_loads              | 26.2 us                                                | 24.4 us: 1.07x faster                                                            |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| json                    | 4.95 ms                                                | 4.64 ms: 1.07x faster                                                            |
| pickle_pure_python      | 304 us                                                 | 286 us: 1.06x faster                                                             |
| deepcopy_memo           | 36.4 us                                                | 34.4 us: 1.06x faster                                                            |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                                             |
| richards                | 46.2 ms                                                | 44.0 ms: 1.05x faster                                                            |
| go                      | 143 ms                                                 | 137 ms: 1.05x faster                                                             |
| nqueens                 | 85.0 ms                                                | 81.1 ms: 1.05x faster                                                            |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                                             |
| sqlglot_optimize        | 53.0 ms                                                | 50.8 ms: 1.04x faster                                                            |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                            |
| pycparser               | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                           |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                                             |
| pprint_pformat          | 1.44 sec                                               | 1.39 sec: 1.04x faster                                                           |
| logging_simple          | 6.06 us                                                | 5.86 us: 1.03x faster                                                            |
| xml_etree_iterparse     | 103 ms                                                 | 99.4 ms: 1.03x faster                                                            |
| logging_format          | 6.62 us                                                | 6.41 us: 1.03x faster                                                            |
| genshi_text             | 22.1 ms                                                | 21.5 ms: 1.03x faster                                                            |
| scimark_fft             | 329 ms                                                 | 319 ms: 1.03x faster                                                             |
| deepcopy                | 344 us                                                 | 335 us: 1.03x faster                                                             |
| logging_silent          | 98.5 ns                                                | 96.1 ns: 1.02x faster                                                            |
| gunicorn                | 1.12 ms                                                | 1.10 ms: 1.02x faster                                                            |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                            |
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                                             |
| spectral_norm           | 99.9 ms                                                | 97.8 ms: 1.02x faster                                                            |
| bench_thread_pool       | 810 us                                                 | 793 us: 1.02x faster                                                             |
| sympy_expand            | 472 ms                                                 | 462 ms: 1.02x faster                                                             |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                            |
| pyflate                 | 417 ms                                                 | 409 ms: 1.02x faster                                                             |
| docutils                | 2.60 sec                                               | 2.55 sec: 1.02x faster                                                           |
| html5lib                | 63.2 ms                                                | 62.1 ms: 1.02x faster                                                            |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                                            |
| telco                   | 6.62 ms                                                | 6.52 ms: 1.02x faster                                                            |
| float                   | 76.3 ms                                                | 75.2 ms: 1.02x faster                                                            |
| tornado_http            | 96.6 ms                                                | 95.2 ms: 1.02x faster                                                            |
| pickle_list             | 4.17 us                                                | 4.12 us: 1.01x faster                                                            |
| regex_compile           | 136 ms                                                 | 134 ms: 1.01x faster                                                             |
| hexiom                  | 6.35 ms                                                | 6.27 ms: 1.01x faster                                                            |
| raytrace                | 290 ms                                                 | 287 ms: 1.01x faster                                                             |
| pprint_safe_repr        | 691 ms                                                 | 683 ms: 1.01x faster                                                             |
| chaos                   | 68.6 ms                                                | 67.9 ms: 1.01x faster                                                            |
| pickle_dict             | 31.4 us                                                | 31.1 us: 1.01x faster                                                            |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                                             |
| sympy_str               | 287 ms                                                 | 285 ms: 1.01x faster                                                             |
| scimark_monte_carlo     | 68.3 ms                                                | 67.8 ms: 1.01x faster                                                            |
| mdp                     | 2.62 sec                                               | 2.63 sec: 1.00x slower                                                           |
| crypto_pyaes            | 73.9 ms                                                | 74.2 ms: 1.00x slower                                                            |
| unpack_sequence         | 43.4 ns                                                | 43.8 ns: 1.01x slower                                                            |
| sympy_sum               | 166 ms                                                 | 168 ms: 1.01x slower                                                             |
| mako                    | 9.85 ms                                                | 10.0 ms: 1.02x slower                                                            |
| unpickle_list           | 4.95 us                                                | 5.05 us: 1.02x slower                                                            |
| xml_etree_process       | 53.8 ms                                                | 55.2 ms: 1.03x slower                                                            |
| django_template         | 32.5 ms                                                | 33.5 ms: 1.03x slower                                                            |
| unpickle                | 13.3 us                                                | 13.8 us: 1.04x slower                                                            |
| sqlglot_transpile       | 1.66 ms                                                | 1.72 ms: 1.04x slower                                                            |
| scimark_lu              | 107 ms                                                 | 112 ms: 1.04x slower                                                             |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                                            |
| sqlglot_parse           | 1.37 ms                                                | 1.44 ms: 1.05x slower                                                            |
| async_tree_memoization  | 625 ms                                                 | 660 ms: 1.06x slower                                                             |
| thrift                  | 752 us                                                 | 796 us: 1.06x slower                                                             |
| xml_etree_generate      | 76.2 ms                                                | 81.0 ms: 1.06x slower                                                            |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.68 ms: 1.06x slower                                                            |
| sqlite_synth            | 2.49 us                                                | 2.65 us: 1.06x slower                                                            |
| python_startup          | 8.36 ms                                                | 9.02 ms: 1.08x slower                                                            |
| python_startup_no_site  | 5.96 ms                                                | 6.54 ms: 1.10x slower                                                            |
| async_generators        | 359 ms                                                 | 413 ms: 1.15x slower                                                             |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (12): async_tree_cpu_io_mixed, sqlalchemy_declarative, async_tree_none, deepcopy_reduce, async_tree_io, dulwich_log, sqlalchemy_imperative, bench_mp_pool, regex_dna, regex_effbot, chameleon, nbody
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230315-3.12.0a6+-3e2c3ab/bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
