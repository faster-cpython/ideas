
# Results vs. base

- fork: brandtbucher
- ref: no_superinstructions
- machine: linux-x86_64
- commit hash: b633237
- commit date: 2023-01-14
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 255 ms: 1.02x slower                                                         |
| chameleon      | 6.23 ms                                                                | 6.49 ms: 1.04x slower                                                        |
| docutils       | 2.49 sec                                                               | 2.50 sec: 1.00x slower                                                       |
| html5lib       | 59.5 ms                                                                | 60.6 ms: 1.02x slower                                                        |
| tornado_http   | 93.3 ms                                                                | 94.9 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 193 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                 |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 130 ms                                                                 | 133 ms: 1.02x slower                                                         |
| regex_dna      | 210 ms                                                                 | 207 ms: 1.01x faster                                                         |
| regex_v8       | 22.3 ms                                                                | 21.2 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle               | 9.96 us                                                                | 10.0 us: 1.01x slower                                                        |
| pickle_dict          | 31.0 us                                                                | 29.5 us: 1.05x faster                                                        |
| pickle_pure_python   | 279 us                                                                 | 287 us: 1.03x slower                                                         |
| unpickle_list        | 4.94 us                                                                | 4.91 us: 1.01x faster                                                        |
| unpickle_pure_python | 198 us                                                                 | 201 us: 1.01x slower                                                         |
| xml_etree_iterparse  | 108 ms                                                                 | 105 ms: 1.03x faster                                                         |
| xml_etree_generate   | 77.7 ms                                                                | 77.0 ms: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (6): json_dumps, json_loads, pickle_list, unpickle, xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.84 ms                                                                | 8.74 ms: 1.01x faster                                                        |
| python_startup_no_site | 6.40 ms                                                                | 6.30 ms: 1.02x faster                                                        |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 32.2 ms                                                                | 32.7 ms: 1.02x slower                                                        |
| genshi_xml      | 46.5 ms                                                                | 47.1 ms: 1.01x slower                                                        |
| mako            | 9.43 ms                                                                | 9.89 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20230119-linux-x86_64-python-8a2d4f4e8eea86352de3-3.12.0a4+-8a2d4f4 | bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4+-b633237 |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3                    | 252 ms                                                                 | 255 ms: 1.02x slower                                                         |
| aiohttp                 | 992 us                                                                 | 1.00 ms: 1.01x slower                                                        |
| async_generators        | 354 ms                                                                 | 356 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed | 739 ms                                                                 | 749 ms: 1.01x slower                                                         |
| chameleon               | 6.23 ms                                                                | 6.49 ms: 1.04x slower                                                        |
| chaos                   | 68.6 ms                                                                | 70.4 ms: 1.03x slower                                                        |
| bench_thread_pool       | 779 us                                                                 | 784 us: 1.01x slower                                                         |
| coroutines              | 24.9 ms                                                                | 25.0 ms: 1.01x slower                                                        |
| coverage                | 97.7 ms                                                                | 96.2 ms: 1.02x faster                                                        |
| crypto_pyaes            | 76.0 ms                                                                | 77.7 ms: 1.02x slower                                                        |
| dask                    | 496 ms                                                                 | 507 ms: 1.02x slower                                                         |
| deepcopy                | 327 us                                                                 | 336 us: 1.03x slower                                                         |
| deepcopy_reduce         | 2.92 us                                                                | 2.95 us: 1.01x slower                                                        |
| deepcopy_memo           | 33.7 us                                                                | 36.1 us: 1.07x slower                                                        |
| deltablue               | 3.18 ms                                                                | 3.23 ms: 1.01x slower                                                        |
| django_template         | 32.2 ms                                                                | 32.7 ms: 1.02x slower                                                        |
| djangocms               | 32.0 us                                                                | 32.9 us: 1.03x slower                                                        |
| docutils                | 2.49 sec                                                               | 2.50 sec: 1.00x slower                                                       |
| dulwich_log             | 61.2 ms                                                                | 62.4 ms: 1.02x slower                                                        |
| fannkuch                | 378 ms                                                                 | 374 ms: 1.01x faster                                                         |
| gc_traversal            | 4.16 ms                                                                | 3.50 ms: 1.19x faster                                                        |
| generators              | 77.8 ms                                                                | 74.6 ms: 1.04x faster                                                        |
| genshi_xml              | 46.5 ms                                                                | 47.1 ms: 1.01x slower                                                        |
| go                      | 134 ms                                                                 | 137 ms: 1.02x slower                                                         |
| gunicorn                | 1.06 ms                                                                | 1.08 ms: 1.02x slower                                                        |
| hexiom                  | 6.03 ms                                                                | 6.18 ms: 1.02x slower                                                        |
| html5lib                | 59.5 ms                                                                | 60.6 ms: 1.02x slower                                                        |
| logging_format          | 6.19 us                                                                | 6.52 us: 1.05x slower                                                        |
| logging_silent          | 90.8 ns                                                                | 91.7 ns: 1.01x slower                                                        |
| logging_simple          | 5.61 us                                                                | 5.82 us: 1.04x slower                                                        |
| mako                    | 9.43 ms                                                                | 9.89 ms: 1.05x slower                                                        |
| mdp                     | 2.45 sec                                                               | 2.61 sec: 1.06x slower                                                       |
| pathlib                 | 17.7 ms                                                                | 18.2 ms: 1.03x slower                                                        |
| pickle                  | 9.96 us                                                                | 10.0 us: 1.01x slower                                                        |
| pickle_dict             | 31.0 us                                                                | 29.5 us: 1.05x faster                                                        |
| pickle_pure_python      | 279 us                                                                 | 287 us: 1.03x slower                                                         |
| pidigits                | 190 ms                                                                 | 193 ms: 1.02x slower                                                         |
| pprint_safe_repr        | 670 ms                                                                 | 676 ms: 1.01x slower                                                         |
| pycparser               | 1.14 sec                                                               | 1.11 sec: 1.03x faster                                                       |
| pyflate                 | 401 ms                                                                 | 398 ms: 1.01x faster                                                         |
| python_startup          | 8.84 ms                                                                | 8.74 ms: 1.01x faster                                                        |
| python_startup_no_site  | 6.40 ms                                                                | 6.30 ms: 1.02x faster                                                        |
| raytrace                | 283 ms                                                                 | 288 ms: 1.02x slower                                                         |
| regex_compile           | 130 ms                                                                 | 133 ms: 1.02x slower                                                         |
| regex_dna               | 210 ms                                                                 | 207 ms: 1.01x faster                                                         |
| regex_v8                | 22.3 ms                                                                | 21.2 ms: 1.05x faster                                                        |
| richards                | 42.0 ms                                                                | 44.0 ms: 1.05x slower                                                        |
| scimark_fft             | 308 ms                                                                 | 317 ms: 1.03x slower                                                         |
| scimark_lu              | 108 ms                                                                 | 106 ms: 1.01x faster                                                         |
| scimark_sor             | 105 ms                                                                 | 107 ms: 1.02x slower                                                         |
| sqlglot_parse           | 1.39 ms                                                                | 1.40 ms: 1.01x slower                                                        |
| sqlglot_transpile       | 1.68 ms                                                                | 1.70 ms: 1.01x slower                                                        |
| sqlglot_optimize        | 51.1 ms                                                                | 51.4 ms: 1.01x slower                                                        |
| sqlite_synth            | 2.60 us                                                                | 2.58 us: 1.01x faster                                                        |
| sympy_expand            | 459 ms                                                                 | 466 ms: 1.01x slower                                                         |
| sympy_integrate         | 20.4 ms                                                                | 20.5 ms: 1.01x slower                                                        |
| sympy_sum               | 164 ms                                                                 | 165 ms: 1.01x slower                                                         |
| sympy_str               | 283 ms                                                                 | 288 ms: 1.02x slower                                                         |
| telco                   | 6.49 ms                                                                | 6.43 ms: 1.01x faster                                                        |
| tornado_http            | 93.3 ms                                                                | 94.9 ms: 1.02x slower                                                        |
| unpack_sequence         | 41.6 ns                                                                | 49.0 ns: 1.18x slower                                                        |
| unpickle_list           | 4.94 us                                                                | 4.91 us: 1.01x faster                                                        |
| unpickle_pure_python    | 198 us                                                                 | 201 us: 1.01x slower                                                         |
| xml_etree_iterparse     | 108 ms                                                                 | 105 ms: 1.03x faster                                                         |
| xml_etree_generate      | 77.7 ms                                                                | 77.0 ms: 1.01x faster                                                        |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                                 |

Benchmark hidden because not significant (26): async_tree_none, async_tree_io, async_tree_memoization, asyncio_tcp, bench_mp_pool, float, create_gc_cycles, genshi_text, json, json_dumps, json_loads, meteor_contest, mypy, nbody, nqueens, pickle_list, pprint_pformat, regex_effbot, scimark_monte_carlo, scimark_sparse_mat_mult, spectral_norm, sqlglot_normalize, thrift, unpickle, xml_etree_parse, xml_etree_process
