
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c1c5882
- commit date: 2023-01-21
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 254 ms: 1.01x faster                                   |
| chameleon      | 6.41 ms                                                | 6.32 ms: 1.01x faster                                  |
| docutils       | 2.60 sec                                               | 2.51 sec: 1.04x faster                                 |
| html5lib       | 63.2 ms                                                | 60.8 ms: 1.04x faster                                  |
| tornado_http   | 96.6 ms                                                | 93.9 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.0 ms: 1.06x faster                                  |
| nbody          | 95.0 ms                                                | 92.7 ms: 1.02x faster                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.04x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna      | 203 ms                                                 | 210 ms: 1.03x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.65 ms: 1.09x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.5 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.39 ms: 1.35x faster                                  |
| json_loads           | 26.2 us                                                | 24.1 us: 1.09x faster                                  |
| pickle               | 9.79 us                                                | 10.0 us: 1.02x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.3 us: 1.04x faster                                  |
| pickle_list          | 4.17 us                                                | 4.01 us: 1.04x faster                                  |
| pickle_pure_python   | 304 us                                                 | 283 us: 1.07x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 106 ms: 1.04x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 78.1 ms: 1.02x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 54.1 ms: 1.01x slower                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.95 ms: 1.07x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.49 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text    | 22.1 ms                                                | 21.1 ms: 1.05x faster                                  |
| genshi_xml     | 52.1 ms                                                | 47.3 ms: 1.10x faster                                  |
| mako           | 9.85 ms                                                | 9.90 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 254 ms: 1.01x faster                                   |
| aiohttp                 | 1.05 ms                                                | 996 us: 1.05x faster                                   |
| async_generators        | 359 ms                                                 | 347 ms: 1.03x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 645 ms: 1.03x slower                                   |
| chameleon               | 6.41 ms                                                | 6.32 ms: 1.01x faster                                  |
| chaos                   | 68.6 ms                                                | 62.4 ms: 1.10x faster                                  |
| bench_thread_pool       | 810 us                                                 | 781 us: 1.04x faster                                   |
| coroutines              | 26.1 ms                                                | 24.6 ms: 1.06x faster                                  |
| coverage                | 101 ms                                                 | 96.0 ms: 1.05x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.8 ms: 1.01x faster                                  |
| deepcopy                | 344 us                                                 | 325 us: 1.06x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.91 us: 1.02x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 33.9 us: 1.07x faster                                  |
| deltablue               | 3.64 ms                                                | 3.19 ms: 1.14x faster                                  |
| docutils                | 2.60 sec                                               | 2.51 sec: 1.04x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.5 ms: 1.02x faster                                  |
| fannkuch                | 388 ms                                                 | 364 ms: 1.07x faster                                   |
| float                   | 76.3 ms                                                | 72.0 ms: 1.06x faster                                  |
| generators              | 72.2 ms                                                | 76.6 ms: 1.06x slower                                  |
| genshi_text             | 22.1 ms                                                | 21.1 ms: 1.05x faster                                  |
| genshi_xml              | 52.1 ms                                                | 47.3 ms: 1.10x faster                                  |
| go                      | 143 ms                                                 | 136 ms: 1.05x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 5.88 ms: 1.08x faster                                  |
| html5lib                | 63.2 ms                                                | 60.8 ms: 1.04x faster                                  |
| json                    | 4.95 ms                                                | 4.73 ms: 1.05x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.39 ms: 1.35x faster                                  |
| json_loads              | 26.2 us                                                | 24.1 us: 1.09x faster                                  |
| logging_format          | 6.62 us                                                | 6.34 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 92.0 ns: 1.07x faster                                  |
| logging_simple          | 6.06 us                                                | 5.84 us: 1.04x faster                                  |
| mako                    | 9.85 ms                                                | 9.90 ms: 1.01x slower                                  |
| mdp                     | 2.62 sec                                               | 2.46 sec: 1.07x faster                                 |
| mypy                    | 669 ms                                                 | 809 ms: 1.21x slower                                   |
| nbody                   | 95.0 ms                                                | 92.7 ms: 1.02x faster                                  |
| nqueens                 | 85.0 ms                                                | 76.0 ms: 1.12x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.0 us: 1.02x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.3 us: 1.04x faster                                  |
| pickle_list             | 4.17 us                                                | 4.01 us: 1.04x faster                                  |
| pickle_pure_python      | 304 us                                                 | 283 us: 1.07x faster                                   |
| pidigits                | 199 ms                                                 | 193 ms: 1.04x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 665 ms: 1.04x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.15 sec: 1.02x faster                                 |
| pyflate                 | 417 ms                                                 | 398 ms: 1.05x faster                                   |
| python_startup          | 8.36 ms                                                | 8.95 ms: 1.07x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.49 ms: 1.09x slower                                  |
| raytrace                | 290 ms                                                 | 283 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                   |
| regex_dna               | 203 ms                                                 | 210 ms: 1.03x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.65 ms: 1.09x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.5 ms: 1.01x slower                                  |
| richards                | 46.2 ms                                                | 42.9 ms: 1.08x faster                                  |
| scimark_fft             | 329 ms                                                 | 302 ms: 1.09x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.5 ms: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 105 ms: 1.09x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.97 ms: 1.11x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.8 ms: 1.04x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.40 ms: 1.02x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.70 ms: 1.02x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.6 ms: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.56 us: 1.03x slower                                  |
| sympy_expand            | 472 ms                                                 | 452 ms: 1.05x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.2 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 163 ms: 1.02x faster                                   |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.39 ms: 1.04x faster                                  |
| thrift                  | 752 us                                                 | 744 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 93.9 ms: 1.03x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 41.7 ns: 1.04x faster                                  |
| unpickle_list           | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 106 ms: 1.04x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 78.1 ms: 1.02x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 54.1 ms: 1.01x slower                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (8): async_tree_none, async_tree_cpu_io_mixed, bench_mp_pool, django_template, meteor_contest, scimark_lu, unpickle, xml_etree_parse
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230121-3.12.0a4+-c1c5882/bm-20230121-linux-x86_64-python-main-3.12.0a4+-c1c5882.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
