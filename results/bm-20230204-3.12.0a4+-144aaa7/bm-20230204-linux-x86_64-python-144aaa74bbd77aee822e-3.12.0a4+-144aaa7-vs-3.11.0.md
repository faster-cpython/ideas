
# Results vs. 3.11.0

- fork: python
- ref: 144aaa74bbd77aee822e
- machine: linux-x86_64
- commit hash: 144aaa7
- commit date: 2023-02-04
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 253 ms: 1.02x faster                                                   |
| chameleon      | 6.41 ms                                                | 6.25 ms: 1.03x faster                                                  |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                 |
| html5lib       | 63.2 ms                                                | 59.6 ms: 1.06x faster                                                  |
| tornado_http   | 96.6 ms                                                | 93.8 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.4 ms: 1.05x faster                                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.04x faster                                                   |
| nbody          | 95.0 ms                                                | 97.5 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 126 ms: 1.08x faster                                                   |
| regex_v8       | 22.3 ms                                                | 22.2 ms: 1.00x faster                                                  |
| regex_dna      | 203 ms                                                 | 210 ms: 1.03x slower                                                   |
| regex_effbot   | 3.36 ms                                                | 3.63 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.48 ms: 1.34x faster                                                  |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                                   |
| json_loads           | 26.2 us                                                | 24.1 us: 1.09x faster                                                  |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.08x faster                                                   |
| xml_etree_process    | 53.8 ms                                                | 53.5 ms: 1.01x faster                                                  |
| xml_etree_generate   | 76.2 ms                                                | 77.4 ms: 1.01x slower                                                  |
| pickle_list          | 4.17 us                                                | 4.24 us: 1.01x slower                                                  |
| pickle_dict          | 31.4 us                                                | 31.9 us: 1.02x slower                                                  |
| unpickle_list        | 4.95 us                                                | 5.12 us: 1.03x slower                                                  |
| pickle               | 9.79 us                                                | 10.1 us: 1.04x slower                                                  |
| unpickle             | 13.3 us                                                | 14.9 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.93 ms: 1.07x slower                                                  |
| python_startup_no_site | 5.96 ms                                                | 6.46 ms: 1.08x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.0 ms: 1.11x faster                                                  |
| genshi_text     | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                  |
| mako            | 9.85 ms                                                | 9.79 ms: 1.01x faster                                                  |
| django_template | 32.5 ms                                                | 32.6 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.48 ms: 1.34x faster                                                  |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                                   |
| deltablue               | 3.64 ms                                                | 3.21 ms: 1.14x faster                                                  |
| genshi_xml              | 52.1 ms                                                | 47.0 ms: 1.11x faster                                                  |
| richards                | 46.2 ms                                                | 42.3 ms: 1.09x faster                                                  |
| json_loads              | 26.2 us                                                | 24.1 us: 1.09x faster                                                  |
| nqueens                 | 85.0 ms                                                | 78.3 ms: 1.09x faster                                                  |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.08x faster                                                   |
| regex_compile           | 136 ms                                                 | 126 ms: 1.08x faster                                                   |
| genshi_text             | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                  |
| fannkuch                | 388 ms                                                 | 363 ms: 1.07x faster                                                   |
| logging_silent          | 98.5 ns                                                | 92.3 ns: 1.07x faster                                                  |
| deepcopy_memo           | 36.4 us                                                | 34.2 us: 1.07x faster                                                  |
| go                      | 143 ms                                                 | 134 ms: 1.07x faster                                                   |
| sympy_str               | 287 ms                                                 | 270 ms: 1.06x faster                                                   |
| sympy_sum               | 166 ms                                                 | 156 ms: 1.06x faster                                                   |
| coverage                | 101 ms                                                 | 94.5 ms: 1.06x faster                                                  |
| deepcopy                | 344 us                                                 | 323 us: 1.06x faster                                                   |
| logging_simple          | 6.06 us                                                | 5.71 us: 1.06x faster                                                  |
| scimark_fft             | 329 ms                                                 | 310 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.15 ms: 1.06x faster                                                  |
| html5lib                | 63.2 ms                                                | 59.6 ms: 1.06x faster                                                  |
| scimark_sor             | 115 ms                                                 | 109 ms: 1.06x faster                                                   |
| sympy_integrate         | 20.9 ms                                                | 19.7 ms: 1.06x faster                                                  |
| chaos                   | 68.6 ms                                                | 65.0 ms: 1.06x faster                                                  |
| float                   | 76.3 ms                                                | 72.4 ms: 1.05x faster                                                  |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                                 |
| logging_format          | 6.62 us                                                | 6.29 us: 1.05x faster                                                  |
| hexiom                  | 6.35 ms                                                | 6.05 ms: 1.05x faster                                                  |
| aiohttp                 | 1.05 ms                                                | 997 us: 1.05x faster                                                   |
| json                    | 4.95 ms                                                | 4.72 ms: 1.05x faster                                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.8 ms: 1.04x faster                                                  |
| unpack_sequence         | 43.4 ns                                                | 41.7 ns: 1.04x faster                                                  |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                                  |
| sympy_expand            | 472 ms                                                 | 455 ms: 1.04x faster                                                   |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                 |
| pidigits                | 199 ms                                                 | 193 ms: 1.04x faster                                                   |
| pprint_safe_repr        | 691 ms                                                 | 669 ms: 1.03x faster                                                   |
| bench_thread_pool       | 810 us                                                 | 785 us: 1.03x faster                                                   |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                                   |
| pyflate                 | 417 ms                                                 | 404 ms: 1.03x faster                                                   |
| tornado_http            | 96.6 ms                                                | 93.8 ms: 1.03x faster                                                  |
| raytrace                | 290 ms                                                 | 282 ms: 1.03x faster                                                   |
| pycparser               | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                 |
| spectral_norm           | 99.9 ms                                                | 97.2 ms: 1.03x faster                                                  |
| chameleon               | 6.41 ms                                                | 6.25 ms: 1.03x faster                                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.1 ms: 1.02x faster                                                  |
| async_generators        | 359 ms                                                 | 352 ms: 1.02x faster                                                   |
| 2to3                    | 257 ms                                                 | 253 ms: 1.02x faster                                                   |
| dulwich_log             | 63.9 ms                                                | 62.8 ms: 1.02x faster                                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 67.2 ms: 1.02x faster                                                  |
| coroutines              | 26.1 ms                                                | 25.7 ms: 1.02x faster                                                  |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                                   |
| telco                   | 6.62 ms                                                | 6.55 ms: 1.01x faster                                                  |
| pathlib                 | 18.2 ms                                                | 18.0 ms: 1.01x faster                                                  |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                                  |
| mdp                     | 2.62 sec                                               | 2.61 sec: 1.01x faster                                                 |
| mako                    | 9.85 ms                                                | 9.79 ms: 1.01x faster                                                  |
| xml_etree_process       | 53.8 ms                                                | 53.5 ms: 1.01x faster                                                  |
| regex_v8                | 22.3 ms                                                | 22.2 ms: 1.00x faster                                                  |
| django_template         | 32.5 ms                                                | 32.6 ms: 1.01x slower                                                  |
| thrift                  | 752 us                                                 | 758 us: 1.01x slower                                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                                 |
| async_tree_cpu_io_mixed | 752 ms                                                 | 760 ms: 1.01x slower                                                   |
| xml_etree_generate      | 76.2 ms                                                | 77.4 ms: 1.01x slower                                                  |
| pickle_list             | 4.17 us                                                | 4.24 us: 1.01x slower                                                  |
| pickle_dict             | 31.4 us                                                | 31.9 us: 1.02x slower                                                  |
| scimark_lu              | 107 ms                                                 | 110 ms: 1.02x slower                                                   |
| nbody                   | 95.0 ms                                                | 97.5 ms: 1.03x slower                                                  |
| regex_dna               | 203 ms                                                 | 210 ms: 1.03x slower                                                   |
| sqlglot_transpile       | 1.66 ms                                                | 1.72 ms: 1.03x slower                                                  |
| unpickle_list           | 4.95 us                                                | 5.12 us: 1.03x slower                                                  |
| pickle                  | 9.79 us                                                | 10.1 us: 1.04x slower                                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.04x slower                                                  |
| sqlite_synth            | 2.49 us                                                | 2.60 us: 1.04x slower                                                  |
| async_tree_memoization  | 625 ms                                                 | 652 ms: 1.04x slower                                                   |
| generators              | 72.2 ms                                                | 76.4 ms: 1.06x slower                                                  |
| python_startup          | 8.36 ms                                                | 8.93 ms: 1.07x slower                                                  |
| regex_effbot            | 3.36 ms                                                | 3.63 ms: 1.08x slower                                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.46 ms: 1.08x slower                                                  |
| unpickle                | 13.3 us                                                | 14.9 us: 1.12x slower                                                  |
| mypy                    | 669 ms                                                 | 805 ms: 1.20x slower                                                   |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): async_tree_none, xml_etree_iterparse, bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230204-3.12.0a4+-144aaa7/bm-20230204-linux-x86_64-python-144aaa74bbd77aee822e-3.12.0a4+-144aaa7.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
