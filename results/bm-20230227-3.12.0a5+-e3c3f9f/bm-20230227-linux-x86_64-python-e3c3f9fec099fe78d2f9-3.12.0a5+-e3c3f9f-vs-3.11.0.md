
# Results vs. 3.11.0

- fork: python
- ref: e3c3f9fec099fe78d2f9
- machine: linux-x86_64
- commit hash: e3c3f9f
- commit date: 2023-02-27
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 247 ms: 1.04x faster                                                   |
| chameleon      | 6.41 ms                                                | 6.37 ms: 1.01x faster                                                  |
| docutils       | 2.60 sec                                               | 2.55 sec: 1.02x faster                                                 |
| html5lib       | 63.2 ms                                                | 61.3 ms: 1.03x faster                                                  |
| tornado_http   | 96.6 ms                                                | 94.2 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.5 ms: 1.05x faster                                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.03x faster                                                   |
| nbody          | 95.0 ms                                                | 96.0 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 131 ms: 1.04x faster                                                   |
| regex_v8       | 22.3 ms                                                | 21.7 ms: 1.03x faster                                                  |
| regex_dna      | 203 ms                                                 | 198 ms: 1.03x faster                                                   |
| regex_effbot   | 3.36 ms                                                | 3.63 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.52 ms: 1.33x faster                                                  |
| unpickle_pure_python | 225 us                                                 | 195 us: 1.15x faster                                                   |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                                  |
| pickle_pure_python   | 304 us                                                 | 280 us: 1.08x faster                                                   |
| xml_etree_parse      | 158 ms                                                 | 150 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 103 ms                                                 | 99.8 ms: 1.03x faster                                                  |
| xml_etree_process    | 53.8 ms                                                | 55.1 ms: 1.02x slower                                                  |
| unpickle_list        | 4.95 us                                                | 5.08 us: 1.03x slower                                                  |
| pickle_dict          | 31.4 us                                                | 32.5 us: 1.03x slower                                                  |
| pickle_list          | 4.17 us                                                | 4.33 us: 1.04x slower                                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.6 ms: 1.06x slower                                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.95 ms: 1.07x slower                                                  |
| python_startup_no_site | 5.96 ms                                                | 6.49 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 52.1 ms                                                | 47.0 ms: 1.11x faster                                                  |
| genshi_text    | 22.1 ms                                                | 20.9 ms: 1.06x faster                                                  |
| mako           | 9.85 ms                                                | 9.99 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.9 ms: 2.41x faster                                                  |
| json_dumps              | 12.7 ms                                                | 9.52 ms: 1.33x faster                                                  |
| deltablue               | 3.64 ms                                                | 3.11 ms: 1.17x faster                                                  |
| unpickle_pure_python    | 225 us                                                 | 195 us: 1.15x faster                                                   |
| richards                | 46.2 ms                                                | 41.0 ms: 1.13x faster                                                  |
| genshi_xml              | 52.1 ms                                                | 47.0 ms: 1.11x faster                                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.10x faster                                                   |
| fannkuch                | 388 ms                                                 | 352 ms: 1.10x faster                                                   |
| coroutines              | 26.1 ms                                                | 23.7 ms: 1.10x faster                                                  |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                                  |
| json                    | 4.95 ms                                                | 4.53 ms: 1.09x faster                                                  |
| pickle_pure_python      | 304 us                                                 | 280 us: 1.08x faster                                                   |
| nqueens                 | 85.0 ms                                                | 78.4 ms: 1.08x faster                                                  |
| go                      | 143 ms                                                 | 132 ms: 1.08x faster                                                   |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.08x faster                                                 |
| logging_silent          | 98.5 ns                                                | 92.2 ns: 1.07x faster                                                  |
| spectral_norm           | 99.9 ms                                                | 94.0 ms: 1.06x faster                                                  |
| genshi_text             | 22.1 ms                                                | 20.9 ms: 1.06x faster                                                  |
| hexiom                  | 6.35 ms                                                | 6.00 ms: 1.06x faster                                                  |
| xml_etree_parse         | 158 ms                                                 | 150 ms: 1.06x faster                                                   |
| float                   | 76.3 ms                                                | 72.5 ms: 1.05x faster                                                  |
| deepcopy_memo           | 36.4 us                                                | 34.6 us: 1.05x faster                                                  |
| scimark_fft             | 329 ms                                                 | 313 ms: 1.05x faster                                                   |
| logging_simple          | 6.06 us                                                | 5.79 us: 1.05x faster                                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.8 ms: 1.04x faster                                                  |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                                  |
| coverage                | 101 ms                                                 | 96.5 ms: 1.04x faster                                                  |
| 2to3                    | 257 ms                                                 | 247 ms: 1.04x faster                                                   |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                  |
| raytrace                | 290 ms                                                 | 280 ms: 1.04x faster                                                   |
| logging_format          | 6.62 us                                                | 6.38 us: 1.04x faster                                                  |
| sympy_expand            | 472 ms                                                 | 455 ms: 1.04x faster                                                   |
| regex_compile           | 136 ms                                                 | 131 ms: 1.04x faster                                                   |
| pprint_pformat          | 1.44 sec                                               | 1.39 sec: 1.04x faster                                                 |
| pidigits                | 199 ms                                                 | 193 ms: 1.03x faster                                                   |
| deepcopy                | 344 us                                                 | 333 us: 1.03x faster                                                   |
| html5lib                | 63.2 ms                                                | 61.3 ms: 1.03x faster                                                  |
| regex_v8                | 22.3 ms                                                | 21.7 ms: 1.03x faster                                                  |
| bench_thread_pool       | 810 us                                                 | 786 us: 1.03x faster                                                   |
| pyflate                 | 417 ms                                                 | 405 ms: 1.03x faster                                                   |
| xml_etree_iterparse     | 103 ms                                                 | 99.8 ms: 1.03x faster                                                  |
| unpack_sequence         | 43.4 ns                                                | 42.2 ns: 1.03x faster                                                  |
| regex_dna               | 203 ms                                                 | 198 ms: 1.03x faster                                                   |
| tornado_http            | 96.6 ms                                                | 94.2 ms: 1.03x faster                                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.1 ms: 1.03x faster                                                  |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                                   |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                  |
| sqlalchemy_declarative  | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| docutils                | 2.60 sec                                               | 2.55 sec: 1.02x faster                                                 |
| pprint_safe_repr        | 691 ms                                                 | 680 ms: 1.02x faster                                                   |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                                  |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                                   |
| telco                   | 6.62 ms                                                | 6.53 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed | 752 ms                                                 | 743 ms: 1.01x faster                                                   |
| async_tree_none         | 529 ms                                                 | 524 ms: 1.01x faster                                                   |
| dulwich_log             | 63.9 ms                                                | 63.3 ms: 1.01x faster                                                  |
| sympy_sum               | 166 ms                                                 | 165 ms: 1.01x faster                                                   |
| chameleon               | 6.41 ms                                                | 6.37 ms: 1.01x faster                                                  |
| chaos                   | 68.6 ms                                                | 68.2 ms: 1.01x faster                                                  |
| scimark_lu              | 107 ms                                                 | 108 ms: 1.01x slower                                                   |
| nbody                   | 95.0 ms                                                | 96.0 ms: 1.01x slower                                                  |
| thrift                  | 752 us                                                 | 761 us: 1.01x slower                                                   |
| mako                    | 9.85 ms                                                | 9.99 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.48 ms: 1.02x slower                                                  |
| deepcopy_reduce         | 2.97 us                                                | 3.02 us: 1.02x slower                                                  |
| xml_etree_process       | 53.8 ms                                                | 55.1 ms: 1.02x slower                                                  |
| unpickle_list           | 4.95 us                                                | 5.08 us: 1.03x slower                                                  |
| mdp                     | 2.62 sec                                               | 2.69 sec: 1.03x slower                                                 |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.41 ms: 1.03x slower                                                  |
| pickle_dict             | 31.4 us                                                | 32.5 us: 1.03x slower                                                  |
| pickle_list             | 4.17 us                                                | 4.33 us: 1.04x slower                                                  |
| async_tree_memoization  | 625 ms                                                 | 649 ms: 1.04x slower                                                   |
| xml_etree_generate      | 76.2 ms                                                | 80.6 ms: 1.06x slower                                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.06x slower                                                  |
| sqlite_synth            | 2.49 us                                                | 2.64 us: 1.06x slower                                                  |
| python_startup          | 8.36 ms                                                | 8.95 ms: 1.07x slower                                                  |
| regex_effbot            | 3.36 ms                                                | 3.63 ms: 1.08x slower                                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.49 ms: 1.09x slower                                                  |
| async_generators        | 359 ms                                                 | 409 ms: 1.14x slower                                                   |
| Geometric mean          | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (6): async_tree_io, unpickle, sqlalchemy_imperative, bench_mp_pool, scimark_monte_carlo, django_template
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230227-3.12.0a5+-e3c3f9f/bm-20230227-linux-x86_64-python-e3c3f9fec099fe78d2f9-3.12.0a5+-e3c3f9f.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
