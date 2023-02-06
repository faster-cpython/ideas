
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a2b984
- commit date: 2023-02-04
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 253 ms: 1.02x faster                                   |
| chameleon      | 6.41 ms                                                | 6.29 ms: 1.02x faster                                  |
| docutils       | 2.60 sec                                               | 2.51 sec: 1.04x faster                                 |
| html5lib       | 63.2 ms                                                | 60.0 ms: 1.05x faster                                  |
| tornado_http   | 96.6 ms                                                | 94.1 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 189 ms: 1.06x faster                                   |
| float          | 76.3 ms                                                | 72.8 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 93.8 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_v8       | 22.3 ms                                                | 22.4 ms: 1.00x slower                                  |
| regex_dna      | 203 ms                                                 | 216 ms: 1.06x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.64 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.26 ms: 1.37x faster                                  |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                   |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| xml_etree_parse      | 158 ms                                                 | 146 ms: 1.08x faster                                   |
| pickle_pure_python   | 304 us                                                 | 283 us: 1.08x faster                                   |
| pickle_list          | 4.17 us                                                | 4.05 us: 1.03x faster                                  |
| pickle_dict          | 31.4 us                                                | 30.8 us: 1.02x faster                                  |
| xml_etree_process    | 53.8 ms                                                | 53.2 ms: 1.01x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 77.3 ms: 1.01x slower                                  |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| Geometric mean       | (ref)                                                  | 1.06x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.93 ms: 1.07x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.46 ms: 1.08x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.11x faster                                  |
| genshi_text     | 22.1 ms                                                | 20.6 ms: 1.07x faster                                  |
| mako            | 9.85 ms                                                | 9.70 ms: 1.02x faster                                  |
| django_template | 32.5 ms                                                | 32.8 ms: 1.01x slower                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.26 ms: 1.37x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                   |
| deltablue               | 3.64 ms                                                | 3.22 ms: 1.13x faster                                  |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.11x faster                                  |
| scimark_fft             | 329 ms                                                 | 299 ms: 1.10x faster                                   |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| spectral_norm           | 99.9 ms                                                | 91.5 ms: 1.09x faster                                  |
| json                    | 4.95 ms                                                | 4.57 ms: 1.08x faster                                  |
| xml_etree_parse         | 158 ms                                                 | 146 ms: 1.08x faster                                   |
| nqueens                 | 85.0 ms                                                | 78.8 ms: 1.08x faster                                  |
| pickle_pure_python      | 304 us                                                 | 283 us: 1.08x faster                                   |
| genshi_text             | 22.1 ms                                                | 20.6 ms: 1.07x faster                                  |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.07x faster                                   |
| richards                | 46.2 ms                                                | 43.2 ms: 1.07x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.1 us: 1.07x faster                                  |
| sympy_sum               | 166 ms                                                 | 156 ms: 1.07x faster                                   |
| logging_simple          | 6.06 us                                                | 5.70 us: 1.06x faster                                  |
| regex_compile           | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| logging_silent          | 98.5 ns                                                | 92.8 ns: 1.06x faster                                  |
| chaos                   | 68.6 ms                                                | 64.7 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 136 ms: 1.06x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.01 ms: 1.06x faster                                  |
| sympy_str               | 287 ms                                                 | 272 ms: 1.06x faster                                   |
| fannkuch                | 388 ms                                                 | 368 ms: 1.06x faster                                   |
| pidigits                | 199 ms                                                 | 189 ms: 1.06x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.06x faster                                 |
| sympy_integrate         | 20.9 ms                                                | 19.8 ms: 1.05x faster                                  |
| logging_format          | 6.62 us                                                | 6.28 us: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 60.0 ms: 1.05x faster                                  |
| deepcopy                | 344 us                                                 | 327 us: 1.05x faster                                   |
| float                   | 76.3 ms                                                | 72.8 ms: 1.05x faster                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.20 ms: 1.05x faster                                  |
| coroutines              | 26.1 ms                                                | 24.9 ms: 1.05x faster                                  |
| aiohttp                 | 1.05 ms                                                | 999 us: 1.05x faster                                   |
| sqlglot_optimize        | 53.0 ms                                                | 50.7 ms: 1.04x faster                                  |
| coverage                | 101 ms                                                 | 96.2 ms: 1.04x faster                                  |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                  |
| telco                   | 6.62 ms                                                | 6.35 ms: 1.04x faster                                  |
| docutils                | 2.60 sec                                               | 2.51 sec: 1.04x faster                                 |
| mdp                     | 2.62 sec                                               | 2.53 sec: 1.04x faster                                 |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.03x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 668 ms: 1.03x faster                                   |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                   |
| pickle_list             | 4.17 us                                                | 4.05 us: 1.03x faster                                  |
| bench_thread_pool       | 810 us                                                 | 785 us: 1.03x faster                                   |
| pyflate                 | 417 ms                                                 | 405 ms: 1.03x faster                                   |
| async_generators        | 359 ms                                                 | 349 ms: 1.03x faster                                   |
| pycparser               | 1.17 sec                                               | 1.14 sec: 1.03x faster                                 |
| tornado_http            | 96.6 ms                                                | 94.1 ms: 1.03x faster                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 66.8 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.3 ms: 1.02x faster                                  |
| pickle_dict             | 31.4 us                                                | 30.8 us: 1.02x faster                                  |
| chameleon               | 6.41 ms                                                | 6.29 ms: 1.02x faster                                  |
| 2to3                    | 257 ms                                                 | 253 ms: 1.02x faster                                   |
| unpack_sequence         | 43.4 ns                                                | 42.7 ns: 1.02x faster                                  |
| mako                    | 9.85 ms                                                | 9.70 ms: 1.02x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.02x faster                                  |
| nbody                   | 95.0 ms                                                | 93.8 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                                | 53.2 ms: 1.01x faster                                  |
| dulwich_log             | 63.9 ms                                                | 63.2 ms: 1.01x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| async_tree_none         | 529 ms                                                 | 524 ms: 1.01x faster                                   |
| regex_v8                | 22.3 ms                                                | 22.4 ms: 1.00x slower                                  |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| django_template         | 32.5 ms                                                | 32.8 ms: 1.01x slower                                  |
| unpickle_list           | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 77.3 ms: 1.01x slower                                  |
| meteor_contest          | 105 ms                                                 | 107 ms: 1.02x slower                                   |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.42 ms: 1.04x slower                                  |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                  |
| async_tree_memoization  | 625 ms                                                 | 655 ms: 1.05x slower                                   |
| generators              | 72.2 ms                                                | 76.8 ms: 1.06x slower                                  |
| regex_dna               | 203 ms                                                 | 216 ms: 1.06x slower                                   |
| python_startup          | 8.36 ms                                                | 8.93 ms: 1.07x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.46 ms: 1.08x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.64 ms: 1.09x slower                                  |
| mypy                    | 669 ms                                                 | 808 ms: 1.21x slower                                   |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (7): unpickle, raytrace, thrift, scimark_lu, bench_mp_pool, deepcopy_reduce, async_tree_cpu_io_mixed
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230204-3.12.0a4+-5a2b984/bm-20230204-linux-x86_64-python-main-3.12.0a4+-5a2b984.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
