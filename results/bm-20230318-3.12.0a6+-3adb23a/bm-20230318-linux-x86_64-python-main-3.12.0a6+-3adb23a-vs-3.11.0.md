
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3adb23a
- commit date: 2023-03-18
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.04x faster                                   |
| chameleon      | 6.41 ms                                                | 6.35 ms: 1.01x faster                                  |
| docutils       | 2.60 sec                                               | 2.53 sec: 1.03x faster                                 |
| html5lib       | 63.2 ms                                                | 61.2 ms: 1.03x faster                                  |
| tornado_http   | 96.6 ms                                                | 91.2 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 95.0 ms                                                | 86.0 ms: 1.11x faster                                  |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| float          | 76.3 ms                                                | 73.9 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                | 21.7 ms: 1.03x faster                                  |
| regex_dna      | 203 ms                                                 | 201 ms: 1.01x faster                                   |
| regex_compile  | 136 ms                                                 | 135 ms: 1.01x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.63 ms: 1.08x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.57 ms: 1.32x faster                                  |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                   |
| json_loads           | 26.2 us                                                | 24.2 us: 1.09x faster                                  |
| pickle_pure_python   | 304 us                                                 | 284 us: 1.07x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 149 ms: 1.06x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| pickle_dict          | 31.4 us                                                | 31.3 us: 1.01x faster                                  |
| unpickle_list        | 4.95 us                                                | 5.00 us: 1.01x slower                                  |
| pickle_list          | 4.17 us                                                | 4.26 us: 1.02x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 55.2 ms: 1.03x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.4 ms: 1.05x slower                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.07x slower                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.91 ms: 1.07x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.52 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.11x faster                                  |
| genshi_text     | 22.1 ms                                                | 21.0 ms: 1.05x faster                                  |
| django_template | 32.5 ms                                                | 32.9 ms: 1.02x slower                                  |
| mako            | 9.85 ms                                                | 10.1 ms: 1.02x slower                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 72.2 ms                                                | 29.3 ms: 2.46x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.57 ms: 1.32x faster                                  |
| deltablue               | 3.64 ms                                                | 3.17 ms: 1.15x faster                                  |
| coroutines              | 26.1 ms                                                | 22.8 ms: 1.15x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                   |
| nbody                   | 95.0 ms                                                | 86.0 ms: 1.11x faster                                  |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.11x faster                                  |
| richards                | 46.2 ms                                                | 41.9 ms: 1.10x faster                                  |
| scimark_fft             | 329 ms                                                 | 300 ms: 1.10x faster                                   |
| nqueens                 | 85.0 ms                                                | 77.9 ms: 1.09x faster                                  |
| json_loads              | 26.2 us                                                | 24.2 us: 1.09x faster                                  |
| scimark_sor             | 115 ms                                                 | 106 ms: 1.08x faster                                   |
| spectral_norm           | 99.9 ms                                                | 92.7 ms: 1.08x faster                                  |
| json                    | 4.95 ms                                                | 4.62 ms: 1.07x faster                                  |
| pickle_pure_python      | 304 us                                                 | 284 us: 1.07x faster                                   |
| deepcopy_memo           | 36.4 us                                                | 34.2 us: 1.07x faster                                  |
| logging_simple          | 6.06 us                                                | 5.69 us: 1.07x faster                                  |
| deepcopy                | 344 us                                                 | 323 us: 1.06x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 149 ms: 1.06x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.15 ms: 1.06x faster                                  |
| tornado_http            | 96.6 ms                                                | 91.2 ms: 1.06x faster                                  |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| pycparser               | 1.17 sec                                               | 1.11 sec: 1.05x faster                                 |
| genshi_text             | 22.1 ms                                                | 21.0 ms: 1.05x faster                                  |
| go                      | 143 ms                                                 | 137 ms: 1.05x faster                                   |
| logging_format          | 6.62 us                                                | 6.31 us: 1.05x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.04x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.9 ms: 1.04x faster                                  |
| chaos                   | 68.6 ms                                                | 66.0 ms: 1.04x faster                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 65.7 ms: 1.04x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.11 ms: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 94.9 ns: 1.04x faster                                  |
| 2to3                    | 257 ms                                                 | 249 ms: 1.04x faster                                   |
| coverage                | 101 ms                                                 | 97.0 ms: 1.04x faster                                  |
| raytrace                | 290 ms                                                 | 280 ms: 1.04x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                  |
| float                   | 76.3 ms                                                | 73.9 ms: 1.03x faster                                  |
| bench_thread_pool       | 810 us                                                 | 785 us: 1.03x faster                                   |
| html5lib                | 63.2 ms                                                | 61.2 ms: 1.03x faster                                  |
| sympy_expand            | 472 ms                                                 | 458 ms: 1.03x faster                                   |
| fannkuch                | 388 ms                                                 | 377 ms: 1.03x faster                                   |
| telco                   | 6.62 ms                                                | 6.43 ms: 1.03x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.03x faster                                  |
| regex_v8                | 22.3 ms                                                | 21.7 ms: 1.03x faster                                  |
| docutils                | 2.60 sec                                               | 2.53 sec: 1.03x faster                                 |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.02x faster                                 |
| deepcopy_reduce         | 2.97 us                                                | 2.90 us: 1.02x faster                                  |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| sympy_str               | 287 ms                                                 | 283 ms: 1.02x faster                                   |
| sqlalchemy_declarative  | 139 ms                                                 | 137 ms: 1.02x faster                                   |
| dulwich_log             | 63.9 ms                                                | 63.0 ms: 1.01x faster                                  |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                   |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.8 ms: 1.01x faster                                  |
| async_tree_none         | 529 ms                                                 | 523 ms: 1.01x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| regex_dna               | 203 ms                                                 | 201 ms: 1.01x faster                                   |
| regex_compile           | 136 ms                                                 | 135 ms: 1.01x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.29 sec: 1.01x faster                                 |
| chameleon               | 6.41 ms                                                | 6.35 ms: 1.01x faster                                  |
| pprint_safe_repr        | 691 ms                                                 | 686 ms: 1.01x faster                                   |
| pyflate                 | 417 ms                                                 | 414 ms: 1.01x faster                                   |
| pickle_dict             | 31.4 us                                                | 31.3 us: 1.01x faster                                  |
| mdp                     | 2.62 sec                                               | 2.61 sec: 1.00x faster                                 |
| unpickle_list           | 4.95 us                                                | 5.00 us: 1.01x slower                                  |
| django_template         | 32.5 ms                                                | 32.9 ms: 1.02x slower                                  |
| scimark_lu              | 107 ms                                                 | 109 ms: 1.02x slower                                   |
| pickle_list             | 4.17 us                                                | 4.26 us: 1.02x slower                                  |
| mako                    | 9.85 ms                                                | 10.1 ms: 1.02x slower                                  |
| thrift                  | 752 us                                                 | 771 us: 1.03x slower                                   |
| xml_etree_process       | 53.8 ms                                                | 55.2 ms: 1.03x slower                                  |
| async_tree_memoization  | 625 ms                                                 | 644 ms: 1.03x slower                                   |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.04x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.62 us: 1.05x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 80.4 ms: 1.05x slower                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.07x slower                                  |
| python_startup          | 8.36 ms                                                | 8.91 ms: 1.07x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.63 ms: 1.08x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.52 ms: 1.09x slower                                  |
| async_generators        | 359 ms                                                 | 413 ms: 1.15x slower                                   |
| Geometric mean          | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, unpack_sequence, crypto_pyaes, bench_mp_pool, sympy_sum, unpickle
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230318-3.12.0a6+-3adb23a/bm-20230318-linux-x86_64-python-main-3.12.0a6+-3adb23a.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
