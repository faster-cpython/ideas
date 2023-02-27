
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d71edbd
- commit date: 2023-02-25
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| docutils       | 2.60 sec                                               | 2.54 sec: 1.02x faster                                 |
| html5lib       | 63.2 ms                                                | 61.1 ms: 1.03x faster                                  |
| tornado_http   | 96.6 ms                                                | 94.3 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| float          | 76.3 ms                                                | 73.9 ms: 1.03x faster                                  |
| nbody          | 95.0 ms                                                | 96.6 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 131 ms: 1.04x faster                                   |
| regex_v8       | 22.3 ms                                                | 21.6 ms: 1.03x faster                                  |
| regex_dna      | 203 ms                                                 | 208 ms: 1.02x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.65 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.45 ms: 1.34x faster                                  |
| unpickle_pure_python | 225 us                                                 | 195 us: 1.16x faster                                   |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| pickle_pure_python   | 304 us                                                 | 282 us: 1.08x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 99.3 ms: 1.03x faster                                  |
| pickle_list          | 4.17 us                                                | 4.19 us: 1.00x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.7 us: 1.01x slower                                  |
| unpickle_list        | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 55.0 ms: 1.02x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.3 ms: 1.05x slower                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.06x slower                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.01 ms: 1.08x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.54 ms: 1.10x slower                                  |
| Geometric mean         | (ref)                                                  | 1.09x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 46.3 ms: 1.12x faster                                  |
| genshi_text     | 22.1 ms                                                | 20.4 ms: 1.08x faster                                  |
| mako            | 9.85 ms                                                | 9.89 ms: 1.00x slower                                  |
| django_template | 32.5 ms                                                | 33.0 ms: 1.02x slower                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.6 ms: 2.44x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.45 ms: 1.34x faster                                  |
| deltablue               | 3.64 ms                                                | 3.14 ms: 1.16x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 195 us: 1.16x faster                                   |
| richards                | 46.2 ms                                                | 40.6 ms: 1.14x faster                                  |
| coroutines              | 26.1 ms                                                | 23.0 ms: 1.13x faster                                  |
| genshi_xml              | 52.1 ms                                                | 46.3 ms: 1.12x faster                                  |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| json                    | 4.95 ms                                                | 4.54 ms: 1.09x faster                                  |
| scimark_sor             | 115 ms                                                 | 106 ms: 1.08x faster                                   |
| genshi_text             | 22.1 ms                                                | 20.4 ms: 1.08x faster                                  |
| pickle_pure_python      | 304 us                                                 | 282 us: 1.08x faster                                   |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                   |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.07x faster                                 |
| fannkuch                | 388 ms                                                 | 364 ms: 1.07x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| nqueens                 | 85.0 ms                                                | 80.0 ms: 1.06x faster                                  |
| logging_simple          | 6.06 us                                                | 5.72 us: 1.06x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.01 ms: 1.06x faster                                  |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| deepcopy_memo           | 36.4 us                                                | 34.7 us: 1.05x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.5 ms: 1.05x faster                                  |
| logging_format          | 6.62 us                                                | 6.31 us: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.05x faster                                   |
| logging_silent          | 98.5 ns                                                | 94.4 ns: 1.04x faster                                  |
| coverage                | 101 ms                                                 | 96.5 ms: 1.04x faster                                  |
| regex_compile           | 136 ms                                                 | 131 ms: 1.04x faster                                   |
| scimark_fft             | 329 ms                                                 | 317 ms: 1.04x faster                                   |
| sympy_expand            | 472 ms                                                 | 454 ms: 1.04x faster                                   |
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| raytrace                | 290 ms                                                 | 280 ms: 1.04x faster                                   |
| spectral_norm           | 99.9 ms                                                | 96.4 ms: 1.04x faster                                  |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                  |
| deepcopy                | 344 us                                                 | 332 us: 1.03x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 66.0 ms: 1.03x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 99.3 ms: 1.03x faster                                  |
| float                   | 76.3 ms                                                | 73.9 ms: 1.03x faster                                  |
| html5lib                | 63.2 ms                                                | 61.1 ms: 1.03x faster                                  |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                  |
| regex_v8                | 22.3 ms                                                | 21.6 ms: 1.03x faster                                  |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                 |
| bench_thread_pool       | 810 us                                                 | 787 us: 1.03x faster                                   |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.03x faster                                  |
| tornado_http            | 96.6 ms                                                | 94.3 ms: 1.02x faster                                  |
| chaos                   | 68.6 ms                                                | 67.0 ms: 1.02x faster                                  |
| pyflate                 | 417 ms                                                 | 407 ms: 1.02x faster                                   |
| unpack_sequence         | 43.4 ns                                                | 42.4 ns: 1.02x faster                                  |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| docutils                | 2.60 sec                                               | 2.54 sec: 1.02x faster                                 |
| sympy_str               | 287 ms                                                 | 282 ms: 1.02x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 739 ms: 1.02x faster                                   |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.7 ms: 1.02x faster                                  |
| pprint_safe_repr        | 691 ms                                                 | 681 ms: 1.01x faster                                   |
| dulwich_log             | 63.9 ms                                                | 63.1 ms: 1.01x faster                                  |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                   |
| sqlalchemy_declarative  | 139 ms                                                 | 138 ms: 1.01x faster                                   |
| telco                   | 6.62 ms                                                | 6.57 ms: 1.01x faster                                  |
| async_tree_io           | 1.31 sec                                               | 1.30 sec: 1.01x faster                                 |
| mako                    | 9.85 ms                                                | 9.89 ms: 1.00x slower                                  |
| pickle_list             | 4.17 us                                                | 4.19 us: 1.00x slower                                  |
| deepcopy_reduce         | 2.97 us                                                | 2.99 us: 1.01x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.7 us: 1.01x slower                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.7 ms: 1.01x slower                                  |
| unpickle_list           | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| nbody                   | 95.0 ms                                                | 96.6 ms: 1.02x slower                                  |
| mdp                     | 2.62 sec                                               | 2.66 sec: 1.02x slower                                 |
| django_template         | 32.5 ms                                                | 33.0 ms: 1.02x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 55.0 ms: 1.02x slower                                  |
| regex_dna               | 203 ms                                                 | 208 ms: 1.02x slower                                   |
| async_tree_memoization  | 625 ms                                                 | 640 ms: 1.02x slower                                   |
| sqlglot_transpile       | 1.66 ms                                                | 1.70 ms: 1.03x slower                                  |
| thrift                  | 752 us                                                 | 771 us: 1.03x slower                                   |
| sqlglot_parse           | 1.37 ms                                                | 1.41 ms: 1.03x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.62 ms: 1.05x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 80.3 ms: 1.05x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.62 us: 1.05x slower                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.06x slower                                  |
| python_startup          | 8.36 ms                                                | 9.01 ms: 1.08x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.65 ms: 1.09x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.54 ms: 1.10x slower                                  |
| async_generators        | 359 ms                                                 | 420 ms: 1.17x slower                                   |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (6): async_tree_none, unpickle, chameleon, bench_mp_pool, sympy_sum, scimark_lu
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230225-3.12.0a5+-d71edbd/bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
