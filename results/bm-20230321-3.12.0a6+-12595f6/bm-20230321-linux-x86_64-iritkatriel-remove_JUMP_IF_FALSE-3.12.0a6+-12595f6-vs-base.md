
# Results vs. base

- fork: iritkatriel
- ref: remove_JUMP_IF_FALSE
- machine: linux-x86_64
- commit hash: 12595f6
- commit date: 2023-03-21
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 249 ms: 1.00x slower                                                        |
| chameleon      | 6.32 ms                                                                | 6.56 ms: 1.04x slower                                                       |
| docutils       | 2.52 sec                                                               | 2.54 sec: 1.01x slower                                                      |
| tornado_http   | 90.6 ms                                                                | 91.5 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 189 ms: 1.02x faster                                                        |
| nbody          | 86.8 ms                                                                | 87.2 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 206 ms                                                                 | 201 ms: 1.02x faster                                                        |
| regex_v8       | 21.9 ms                                                                | 22.0 ms: 1.00x slower                                                       |
| regex_compile  | 132 ms                                                                 | 134 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_list         | 4.17 us                                                                | 4.08 us: 1.02x faster                                                       |
| pickle              | 10.3 us                                                                | 10.2 us: 1.01x faster                                                       |
| json_loads          | 24.2 us                                                                | 24.0 us: 1.01x faster                                                       |
| pickle_dict         | 30.9 us                                                                | 30.8 us: 1.00x faster                                                       |
| xml_etree_generate  | 81.0 ms                                                                | 81.6 ms: 1.01x slower                                                       |
| xml_etree_parse     | 149 ms                                                                 | 150 ms: 1.01x slower                                                        |
| json_dumps          | 9.43 ms                                                                | 9.51 ms: 1.01x slower                                                       |
| pickle_pure_python  | 283 us                                                                 | 287 us: 1.01x slower                                                        |
| xml_etree_process   | 55.6 ms                                                                | 56.8 ms: 1.02x slower                                                       |
| xml_etree_iterparse | 99.5 ms                                                                | 103 ms: 1.03x slower                                                        |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                                |

