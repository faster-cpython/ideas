
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 206f05a
- commit date: 2023-01-14
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| chameleon      | 6.41 ms                                                | 6.35 ms: 1.01x faster                                  |
| docutils       | 2.60 sec                                               | 2.48 sec: 1.04x faster                                 |
| html5lib       | 63.2 ms                                                | 59.2 ms: 1.07x faster                                  |
| tornado_http   | 96.6 ms                                                | 93.4 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.2 ms: 1.06x faster                                  |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 130 ms: 1.05x faster                                   |
| regex_dna      | 203 ms                                                 | 201 ms: 1.01x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.39 ms: 1.01x slower                                  |
| regex_v8       | 22.3 ms                                                | 21.2 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.40 ms: 1.35x faster                                  |
| json_loads           | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.5 us: 1.03x faster                                  |
| pickle_list          | 4.17 us                                                | 4.08 us: 1.02x faster                                  |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                   |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 149 ms: 1.06x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 107 ms: 1.04x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 76.6 ms: 1.00x slower                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (3): unpickle, unpickle_list, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.95 ms: 1.07x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.49 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.0 ms: 1.01x faster                                  |
| genshi_text     | 22.1 ms                                                | 20.2 ms: 1.09x faster                                  |
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.10x faster                                  |
| mako            | 9.85 ms                                                | 9.90 ms: 1.01x slower                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| aiohttp                 | 1.05 ms                                                | 998 us: 1.05x faster                                   |
| async_tree_none         | 529 ms                                                 | 524 ms: 1.01x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 732 ms: 1.03x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| chameleon               | 6.41 ms                                                | 6.35 ms: 1.01x faster                                  |
| chaos                   | 68.6 ms                                                | 67.9 ms: 1.01x faster                                  |
| bench_thread_pool       | 810 us                                                 | 779 us: 1.04x faster                                   |
| coroutines              | 26.1 ms                                                | 25.2 ms: 1.03x faster                                  |
| coverage                | 101 ms                                                 | 98.6 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.3 ms: 1.01x slower                                  |
| deepcopy                | 344 us                                                 | 331 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 33.7 us: 1.08x faster                                  |
| deltablue               | 3.64 ms                                                | 3.23 ms: 1.13x faster                                  |
| django_template         | 32.5 ms                                                | 32.0 ms: 1.01x faster                                  |
| docutils                | 2.60 sec                                               | 2.48 sec: 1.04x faster                                 |
| dulwich_log             | 63.9 ms                                                | 61.9 ms: 1.03x faster                                  |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                   |
| float                   | 76.3 ms                                                | 72.2 ms: 1.06x faster                                  |
| generators              | 72.2 ms                                                | 78.8 ms: 1.09x slower                                  |
| genshi_text             | 22.1 ms                                                | 20.2 ms: 1.09x faster                                  |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.10x faster                                  |
| go                      | 143 ms                                                 | 132 ms: 1.09x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.07 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 59.2 ms: 1.07x faster                                  |
| json                    | 4.95 ms                                                | 4.68 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.40 ms: 1.35x faster                                  |
| json_loads              | 26.2 us                                                | 24.2 us: 1.08x faster                                  |
| logging_format          | 6.62 us                                                | 6.20 us: 1.07x faster                                  |
| logging_silent          | 98.5 ns                                                | 90.6 ns: 1.09x faster                                  |
| logging_simple          | 6.06 us                                                | 5.61 us: 1.08x faster                                  |
| mako                    | 9.85 ms                                                | 9.90 ms: 1.01x slower                                  |
| mdp                     | 2.62 sec                                               | 2.69 sec: 1.02x slower                                 |
| mypy                    | 669 ms                                                 | 811 ms: 1.21x slower                                   |
| nqueens                 | 85.0 ms                                                | 80.8 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.5 us: 1.03x faster                                  |
| pickle_list             | 4.17 us                                                | 4.08 us: 1.02x faster                                  |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                   |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 670 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.08 sec: 1.08x faster                                 |
| pyflate                 | 417 ms                                                 | 398 ms: 1.05x faster                                   |
| python_startup          | 8.36 ms                                                | 8.95 ms: 1.07x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.49 ms: 1.09x slower                                  |
| raytrace                | 290 ms                                                 | 278 ms: 1.04x faster                                   |
| regex_compile           | 136 ms                                                 | 130 ms: 1.05x faster                                   |
| regex_dna               | 203 ms                                                 | 201 ms: 1.01x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.39 ms: 1.01x slower                                  |
| regex_v8                | 22.3 ms                                                | 21.2 ms: 1.05x faster                                  |
| richards                | 46.2 ms                                                | 41.1 ms: 1.12x faster                                  |
| scimark_fft             | 329 ms                                                 | 306 ms: 1.08x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 63.8 ms: 1.07x faster                                  |
| scimark_sor             | 115 ms                                                 | 106 ms: 1.08x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.05 ms: 1.09x faster                                  |
| spectral_norm           | 99.9 ms                                                | 93.9 ms: 1.06x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.39 ms: 1.01x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.67 ms: 1.01x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.5 ms: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 459 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| sympy_sum               | 166 ms                                                 | 164 ms: 1.01x faster                                   |
| sympy_str               | 287 ms                                                 | 283 ms: 1.01x faster                                   |
| telco                   | 6.62 ms                                                | 6.24 ms: 1.06x faster                                  |
| tornado_http            | 96.6 ms                                                | 93.4 ms: 1.03x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 41.3 ns: 1.05x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 149 ms: 1.06x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 107 ms: 1.04x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 76.6 ms: 1.00x slower                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (10): async_generators, async_tree_memoization, bench_mp_pool, meteor_contest, nbody, scimark_lu, thrift, unpickle, unpickle_list, xml_etree_process
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230114-3.12.0a4+-206f05a/bm-20230114-linux-x86_64-python-main-3.12.0a4+-206f05a.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
