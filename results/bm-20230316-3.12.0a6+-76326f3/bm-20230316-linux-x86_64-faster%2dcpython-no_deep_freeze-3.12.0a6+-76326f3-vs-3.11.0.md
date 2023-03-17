
# Results vs. 3.11.0

- fork: faster-cpython
- ref: no_deep_freeze
- machine: linux-x86_64
- commit hash: 76326f3
- commit date: 2023-03-16
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                                       |
| chameleon      | 6.41 ms                                                | 6.36 ms: 1.01x faster                                                      |
| docutils       | 2.60 sec                                               | 2.52 sec: 1.03x faster                                                     |
| html5lib       | 63.2 ms                                                | 59.2 ms: 1.07x faster                                                      |
| tornado_http   | 96.6 ms                                                | 90.9 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                  | 1.04x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 95.0 ms                                                | 88.2 ms: 1.08x faster                                                      |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                                       |
| float          | 76.3 ms                                                | 73.7 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                  | 1.06x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 133 ms: 1.03x faster                                                       |
| regex_dna      | 203 ms                                                 | 204 ms: 1.01x slower                                                       |
| regex_effbot   | 3.36 ms                                                | 3.45 ms: 1.03x slower                                                      |
| regex_v8       | 22.3 ms                                                | 25.6 ms: 1.15x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.62 ms: 1.32x faster                                                      |
| unpickle_pure_python | 225 us                                                 | 199 us: 1.13x faster                                                       |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                                      |
| pickle_pure_python   | 304 us                                                 | 282 us: 1.08x faster                                                       |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                       |
| pickle_dict          | 31.4 us                                                | 30.0 us: 1.05x faster                                                      |
| xml_etree_iterparse  | 103 ms                                                 | 99.7 ms: 1.03x faster                                                      |
| pickle_list          | 4.17 us                                                | 4.21 us: 1.01x slower                                                      |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                                      |
| xml_etree_process    | 53.8 ms                                                | 56.4 ms: 1.05x slower                                                      |
| xml_etree_generate   | 76.2 ms                                                | 81.8 ms: 1.07x slower                                                      |
| unpickle_list        | 4.95 us                                                | 5.32 us: 1.07x slower                                                      |
| unpickle             | 13.3 us                                                | 14.5 us: 1.09x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 5.96 ms                                                | 6.48 ms: 1.09x slower                                                      |
| python_startup         | 8.36 ms                                                | 9.51 ms: 1.14x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.7 ms: 1.09x faster                                                      |
| genshi_text     | 22.1 ms                                                | 21.2 ms: 1.05x faster                                                      |
| django_template | 32.5 ms                                                | 33.1 ms: 1.02x slower                                                      |
| mako            | 9.85 ms                                                | 10.2 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.9 ms: 2.41x faster                                                      |
| json_dumps              | 12.7 ms                                                | 9.62 ms: 1.32x faster                                                      |
| coroutines              | 26.1 ms                                                | 22.2 ms: 1.17x faster                                                      |
| deltablue               | 3.64 ms                                                | 3.15 ms: 1.16x faster                                                      |
| unpickle_pure_python    | 225 us                                                 | 199 us: 1.13x faster                                                       |
| spectral_norm           | 99.9 ms                                                | 90.6 ms: 1.10x faster                                                      |
| coverage                | 101 ms                                                 | 91.6 ms: 1.10x faster                                                      |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                                      |
| mdp                     | 2.62 sec                                               | 2.40 sec: 1.09x faster                                                     |
| genshi_xml              | 52.1 ms                                                | 47.7 ms: 1.09x faster                                                      |
| scimark_sor             | 115 ms                                                 | 106 ms: 1.09x faster                                                       |
| json                    | 4.95 ms                                                | 4.54 ms: 1.09x faster                                                      |
| go                      | 143 ms                                                 | 132 ms: 1.09x faster                                                       |
| richards                | 46.2 ms                                                | 42.6 ms: 1.08x faster                                                      |
| deepcopy_memo           | 36.4 us                                                | 33.7 us: 1.08x faster                                                      |
| scimark_fft             | 329 ms                                                 | 304 ms: 1.08x faster                                                       |
| nbody                   | 95.0 ms                                                | 88.2 ms: 1.08x faster                                                      |
| pickle_pure_python      | 304 us                                                 | 282 us: 1.08x faster                                                       |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                       |
| html5lib                | 63.2 ms                                                | 59.2 ms: 1.07x faster                                                      |
| logging_simple          | 6.06 us                                                | 5.69 us: 1.07x faster                                                      |
| tornado_http            | 96.6 ms                                                | 90.9 ms: 1.06x faster                                                      |
| logging_silent          | 98.5 ns                                                | 93.4 ns: 1.05x faster                                                      |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                                       |
| aiohttp                 | 1.05 ms                                                | 996 us: 1.05x faster                                                       |
| nqueens                 | 85.0 ms                                                | 81.1 ms: 1.05x faster                                                      |
| pickle_dict             | 31.4 us                                                | 30.0 us: 1.05x faster                                                      |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                                      |
| deepcopy                | 344 us                                                 | 328 us: 1.05x faster                                                       |
| genshi_text             | 22.1 ms                                                | 21.2 ms: 1.05x faster                                                      |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                                       |
| logging_format          | 6.62 us                                                | 6.34 us: 1.04x faster                                                      |
| hexiom                  | 6.35 ms                                                | 6.10 ms: 1.04x faster                                                      |
| float                   | 76.3 ms                                                | 73.7 ms: 1.04x faster                                                      |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                                     |
| async_tree_memoization  | 625 ms                                                 | 606 ms: 1.03x faster                                                       |
| docutils                | 2.60 sec                                               | 2.52 sec: 1.03x faster                                                     |
| raytrace                | 290 ms                                                 | 282 ms: 1.03x faster                                                       |
| sqlglot_optimize        | 53.0 ms                                                | 51.4 ms: 1.03x faster                                                      |
| xml_etree_iterparse     | 103 ms                                                 | 99.7 ms: 1.03x faster                                                      |
| chaos                   | 68.6 ms                                                | 66.7 ms: 1.03x faster                                                      |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.03x faster                                                       |
| dulwich_log             | 63.9 ms                                                | 62.3 ms: 1.03x faster                                                      |
| regex_compile           | 136 ms                                                 | 133 ms: 1.03x faster                                                       |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                                      |
| bench_thread_pool       | 810 us                                                 | 791 us: 1.02x faster                                                       |
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                                       |
| sqlalchemy_declarative  | 139 ms                                                 | 136 ms: 1.02x faster                                                       |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                      |
| scimark_monte_carlo     | 68.3 ms                                                | 67.0 ms: 1.02x faster                                                      |
| sympy_expand            | 472 ms                                                 | 464 ms: 1.02x faster                                                       |
| unpack_sequence         | 43.4 ns                                                | 42.8 ns: 1.01x faster                                                      |
| scimark_lu              | 107 ms                                                 | 106 ms: 1.01x faster                                                       |
| sympy_str               | 287 ms                                                 | 284 ms: 1.01x faster                                                       |
| telco                   | 6.62 ms                                                | 6.56 ms: 1.01x faster                                                      |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.37 ms: 1.01x faster                                                      |
| chameleon               | 6.41 ms                                                | 6.36 ms: 1.01x faster                                                      |
| pprint_safe_repr        | 691 ms                                                 | 687 ms: 1.00x faster                                                       |
| regex_dna               | 203 ms                                                 | 204 ms: 1.01x slower                                                       |
| crypto_pyaes            | 73.9 ms                                                | 74.4 ms: 1.01x slower                                                      |
| pickle_list             | 4.17 us                                                | 4.21 us: 1.01x slower                                                      |
| async_tree_none         | 529 ms                                                 | 535 ms: 1.01x slower                                                       |
| pyflate                 | 417 ms                                                 | 423 ms: 1.01x slower                                                       |
| django_template         | 32.5 ms                                                | 33.1 ms: 1.02x slower                                                      |
| async_tree_cpu_io_mixed | 752 ms                                                 | 770 ms: 1.02x slower                                                       |
| regex_effbot            | 3.36 ms                                                | 3.45 ms: 1.03x slower                                                      |
| thrift                  | 752 us                                                 | 772 us: 1.03x slower                                                       |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                                      |
| mako                    | 9.85 ms                                                | 10.2 ms: 1.03x slower                                                      |
| sqlglot_parse           | 1.37 ms                                                | 1.42 ms: 1.04x slower                                                      |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                                      |
| xml_etree_process       | 53.8 ms                                                | 56.4 ms: 1.05x slower                                                      |
| sqlite_synth            | 2.49 us                                                | 2.65 us: 1.06x slower                                                      |
| xml_etree_generate      | 76.2 ms                                                | 81.8 ms: 1.07x slower                                                      |
| unpickle_list           | 4.95 us                                                | 5.32 us: 1.07x slower                                                      |
| python_startup_no_site  | 5.96 ms                                                | 6.48 ms: 1.09x slower                                                      |
| unpickle                | 13.3 us                                                | 14.5 us: 1.09x slower                                                      |
| python_startup          | 8.36 ms                                                | 9.51 ms: 1.14x slower                                                      |
| async_generators        | 359 ms                                                 | 411 ms: 1.14x slower                                                       |
| regex_v8                | 22.3 ms                                                | 25.6 ms: 1.15x slower                                                      |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (6): sqlalchemy_imperative, pycparser, async_tree_io, deepcopy_reduce, bench_mp_pool, sympy_sum
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230316-3.12.0a6+-76326f3/bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