Benchmark hidden because not significant (3): unpickle_list, unpickle_pure_python, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.89 ms                                                                | 8.87 ms: 1.00x faster                                                       |
| python_startup_no_site | 6.51 ms                                                                | 6.50 ms: 1.00x faster                                                       |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.90 ms                                                                | 10.0 ms: 1.01x slower                                                       |
| genshi_text    | 21.1 ms                                                                | 21.8 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark               | bm-20230321-linux-x86_64-python-7f760c2fca3dc5f46a51-3.12.0a6+-7f760c2 | bm-20230321-linux-x86_64-iritkatriel-remove_JUMP_IF_FALSE-3.12.0a6+-12595f6 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                     | 2.55 sec                                                               | 2.43 sec: 1.05x faster                                                      |
| thrift                  | 793 us                                                                 | 773 us: 1.03x faster                                                        |
| regex_dna               | 206 ms                                                                 | 201 ms: 1.02x faster                                                        |
| spectral_norm           | 90.6 ms                                                                | 88.6 ms: 1.02x faster                                                       |
| pickle_list             | 4.17 us                                                                | 4.08 us: 1.02x faster                                                       |
| scimark_sor             | 106 ms                                                                 | 104 ms: 1.02x faster                                                        |
| pidigits                | 193 ms                                                                 | 189 ms: 1.02x faster                                                        |
| coroutines              | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                       |
| pathlib                 | 18.0 ms                                                                | 17.8 ms: 1.01x faster                                                       |
| pickle                  | 10.3 us                                                                | 10.2 us: 1.01x faster                                                       |
| sympy_expand            | 462 ms                                                                 | 459 ms: 1.01x faster                                                        |
| json_loads              | 24.2 us                                                                | 24.0 us: 1.01x faster                                                       |
| crypto_pyaes            | 73.8 ms                                                                | 73.4 ms: 1.01x faster                                                       |
| pickle_dict             | 30.9 us                                                                | 30.8 us: 1.00x faster                                                       |
| python_startup          | 8.89 ms                                                                | 8.87 ms: 1.00x faster                                                       |
| python_startup_no_site  | 6.51 ms                                                                | 6.50 ms: 1.00x faster                                                       |
| regex_v8                | 21.9 ms                                                                | 22.0 ms: 1.00x slower                                                       |
| 2to3                    | 248 ms                                                                 | 249 ms: 1.00x slower                                                        |
| hexiom                  | 6.09 ms                                                                | 6.11 ms: 1.00x slower                                                       |
| dulwich_log             | 63.1 ms                                                                | 63.3 ms: 1.00x slower                                                       |
| nbody                   | 86.8 ms                                                                | 87.2 ms: 1.00x slower                                                       |
| raytrace                | 282 ms                                                                 | 283 ms: 1.01x slower                                                        |
| bench_thread_pool       | 784 us                                                                 | 788 us: 1.01x slower                                                        |
| xml_etree_generate      | 81.0 ms                                                                | 81.6 ms: 1.01x slower                                                       |
| asyncio_tcp             | 508 ms                                                                 | 512 ms: 1.01x slower                                                        |
| docutils                | 2.52 sec                                                               | 2.54 sec: 1.01x slower                                                      |
| xml_etree_parse         | 149 ms                                                                 | 150 ms: 1.01x slower                                                        |
| json_dumps              | 9.43 ms                                                                | 9.51 ms: 1.01x slower                                                       |
| aiohttp                 | 1.00 ms                                                                | 1.01 ms: 1.01x slower                                                       |
| tornado_http            | 90.6 ms                                                                | 91.5 ms: 1.01x slower                                                       |
| deltablue               | 3.16 ms                                                                | 3.18 ms: 1.01x slower                                                       |
| gunicorn                | 1.08 ms                                                                | 1.09 ms: 1.01x slower                                                       |
| meteor_contest          | 102 ms                                                                 | 103 ms: 1.01x slower                                                        |
| sqlglot_normalize       | 105 ms                                                                 | 106 ms: 1.01x slower                                                        |
| regex_compile           | 132 ms                                                                 | 134 ms: 1.01x slower                                                        |
| chaos                   | 65.8 ms                                                                | 66.6 ms: 1.01x slower                                                       |
| pickle_pure_python      | 283 us                                                                 | 287 us: 1.01x slower                                                        |
| go                      | 132 ms                                                                 | 134 ms: 1.01x slower                                                        |
| pycparser               | 1.11 sec                                                               | 1.13 sec: 1.01x slower                                                      |
| telco                   | 6.43 ms                                                                | 6.51 ms: 1.01x slower                                                       |
| create_gc_cycles        | 1.48 ms                                                                | 1.50 ms: 1.01x slower                                                       |
| mako                    | 9.90 ms                                                                | 10.0 ms: 1.01x slower                                                       |
| pyflate                 | 402 ms                                                                 | 407 ms: 1.01x slower                                                        |
| dask                    | 500 ms                                                                 | 508 ms: 1.01x slower                                                        |
| scimark_monte_carlo     | 65.2 ms                                                                | 66.2 ms: 1.02x slower                                                       |
| deepcopy                | 325 us                                                                 | 330 us: 1.02x slower                                                        |
| sqlglot_transpile       | 1.72 ms                                                                | 1.74 ms: 1.02x slower                                                       |
| deepcopy_memo           | 34.1 us                                                                | 34.6 us: 1.02x slower                                                       |
| sqlglot_parse           | 1.43 ms                                                                | 1.45 ms: 1.02x slower                                                       |
| deepcopy_reduce         | 2.93 us                                                                | 2.98 us: 1.02x slower                                                       |
| logging_simple          | 5.67 us                                                                | 5.78 us: 1.02x slower                                                       |
| comprehensions          | 23.4 us                                                                | 23.9 us: 1.02x slower                                                       |
| xml_etree_process       | 55.6 ms                                                                | 56.8 ms: 1.02x slower                                                       |
| scimark_fft             | 302 ms                                                                 | 309 ms: 1.02x slower                                                        |
| async_tree_memoization  | 648 ms                                                                 | 666 ms: 1.03x slower                                                        |
| genshi_text             | 21.1 ms                                                                | 21.8 ms: 1.03x slower                                                       |
| xml_etree_iterparse     | 99.5 ms                                                                | 103 ms: 1.03x slower                                                        |
| pprint_safe_repr        | 686 ms                                                                 | 711 ms: 1.04x slower                                                        |
| chameleon               | 6.32 ms                                                                | 6.56 ms: 1.04x slower                                                       |
| pprint_pformat          | 1.39 sec                                                               | 1.45 sec: 1.04x slower                                                      |
| richards                | 41.8 ms                                                                | 43.5 ms: 1.04x slower                                                       |
| unpack_sequence         | 42.4 ns                                                                | 44.2 ns: 1.04x slower                                                       |
| logging_silent          | 94.2 ns                                                                | 98.4 ns: 1.04x slower                                                       |
| scimark_sparse_mat_mult | 4.10 ms                                                                | 4.32 ms: 1.05x slower                                                       |
| gc_traversal            | 3.54 ms                                                                | 3.83 ms: 1.08x slower                                                       |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                                |

Benchmark hidden because not significant (29): scimark_lu, djangocms, coverage, async_tree_io, genshi_xml, json, sympy_str, regex_effbot, nqueens, sqlglot_optimize, unpickle_list, unpickle_pure_python, bench_mp_pool, sqlalchemy_declarative, generators, sympy_sum, sympy_integrate, mypy2, django_template, async_tree_none, logging_format, float, async_generators, sqlite_synth, async_tree_cpu_io_mixed, html5lib, fannkuch, unpickle, sqlalchemy_imperative
