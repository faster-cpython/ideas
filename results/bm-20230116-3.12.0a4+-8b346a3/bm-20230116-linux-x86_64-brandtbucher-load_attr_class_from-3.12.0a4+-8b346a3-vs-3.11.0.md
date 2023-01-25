
# Results vs. 3.11.0

- fork: brandtbucher
- ref: load_attr_class_from
- machine: linux-x86_64
- commit hash: 8b346a3
- commit date: 2023-01-16
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                                         |
| chameleon      | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                        |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                       |
| html5lib       | 63.2 ms                                                | 60.1 ms: 1.05x faster                                                        |
| tornado_http   | 96.6 ms                                                | 94.4 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.8 ms: 1.06x faster                                                        |
| nbody          | 95.0 ms                                                | 93.6 ms: 1.02x faster                                                        |
| pidigits       | 199 ms                                                 | 193 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                                         |
| regex_dna      | 203 ms                                                 | 210 ms: 1.03x slower                                                         |
| regex_effbot   | 3.36 ms                                                | 3.47 ms: 1.03x slower                                                        |
| regex_v8       | 22.3 ms                                                | 22.4 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.28 ms: 1.36x faster                                                        |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                                        |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                                        |
| pickle_dict          | 31.4 us                                                | 30.5 us: 1.03x faster                                                        |
| pickle_list          | 4.17 us                                                | 4.10 us: 1.02x faster                                                        |
| pickle_pure_python   | 304 us                                                 | 272 us: 1.12x faster                                                         |
| unpickle_list        | 4.95 us                                                | 5.03 us: 1.02x slower                                                        |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                                         |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.08x faster                                                         |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                                         |
| xml_etree_generate   | 76.2 ms                                                | 78.4 ms: 1.03x slower                                                        |
| xml_etree_process    | 53.8 ms                                                | 54.1 ms: 1.01x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                                 |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.93 ms: 1.07x slower                                                        |
| python_startup_no_site | 5.96 ms                                                | 6.46 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.3 ms: 1.01x faster                                                        |
| genshi_text     | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                        |
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.11x faster                                                        |
| mako            | 9.85 ms                                                | 9.58 ms: 1.03x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                                         |
| aiohttp                 | 1.05 ms                                                | 994 us: 1.05x faster                                                         |
| async_generators        | 359 ms                                                 | 349 ms: 1.03x faster                                                         |
| async_tree_none         | 529 ms                                                 | 524 ms: 1.01x faster                                                         |
| async_tree_cpu_io_mixed | 752 ms                                                 | 756 ms: 1.01x slower                                                         |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                                       |
| chameleon               | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                        |
| chaos                   | 68.6 ms                                                | 64.8 ms: 1.06x faster                                                        |
| bench_thread_pool       | 810 us                                                 | 774 us: 1.05x faster                                                         |
| coroutines              | 26.1 ms                                                | 25.3 ms: 1.03x faster                                                        |
| coverage                | 101 ms                                                 | 96.0 ms: 1.05x faster                                                        |
| crypto_pyaes            | 73.9 ms                                                | 67.2 ms: 1.10x faster                                                        |
| deepcopy                | 344 us                                                 | 326 us: 1.05x faster                                                         |
| deepcopy_memo           | 36.4 us                                                | 34.0 us: 1.07x faster                                                        |
| deltablue               | 3.64 ms                                                | 3.21 ms: 1.14x faster                                                        |
| django_template         | 32.5 ms                                                | 32.3 ms: 1.01x faster                                                        |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                       |
| dulwich_log             | 63.9 ms                                                | 62.5 ms: 1.02x faster                                                        |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                                         |
| float                   | 76.3 ms                                                | 71.8 ms: 1.06x faster                                                        |
| generators              | 72.2 ms                                                | 77.2 ms: 1.07x slower                                                        |
| genshi_text             | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                        |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.11x faster                                                        |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                                         |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                                        |
| hexiom                  | 6.35 ms                                                | 5.98 ms: 1.06x faster                                                        |
| html5lib                | 63.2 ms                                                | 60.1 ms: 1.05x faster                                                        |
| json                    | 4.95 ms                                                | 4.57 ms: 1.08x faster                                                        |
| json_dumps              | 12.7 ms                                                | 9.28 ms: 1.36x faster                                                        |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                                        |
| logging_format          | 6.62 us                                                | 6.31 us: 1.05x faster                                                        |
| logging_silent          | 98.5 ns                                                | 93.6 ns: 1.05x faster                                                        |
| logging_simple          | 6.06 us                                                | 5.69 us: 1.07x faster                                                        |
| mako                    | 9.85 ms                                                | 9.58 ms: 1.03x faster                                                        |
| mdp                     | 2.62 sec                                               | 2.46 sec: 1.07x faster                                                       |
| mypy                    | 669 ms                                                 | 806 ms: 1.21x slower                                                         |
| nbody                   | 95.0 ms                                                | 93.6 ms: 1.02x faster                                                        |
| nqueens                 | 85.0 ms                                                | 78.0 ms: 1.09x faster                                                        |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.02x faster                                                        |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                                        |
| pickle_dict             | 31.4 us                                                | 30.5 us: 1.03x faster                                                        |
| pickle_list             | 4.17 us                                                | 4.10 us: 1.02x faster                                                        |
| pickle_pure_python      | 304 us                                                 | 272 us: 1.12x faster                                                         |
| pidigits                | 199 ms                                                 | 193 ms: 1.03x faster                                                         |
| pprint_safe_repr        | 691 ms                                                 | 679 ms: 1.02x faster                                                         |
| pprint_pformat          | 1.44 sec                                               | 1.39 sec: 1.04x faster                                                       |
| pycparser               | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                       |
| pyflate                 | 417 ms                                                 | 403 ms: 1.03x faster                                                         |
| python_startup          | 8.36 ms                                                | 8.93 ms: 1.07x slower                                                        |
| python_startup_no_site  | 5.96 ms                                                | 6.46 ms: 1.08x slower                                                        |
| raytrace                | 290 ms                                                 | 283 ms: 1.02x faster                                                         |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                                         |
| regex_dna               | 203 ms                                                 | 210 ms: 1.03x slower                                                         |
| regex_effbot            | 3.36 ms                                                | 3.47 ms: 1.03x slower                                                        |
| regex_v8                | 22.3 ms                                                | 22.4 ms: 1.01x slower                                                        |
| richards                | 46.2 ms                                                | 42.3 ms: 1.09x faster                                                        |
| scimark_fft             | 329 ms                                                 | 300 ms: 1.10x faster                                                         |
| scimark_lu              | 107 ms                                                 | 106 ms: 1.02x faster                                                         |
| scimark_monte_carlo     | 68.3 ms                                                | 62.1 ms: 1.10x faster                                                        |
| scimark_sor             | 115 ms                                                 | 105 ms: 1.10x faster                                                         |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.97 ms: 1.11x faster                                                        |
| spectral_norm           | 99.9 ms                                                | 95.9 ms: 1.04x faster                                                        |
| sqlglot_parse           | 1.37 ms                                                | 1.42 ms: 1.03x slower                                                        |
| sqlglot_transpile       | 1.66 ms                                                | 1.70 ms: 1.03x slower                                                        |
| sqlglot_optimize        | 53.0 ms                                                | 50.9 ms: 1.04x faster                                                        |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                                         |
| sqlite_synth            | 2.49 us                                                | 2.57 us: 1.03x slower                                                        |
| sympy_expand            | 472 ms                                                 | 456 ms: 1.03x faster                                                         |
| sympy_integrate         | 20.9 ms                                                | 19.8 ms: 1.05x faster                                                        |
| sympy_sum               | 166 ms                                                 | 156 ms: 1.06x faster                                                         |
| sympy_str               | 287 ms                                                 | 269 ms: 1.07x faster                                                         |
| telco                   | 6.62 ms                                                | 6.50 ms: 1.02x faster                                                        |
| thrift                  | 752 us                                                 | 745 us: 1.01x faster                                                         |
| tornado_http            | 96.6 ms                                                | 94.4 ms: 1.02x faster                                                        |
| unpack_sequence         | 43.4 ns                                                | 41.6 ns: 1.04x faster                                                        |
| unpickle_list           | 4.95 us                                                | 5.03 us: 1.02x slower                                                        |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                                         |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.08x faster                                                         |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                                         |
| xml_etree_generate      | 76.2 ms                                                | 78.4 ms: 1.03x slower                                                        |
| xml_etree_process       | 53.8 ms                                                | 54.1 ms: 1.01x slower                                                        |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                                 |

Benchmark hidden because not significant (5): async_tree_memoization, bench_mp_pool, deepcopy_reduce, meteor_contest, unpickle
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230116-3.12.0a4+-8b346a3/bm-20230116-linux-x86_64-brandtbucher-load_attr_class_from-3.12.0a4+-8b346a3.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
