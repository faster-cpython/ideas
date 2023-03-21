
# Results vs. 3.11.0

- fork: itamaro
- ref: eager_tasks_factory
- machine: linux-x86_64
- commit hash: bcf40dc
- commit date: 2023-03-20
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.03x faster                                                   |
| chameleon      | 6.41 ms                                                | 6.27 ms: 1.02x faster                                                  |
| docutils       | 2.60 sec                                               | 2.52 sec: 1.03x faster                                                 |
| html5lib       | 63.2 ms                                                | 60.6 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 95.0 ms                                                | 87.6 ms: 1.08x faster                                                  |
| float          | 76.3 ms                                                | 74.0 ms: 1.03x faster                                                  |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 132 ms: 1.03x faster                                                   |
| regex_effbot   | 3.36 ms                                                | 3.30 ms: 1.02x faster                                                  |
| regex_v8       | 22.3 ms                                                | 22.1 ms: 1.01x faster                                                  |
| regex_dna      | 203 ms                                                 | 204 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.51 ms: 1.33x faster                                                  |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                                   |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                                  |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                                   |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                                   |
| pickle_dict          | 31.4 us                                                | 31.3 us: 1.00x faster                                                  |
| pickle_list          | 4.17 us                                                | 4.21 us: 1.01x slower                                                  |
| xml_etree_process    | 53.8 ms                                                | 55.3 ms: 1.03x slower                                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.1 ms: 1.05x slower                                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.96 ms: 1.07x slower                                                  |
| python_startup_no_site | 5.96 ms                                                | 6.55 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.8 ms: 1.09x faster                                                  |
| genshi_text     | 22.1 ms                                                | 21.0 ms: 1.05x faster                                                  |
| mako            | 9.85 ms                                                | 9.99 ms: 1.01x slower                                                  |
| django_template | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.4 ms: 2.45x faster                                                  |
| json_dumps              | 12.7 ms                                                | 9.51 ms: 1.33x faster                                                  |
| coroutines              | 26.1 ms                                                | 22.4 ms: 1.17x faster                                                  |
| deltablue               | 3.64 ms                                                | 3.14 ms: 1.16x faster                                                  |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                                   |
| spectral_norm           | 99.9 ms                                                | 88.2 ms: 1.13x faster                                                  |
| scimark_fft             | 329 ms                                                 | 297 ms: 1.11x faster                                                   |
| richards                | 46.2 ms                                                | 42.0 ms: 1.10x faster                                                  |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                                  |
| genshi_xml              | 52.1 ms                                                | 47.8 ms: 1.09x faster                                                  |
| nqueens                 | 85.0 ms                                                | 78.2 ms: 1.09x faster                                                  |
| nbody                   | 95.0 ms                                                | 87.6 ms: 1.08x faster                                                  |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                                   |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| json                    | 4.95 ms                                                | 4.59 ms: 1.08x faster                                                  |
| deepcopy_memo           | 36.4 us                                                | 34.0 us: 1.07x faster                                                  |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                   |
| logging_simple          | 6.06 us                                                | 5.69 us: 1.07x faster                                                  |
| deepcopy                | 344 us                                                 | 323 us: 1.07x faster                                                   |
| fannkuch                | 388 ms                                                 | 365 ms: 1.06x faster                                                   |
| go                      | 143 ms                                                 | 135 ms: 1.06x faster                                                   |
| logging_format          | 6.62 us                                                | 6.23 us: 1.06x faster                                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.18 ms: 1.05x faster                                                  |
| genshi_text             | 22.1 ms                                                | 21.0 ms: 1.05x faster                                                  |
| pycparser               | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                 |
| chaos                   | 68.6 ms                                                | 65.5 ms: 1.05x faster                                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.6 ms: 1.05x faster                                                  |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.04x faster                                                   |
| hexiom                  | 6.35 ms                                                | 6.08 ms: 1.04x faster                                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 65.5 ms: 1.04x faster                                                  |
| telco                   | 6.62 ms                                                | 6.36 ms: 1.04x faster                                                  |
| html5lib                | 63.2 ms                                                | 60.6 ms: 1.04x faster                                                  |
| coverage                | 101 ms                                                 | 96.8 ms: 1.04x faster                                                  |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                  |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                                  |
| sympy_expand            | 472 ms                                                 | 455 ms: 1.04x faster                                                   |
| pyflate                 | 417 ms                                                 | 403 ms: 1.04x faster                                                   |
| bench_thread_pool       | 810 us                                                 | 783 us: 1.03x faster                                                   |
| 2to3                    | 257 ms                                                 | 249 ms: 1.03x faster                                                   |
| float                   | 76.3 ms                                                | 74.0 ms: 1.03x faster                                                  |
| docutils                | 2.60 sec                                               | 2.52 sec: 1.03x faster                                                 |
| regex_compile           | 136 ms                                                 | 132 ms: 1.03x faster                                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                                  |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                                 |
| mdp                     | 2.62 sec                                               | 2.55 sec: 1.03x faster                                                 |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.03x faster                                                  |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                                   |
| logging_silent          | 98.5 ns                                                | 96.2 ns: 1.02x faster                                                  |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.6 ms: 1.02x faster                                                  |
| sqlalchemy_declarative  | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| chameleon               | 6.41 ms                                                | 6.27 ms: 1.02x faster                                                  |
| raytrace                | 290 ms                                                 | 284 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 736 ms: 1.02x faster                                                   |
| regex_effbot            | 3.36 ms                                                | 3.30 ms: 1.02x faster                                                  |
| dulwich_log             | 63.9 ms                                                | 62.9 ms: 1.02x faster                                                  |
| async_tree_none         | 529 ms                                                 | 521 ms: 1.02x faster                                                   |
| async_tree_io           | 1.31 sec                                               | 1.29 sec: 1.01x faster                                                 |
| unpack_sequence         | 43.4 ns                                                | 42.9 ns: 1.01x faster                                                  |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                                  |
| crypto_pyaes            | 73.9 ms                                                | 73.2 ms: 1.01x faster                                                  |
| regex_v8                | 22.3 ms                                                | 22.1 ms: 1.01x faster                                                  |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                                   |
| sympy_sum               | 166 ms                                                 | 165 ms: 1.01x faster                                                   |
| pprint_safe_repr        | 691 ms                                                 | 687 ms: 1.01x faster                                                   |
| pickle_dict             | 31.4 us                                                | 31.3 us: 1.00x faster                                                  |
| regex_dna               | 203 ms                                                 | 204 ms: 1.01x slower                                                   |
| pickle_list             | 4.17 us                                                | 4.21 us: 1.01x slower                                                  |
| mako                    | 9.85 ms                                                | 9.99 ms: 1.01x slower                                                  |
| django_template         | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                  |
| xml_etree_process       | 53.8 ms                                                | 55.3 ms: 1.03x slower                                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.41 ms: 1.03x slower                                                  |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.04x slower                                                  |
| thrift                  | 752 us                                                 | 788 us: 1.05x slower                                                   |
| xml_etree_generate      | 76.2 ms                                                | 80.1 ms: 1.05x slower                                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.07x slower                                                  |
| python_startup          | 8.36 ms                                                | 8.96 ms: 1.07x slower                                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.55 ms: 1.10x slower                                                  |
| async_generators        | 359 ms                                                 | 411 ms: 1.14x slower                                                   |
| Geometric mean          | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (6): async_tree_memoization, scimark_lu, bench_mp_pool, unpickle_list, meteor_contest, unpickle
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint, tornado_http
Ignored benchmarks (7) of public/results/bm-20230320-3.12.0a6+-bcf40dc/bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6+-bcf40dc.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
