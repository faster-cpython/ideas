
# Results vs. base

- fork: faster-cpython
- ref: long_rearrange_size_
- machine: linux-x86_64
- commit hash: ce6bfb2
- commit date: 2023-03-02
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 251 ms: 1.01x faster                                                             |
| chameleon      | 6.35 ms                                                                | 6.43 ms: 1.01x slower                                                            |
| docutils       | 2.56 sec                                                               | 2.55 sec: 1.00x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 188 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                                | 21.5 ms: 1.04x faster                                                            |
| regex_effbot   | 3.35 ms                                                                | 3.44 ms: 1.03x slower                                                            |
| regex_dna      | 210 ms                                                                 | 219 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 295 us                                                                 | 285 us: 1.03x faster                                                             |
| xml_etree_parse      | 151 ms                                                                 | 148 ms: 1.02x faster                                                             |
| xml_etree_generate   | 82.4 ms                                                                | 80.8 ms: 1.02x faster                                                            |
| xml_etree_process    | 56.6 ms                                                                | 55.7 ms: 1.02x faster                                                            |
| unpickle_list        | 5.07 us                                                                | 5.00 us: 1.01x faster                                                            |
| json_dumps           | 9.48 ms                                                                | 9.41 ms: 1.01x faster                                                            |
| unpickle_pure_python | 202 us                                                                 | 200 us: 1.01x faster                                                             |
| json_loads           | 23.7 us                                                                | 23.9 us: 1.01x slower                                                            |
| unpickle             | 13.4 us                                                                | 13.6 us: 1.02x slower                                                            |
| pickle               | 9.98 us                                                                | 10.1 us: 1.02x slower                                                            |
| pickle_dict          | 30.0 us                                                                | 30.9 us: 1.03x slower                                                            |
| pickle_list          | 4.02 us                                                                | 4.15 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.53 ms                                                                | 6.53 ms: 1.00x slower                                                            |
| python_startup         | 9.01 ms                                                                | 9.02 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 21.8 ms                                                                | 21.2 ms: 1.03x faster                                                            |
| mako            | 9.97 ms                                                                | 9.86 ms: 1.01x faster                                                            |
| django_template | 32.9 ms                                                                | 32.7 ms: 1.01x faster                                                            |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20230228-linux-x86_64-python-4c87537efb5fd28b4e4e-3.12.0a5+-4c87537 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8                | 22.3 ms                                                                | 21.5 ms: 1.04x faster                                                            |
| pickle_pure_python      | 295 us                                                                 | 285 us: 1.03x faster                                                             |
| unpack_sequence         | 43.2 ns                                                                | 41.9 ns: 1.03x faster                                                            |
| genshi_text             | 21.8 ms                                                                | 21.2 ms: 1.03x faster                                                            |
| nqueens                 | 82.7 ms                                                                | 80.4 ms: 1.03x faster                                                            |
| coroutines              | 23.7 ms                                                                | 23.1 ms: 1.03x faster                                                            |
| chaos                   | 69.5 ms                                                                | 67.6 ms: 1.03x faster                                                            |
| pprint_pformat          | 1.42 sec                                                               | 1.39 sec: 1.03x faster                                                           |
| xml_etree_parse         | 151 ms                                                                 | 148 ms: 1.02x faster                                                             |
| sqlglot_parse           | 1.47 ms                                                                | 1.43 ms: 1.02x faster                                                            |
| fannkuch                | 368 ms                                                                 | 360 ms: 1.02x faster                                                             |
| go                      | 139 ms                                                                 | 136 ms: 1.02x faster                                                             |
| pprint_safe_repr        | 687 ms                                                                 | 672 ms: 1.02x faster                                                             |
| sqlglot_normalize       | 106 ms                                                                 | 104 ms: 1.02x faster                                                             |
| raytrace                | 295 ms                                                                 | 289 ms: 1.02x faster                                                             |
| xml_etree_generate      | 82.4 ms                                                                | 80.8 ms: 1.02x faster                                                            |
| logging_format          | 6.42 us                                                                | 6.30 us: 1.02x faster                                                            |
| scimark_monte_carlo     | 68.3 ms                                                                | 67.1 ms: 1.02x faster                                                            |
| logging_simple          | 5.88 us                                                                | 5.78 us: 1.02x faster                                                            |
| sqlglot_transpile       | 1.76 ms                                                                | 1.73 ms: 1.02x faster                                                            |
| xml_etree_process       | 56.6 ms                                                                | 55.7 ms: 1.02x faster                                                            |
| unpickle_list           | 5.07 us                                                                | 5.00 us: 1.01x faster                                                            |
| sympy_expand            | 466 ms                                                                 | 460 ms: 1.01x faster                                                             |
| mako                    | 9.97 ms                                                                | 9.86 ms: 1.01x faster                                                            |
| deepcopy                | 335 us                                                                 | 331 us: 1.01x faster                                                             |
| telco                   | 6.56 ms                                                                | 6.50 ms: 1.01x faster                                                            |
| pidigits                | 190 ms                                                                 | 188 ms: 1.01x faster                                                             |
| deltablue               | 3.24 ms                                                                | 3.21 ms: 1.01x faster                                                            |
| json_dumps              | 9.48 ms                                                                | 9.41 ms: 1.01x faster                                                            |
| unpickle_pure_python    | 202 us                                                                 | 200 us: 1.01x faster                                                             |
| 2to3                    | 252 ms                                                                 | 251 ms: 1.01x faster                                                             |
| django_template         | 32.9 ms                                                                | 32.7 ms: 1.01x faster                                                            |
| sympy_integrate         | 20.7 ms                                                                | 20.6 ms: 1.01x faster                                                            |
| mypy2                   | 334 ms                                                                 | 333 ms: 1.01x faster                                                             |
| sympy_sum               | 168 ms                                                                 | 167 ms: 1.00x faster                                                             |
| docutils                | 2.56 sec                                                               | 2.55 sec: 1.00x faster                                                           |
| aiohttp                 | 1.01 ms                                                                | 1.01 ms: 1.00x faster                                                            |
| sqlglot_optimize        | 51.4 ms                                                                | 51.2 ms: 1.00x faster                                                            |
| python_startup_no_site  | 6.53 ms                                                                | 6.53 ms: 1.00x slower                                                            |
| python_startup          | 9.01 ms                                                                | 9.02 ms: 1.00x slower                                                            |
| asyncio_tcp             | 507 ms                                                                 | 509 ms: 1.00x slower                                                             |
| bench_thread_pool       | 796 us                                                                 | 800 us: 1.00x slower                                                             |
| comprehensions          | 24.0 us                                                                | 24.1 us: 1.01x slower                                                            |
| async_generators        | 419 ms                                                                 | 421 ms: 1.01x slower                                                             |
| crypto_pyaes            | 73.9 ms                                                                | 74.5 ms: 1.01x slower                                                            |
| json_loads              | 23.7 us                                                                | 23.9 us: 1.01x slower                                                            |
| pyflate                 | 405 ms                                                                 | 409 ms: 1.01x slower                                                             |
| chameleon               | 6.35 ms                                                                | 6.43 ms: 1.01x slower                                                            |
| unpickle                | 13.4 us                                                                | 13.6 us: 1.02x slower                                                            |
| pickle                  | 9.98 us                                                                | 10.1 us: 1.02x slower                                                            |
| scimark_sor             | 108 ms                                                                 | 110 ms: 1.02x slower                                                             |
| coverage                | 94.1 ms                                                                | 95.7 ms: 1.02x slower                                                            |
| scimark_lu              | 109 ms                                                                 | 111 ms: 1.02x slower                                                             |
| logging_silent          | 92.5 ns                                                                | 94.3 ns: 1.02x slower                                                            |
| generators              | 30.3 ms                                                                | 31.0 ms: 1.02x slower                                                            |
| spectral_norm           | 96.2 ms                                                                | 98.4 ms: 1.02x slower                                                            |
| thrift                  | 763 us                                                                 | 781 us: 1.02x slower                                                             |
| deepcopy_reduce         | 2.93 us                                                                | 3.01 us: 1.02x slower                                                            |
| mdp                     | 2.44 sec                                                               | 2.50 sec: 1.03x slower                                                           |
| pycparser               | 1.11 sec                                                               | 1.14 sec: 1.03x slower                                                           |
| regex_effbot            | 3.35 ms                                                                | 3.44 ms: 1.03x slower                                                            |
| pickle_dict             | 30.0 us                                                                | 30.9 us: 1.03x slower                                                            |
| pickle_list             | 4.02 us                                                                | 4.15 us: 1.03x slower                                                            |
| regex_dna               | 210 ms                                                                 | 219 ms: 1.04x slower                                                             |
| scimark_sparse_mat_mult | 4.52 ms                                                                | 4.71 ms: 1.04x slower                                                            |
| gc_traversal            | 3.54 ms                                                                | 4.07 ms: 1.15x slower                                                            |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (28): html5lib, sqlalchemy_imperative, sqlite_synth, deepcopy_memo, richards, sympy_str, sqlalchemy_declarative, dask, async_tree_none, xml_etree_iterparse, hexiom, async_tree_memoization, nbody, create_gc_cycles, json, bench_mp_pool, tornado_http, async_tree_io, regex_compile, pathlib, async_tree_cpu_io_mixed, scimark_fft, gunicorn, dulwich_log, genshi_xml, float, meteor_contest, djangocms
