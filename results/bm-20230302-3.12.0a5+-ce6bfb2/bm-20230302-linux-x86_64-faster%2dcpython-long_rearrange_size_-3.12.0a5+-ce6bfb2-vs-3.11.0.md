
# Results vs. 3.11.0

- fork: faster-cpython
- ref: long_rearrange_size_
- machine: linux-x86_64
- commit hash: ce6bfb2
- commit date: 2023-03-02
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 251 ms: 1.03x faster                                                             |
| docutils       | 2.60 sec                                               | 2.55 sec: 1.02x faster                                                           |
| html5lib       | 63.2 ms                                                | 61.8 ms: 1.02x faster                                                            |
| tornado_http   | 96.6 ms                                                | 95.0 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 188 ms: 1.06x faster                                                             |
| nbody          | 95.0 ms                                                | 91.6 ms: 1.04x faster                                                            |
| float          | 76.3 ms                                                | 74.6 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                | 21.5 ms: 1.04x faster                                                            |
| regex_compile  | 136 ms                                                 | 134 ms: 1.01x faster                                                             |
| regex_effbot   | 3.36 ms                                                | 3.44 ms: 1.03x slower                                                            |
| regex_dna      | 203 ms                                                 | 219 ms: 1.08x slower                                                             |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.41 ms: 1.35x faster                                                            |
| unpickle_pure_python | 225 us                                                 | 200 us: 1.13x faster                                                             |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                                            |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| pickle_pure_python   | 304 us                                                 | 285 us: 1.06x faster                                                             |
| pickle_dict          | 31.4 us                                                | 30.9 us: 1.02x faster                                                            |
| pickle_list          | 4.17 us                                                | 4.15 us: 1.01x faster                                                            |
| unpickle_list        | 4.95 us                                                | 5.00 us: 1.01x slower                                                            |
| unpickle             | 13.3 us                                                | 13.6 us: 1.03x slower                                                            |
| pickle               | 9.79 us                                                | 10.1 us: 1.04x slower                                                            |
| xml_etree_process    | 53.8 ms                                                | 55.7 ms: 1.04x slower                                                            |
| xml_etree_generate   | 76.2 ms                                                | 80.8 ms: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.02 ms: 1.08x slower                                                            |
| python_startup_no_site | 5.96 ms                                                | 6.53 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 48.2 ms: 1.08x faster                                                            |
| genshi_text     | 22.1 ms                                                | 21.2 ms: 1.04x faster                                                            |
| django_template | 32.5 ms                                                | 32.7 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 31.0 ms: 2.33x faster                                                            |
| json_dumps              | 12.7 ms                                                | 9.41 ms: 1.35x faster                                                            |
| deltablue               | 3.64 ms                                                | 3.21 ms: 1.13x faster                                                            |
| coroutines              | 26.1 ms                                                | 23.1 ms: 1.13x faster                                                            |
| unpickle_pure_python    | 225 us                                                 | 200 us: 1.13x faster                                                             |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                                            |
| json                    | 4.95 ms                                                | 4.57 ms: 1.08x faster                                                            |
| genshi_xml              | 52.1 ms                                                | 48.2 ms: 1.08x faster                                                            |
| fannkuch                | 388 ms                                                 | 360 ms: 1.08x faster                                                             |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                             |
| pickle_pure_python      | 304 us                                                 | 285 us: 1.06x faster                                                             |
| pidigits                | 199 ms                                                 | 188 ms: 1.06x faster                                                             |
| deepcopy_memo           | 36.4 us                                                | 34.4 us: 1.06x faster                                                            |
| nqueens                 | 85.0 ms                                                | 80.4 ms: 1.06x faster                                                            |
| go                      | 143 ms                                                 | 136 ms: 1.05x faster                                                             |
| richards                | 46.2 ms                                                | 43.9 ms: 1.05x faster                                                            |
| logging_format          | 6.62 us                                                | 6.30 us: 1.05x faster                                                            |
| coverage                | 101 ms                                                 | 95.7 ms: 1.05x faster                                                            |
| scimark_sor             | 115 ms                                                 | 110 ms: 1.05x faster                                                             |
| logging_simple          | 6.06 us                                                | 5.78 us: 1.05x faster                                                            |
| mdp                     | 2.62 sec                                               | 2.50 sec: 1.05x faster                                                           |
| logging_silent          | 98.5 ns                                                | 94.3 ns: 1.04x faster                                                            |
| genshi_text             | 22.1 ms                                                | 21.2 ms: 1.04x faster                                                            |
| pprint_pformat          | 1.44 sec                                               | 1.39 sec: 1.04x faster                                                           |
| regex_v8                | 22.3 ms                                                | 21.5 ms: 1.04x faster                                                            |
| deepcopy                | 344 us                                                 | 331 us: 1.04x faster                                                             |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                            |
| nbody                   | 95.0 ms                                                | 91.6 ms: 1.04x faster                                                            |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                                             |
| unpack_sequence         | 43.4 ns                                                | 41.9 ns: 1.04x faster                                                            |
| sqlglot_optimize        | 53.0 ms                                                | 51.2 ms: 1.03x faster                                                            |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                                            |
| pycparser               | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                           |
| pprint_safe_repr        | 691 ms                                                 | 672 ms: 1.03x faster                                                             |
| 2to3                    | 257 ms                                                 | 251 ms: 1.03x faster                                                             |
| sympy_expand            | 472 ms                                                 | 460 ms: 1.03x faster                                                             |
| float                   | 76.3 ms                                                | 74.6 ms: 1.02x faster                                                            |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                            |
| hexiom                  | 6.35 ms                                                | 6.21 ms: 1.02x faster                                                            |
| html5lib                | 63.2 ms                                                | 61.8 ms: 1.02x faster                                                            |
| telco                   | 6.62 ms                                                | 6.50 ms: 1.02x faster                                                            |
| pyflate                 | 417 ms                                                 | 409 ms: 1.02x faster                                                             |
| pickle_dict             | 31.4 us                                                | 30.9 us: 1.02x faster                                                            |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                                             |
| scimark_monte_carlo     | 68.3 ms                                                | 67.1 ms: 1.02x faster                                                            |
| docutils                | 2.60 sec                                               | 2.55 sec: 1.02x faster                                                           |
| tornado_http            | 96.6 ms                                                | 95.0 ms: 1.02x faster                                                            |
| scimark_fft             | 329 ms                                                 | 324 ms: 1.02x faster                                                             |
| spectral_norm           | 99.9 ms                                                | 98.4 ms: 1.02x faster                                                            |
| chaos                   | 68.6 ms                                                | 67.6 ms: 1.01x faster                                                            |
| sympy_integrate         | 20.9 ms                                                | 20.6 ms: 1.01x faster                                                            |
| bench_thread_pool       | 810 us                                                 | 800 us: 1.01x faster                                                             |
| regex_compile           | 136 ms                                                 | 134 ms: 1.01x faster                                                             |
| async_tree_cpu_io_mixed | 752 ms                                                 | 744 ms: 1.01x faster                                                             |
| pickle_list             | 4.17 us                                                | 4.15 us: 1.01x faster                                                            |
| raytrace                | 290 ms                                                 | 289 ms: 1.01x faster                                                             |
| sympy_str               | 287 ms                                                 | 286 ms: 1.00x faster                                                             |
| crypto_pyaes            | 73.9 ms                                                | 74.5 ms: 1.01x slower                                                            |
| sympy_sum               | 166 ms                                                 | 167 ms: 1.01x slower                                                             |
| django_template         | 32.5 ms                                                | 32.7 ms: 1.01x slower                                                            |
| unpickle_list           | 4.95 us                                                | 5.00 us: 1.01x slower                                                            |
| deepcopy_reduce         | 2.97 us                                                | 3.01 us: 1.01x slower                                                            |
| regex_effbot            | 3.36 ms                                                | 3.44 ms: 1.03x slower                                                            |
| unpickle                | 13.3 us                                                | 13.6 us: 1.03x slower                                                            |
| scimark_lu              | 107 ms                                                 | 111 ms: 1.03x slower                                                             |
| pickle                  | 9.79 us                                                | 10.1 us: 1.04x slower                                                            |
| xml_etree_process       | 53.8 ms                                                | 55.7 ms: 1.04x slower                                                            |
| thrift                  | 752 us                                                 | 781 us: 1.04x slower                                                             |
| sqlglot_transpile       | 1.66 ms                                                | 1.73 ms: 1.04x slower                                                            |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.05x slower                                                            |
| sqlite_synth            | 2.49 us                                                | 2.62 us: 1.05x slower                                                            |
| async_tree_memoization  | 625 ms                                                 | 661 ms: 1.06x slower                                                             |
| xml_etree_generate      | 76.2 ms                                                | 80.8 ms: 1.06x slower                                                            |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.71 ms: 1.07x slower                                                            |
| regex_dna               | 203 ms                                                 | 219 ms: 1.08x slower                                                             |
| python_startup          | 8.36 ms                                                | 9.02 ms: 1.08x slower                                                            |
| python_startup_no_site  | 5.96 ms                                                | 6.53 ms: 1.10x slower                                                            |
| async_generators        | 359 ms                                                 | 421 ms: 1.17x slower                                                             |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (9): async_tree_none, async_tree_io, sqlalchemy_imperative, sqlalchemy_declarative, bench_mp_pool, dulwich_log, xml_etree_iterparse, mako, chameleon
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230302-3.12.0a5+-ce6bfb2/bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
