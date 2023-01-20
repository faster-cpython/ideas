
# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_superinstructions
- machine: linux-x86_64
- commit hash: b633237
- commit date: 2023-01-14
- overall geometric mean: 1.02x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 255 ms: 1.01x faster                                                         |
| chameleon      | 6.41 ms                                                | 6.49 ms: 1.01x slower                                                        |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                       |
| html5lib       | 63.2 ms                                                | 60.6 ms: 1.04x faster                                                        |
| tornado_http   | 96.6 ms                                                | 94.9 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.2 ms: 1.06x faster                                                        |
| nbody          | 95.0 ms                                                | 94.2 ms: 1.01x faster                                                        |
| pidigits       | 199 ms                                                 | 193 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 133 ms: 1.02x faster                                                         |
| regex_dna      | 203 ms                                                 | 207 ms: 1.02x slower                                                         |
| regex_effbot   | 3.36 ms                                                | 3.54 ms: 1.06x slower                                                        |
| regex_v8       | 22.3 ms                                                | 21.2 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                  | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.38 ms: 1.35x faster                                                        |
| json_loads           | 26.2 us                                                | 24.1 us: 1.09x faster                                                        |
| pickle               | 9.79 us                                                | 10.0 us: 1.03x slower                                                        |
| pickle_dict          | 31.4 us                                                | 29.5 us: 1.07x faster                                                        |
| pickle_list          | 4.17 us                                                | 4.02 us: 1.04x faster                                                        |
| pickle_pure_python   | 304 us                                                 | 287 us: 1.06x faster                                                         |
| unpickle             | 13.3 us                                                | 12.9 us: 1.03x faster                                                        |
| unpickle_list        | 4.95 us                                                | 4.91 us: 1.01x faster                                                        |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                                         |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                         |
| xml_etree_iterparse  | 103 ms                                                 | 105 ms: 1.02x slower                                                         |
| xml_etree_generate   | 76.2 ms                                                | 77.0 ms: 1.01x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.74 ms: 1.05x slower                                                        |
| python_startup_no_site | 5.96 ms                                                | 6.30 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.7 ms: 1.01x slower                                                        |
| genshi_text     | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                        |
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.11x faster                                                        |
| mako            | 9.85 ms                                                | 9.89 ms: 1.00x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 255 ms: 1.01x faster                                                         |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.04x faster                                                        |
| async_generators        | 359 ms                                                 | 356 ms: 1.01x faster                                                         |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                                       |
| async_tree_memoization  | 625 ms                                                 | 658 ms: 1.05x slower                                                         |
| chameleon               | 6.41 ms                                                | 6.49 ms: 1.01x slower                                                        |
| chaos                   | 68.6 ms                                                | 70.4 ms: 1.03x slower                                                        |
| bench_thread_pool       | 810 us                                                 | 784 us: 1.03x faster                                                         |
| coroutines              | 26.1 ms                                                | 25.0 ms: 1.04x faster                                                        |
| coverage                | 101 ms                                                 | 96.2 ms: 1.04x faster                                                        |
| crypto_pyaes            | 73.9 ms                                                | 77.7 ms: 1.05x slower                                                        |
| deepcopy                | 344 us                                                 | 336 us: 1.02x faster                                                         |
| deepcopy_memo           | 36.4 us                                                | 36.1 us: 1.01x faster                                                        |
| deltablue               | 3.64 ms                                                | 3.23 ms: 1.13x faster                                                        |
| django_template         | 32.5 ms                                                | 32.7 ms: 1.01x slower                                                        |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                       |
| dulwich_log             | 63.9 ms                                                | 62.4 ms: 1.02x faster                                                        |
| fannkuch                | 388 ms                                                 | 374 ms: 1.04x faster                                                         |
| float                   | 76.3 ms                                                | 72.2 ms: 1.06x faster                                                        |
| generators              | 72.2 ms                                                | 74.6 ms: 1.03x slower                                                        |
| genshi_text             | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                        |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.11x faster                                                        |
| go                      | 143 ms                                                 | 137 ms: 1.05x faster                                                         |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                                        |
| hexiom                  | 6.35 ms                                                | 6.18 ms: 1.03x faster                                                        |
| html5lib                | 63.2 ms                                                | 60.6 ms: 1.04x faster                                                        |
| json                    | 4.95 ms                                                | 4.71 ms: 1.05x faster                                                        |
| json_dumps              | 12.7 ms                                                | 9.38 ms: 1.35x faster                                                        |
| json_loads              | 26.2 us                                                | 24.1 us: 1.09x faster                                                        |
| logging_format          | 6.62 us                                                | 6.52 us: 1.01x faster                                                        |
| logging_silent          | 98.5 ns                                                | 91.7 ns: 1.07x faster                                                        |
| logging_simple          | 6.06 us                                                | 5.82 us: 1.04x faster                                                        |
| mako                    | 9.85 ms                                                | 9.89 ms: 1.00x slower                                                        |
| mdp                     | 2.62 sec                                               | 2.61 sec: 1.01x faster                                                       |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                                         |
| mypy                    | 669 ms                                                 | 821 ms: 1.23x slower                                                         |
| nbody                   | 95.0 ms                                                | 94.2 ms: 1.01x faster                                                        |
| nqueens                 | 85.0 ms                                                | 79.4 ms: 1.07x faster                                                        |
| pathlib                 | 18.2 ms                                                | 18.2 ms: 1.00x slower                                                        |
| pickle                  | 9.79 us                                                | 10.0 us: 1.03x slower                                                        |
| pickle_dict             | 31.4 us                                                | 29.5 us: 1.07x faster                                                        |
| pickle_list             | 4.17 us                                                | 4.02 us: 1.04x faster                                                        |
| pickle_pure_python      | 304 us                                                 | 287 us: 1.06x faster                                                         |
| pidigits                | 199 ms                                                 | 193 ms: 1.03x faster                                                         |
| pprint_safe_repr        | 691 ms                                                 | 676 ms: 1.02x faster                                                         |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.04x faster                                                       |
| pycparser               | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                       |
| pyflate                 | 417 ms                                                 | 398 ms: 1.05x faster                                                         |
| python_startup          | 8.36 ms                                                | 8.74 ms: 1.05x slower                                                        |
| python_startup_no_site  | 5.96 ms                                                | 6.30 ms: 1.06x slower                                                        |
| raytrace                | 290 ms                                                 | 288 ms: 1.01x faster                                                         |
| regex_compile           | 136 ms                                                 | 133 ms: 1.02x faster                                                         |
| regex_dna               | 203 ms                                                 | 207 ms: 1.02x slower                                                         |
| regex_effbot            | 3.36 ms                                                | 3.54 ms: 1.06x slower                                                        |
| regex_v8                | 22.3 ms                                                | 21.2 ms: 1.05x faster                                                        |
| richards                | 46.2 ms                                                | 44.0 ms: 1.05x faster                                                        |
| scimark_fft             | 329 ms                                                 | 317 ms: 1.04x faster                                                         |
| scimark_monte_carlo     | 68.3 ms                                                | 66.1 ms: 1.03x faster                                                        |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.07x faster                                                         |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.13 ms: 1.07x faster                                                        |
| spectral_norm           | 99.9 ms                                                | 98.0 ms: 1.02x faster                                                        |
| sqlglot_parse           | 1.37 ms                                                | 1.40 ms: 1.02x slower                                                        |
| sqlglot_transpile       | 1.66 ms                                                | 1.70 ms: 1.03x slower                                                        |
| sqlglot_optimize        | 53.0 ms                                                | 51.4 ms: 1.03x faster                                                        |
| sqlglot_normalize       | 108 ms                                                 | 106 ms: 1.02x faster                                                         |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.03x slower                                                        |
| sympy_expand            | 472 ms                                                 | 466 ms: 1.01x faster                                                         |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                                        |
| telco                   | 6.62 ms                                                | 6.43 ms: 1.03x faster                                                        |
| tornado_http            | 96.6 ms                                                | 94.9 ms: 1.02x faster                                                        |
| unpack_sequence         | 43.4 ns                                                | 49.0 ns: 1.13x slower                                                        |
| unpickle                | 13.3 us                                                | 12.9 us: 1.03x faster                                                        |
| unpickle_list           | 4.95 us                                                | 4.91 us: 1.01x faster                                                        |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                                         |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                         |
| xml_etree_iterparse     | 103 ms                                                 | 105 ms: 1.02x slower                                                         |
| xml_etree_generate      | 76.2 ms                                                | 77.0 ms: 1.01x slower                                                        |
| Geometric mean          | (ref)                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (9): async_tree_none, async_tree_cpu_io_mixed, bench_mp_pool, deepcopy_reduce, scimark_lu, sympy_sum, sympy_str, thrift, xml_etree_process
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230114-3.12.0a4+-b633237/bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
