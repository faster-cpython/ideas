
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 666c084
- commit date: 2023-01-28
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| chameleon      | 6.41 ms                                                | 6.45 ms: 1.01x slower                                  |
| docutils       | 2.60 sec                                               | 2.48 sec: 1.05x faster                                 |
| html5lib       | 63.2 ms                                                | 60.1 ms: 1.05x faster                                  |
| tornado_http   | 96.6 ms                                                | 94.4 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.4 ms: 1.07x faster                                  |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 129 ms: 1.05x faster                                   |
| regex_dna      | 203 ms                                                 | 208 ms: 1.02x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.46 ms: 1.03x slower                                  |
| regex_v8       | 22.3 ms                                                | 21.2 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.57 ms: 1.32x faster                                  |
| json_loads           | 26.2 us                                                | 24.1 us: 1.09x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.0 us: 1.01x faster                                  |
| pickle_list          | 4.17 us                                                | 4.01 us: 1.04x faster                                  |
| pickle_pure_python   | 304 us                                                 | 284 us: 1.07x faster                                   |
| unpickle_pure_python | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.07x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 77.6 ms: 1.02x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 53.5 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (2): unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.90 ms: 1.07x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.44 ms: 1.08x slower                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.8 ms: 1.01x slower                                  |
| genshi_text     | 22.1 ms                                                | 20.6 ms: 1.07x faster                                  |
| genshi_xml      | 52.1 ms                                                | 47.1 ms: 1.10x faster                                  |
| mako            | 9.85 ms                                                | 9.70 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| aiohttp                 | 1.05 ms                                                | 998 us: 1.05x faster                                   |
| async_generators        | 359 ms                                                 | 350 ms: 1.03x faster                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 758 ms: 1.01x slower                                   |
| async_tree_memoization  | 625 ms                                                 | 656 ms: 1.05x slower                                   |
| chameleon               | 6.41 ms                                                | 6.45 ms: 1.01x slower                                  |
| chaos                   | 68.6 ms                                                | 64.8 ms: 1.06x faster                                  |
| bench_thread_pool       | 810 us                                                 | 786 us: 1.03x faster                                   |
| coroutines              | 26.1 ms                                                | 24.9 ms: 1.05x faster                                  |
| coverage                | 101 ms                                                 | 98.3 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 72.9 ms: 1.01x faster                                  |
| deepcopy                | 344 us                                                 | 327 us: 1.05x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 3.00 us: 1.01x slower                                  |
| deepcopy_memo           | 36.4 us                                                | 34.7 us: 1.05x faster                                  |
| deltablue               | 3.64 ms                                                | 3.19 ms: 1.14x faster                                  |
| django_template         | 32.5 ms                                                | 32.8 ms: 1.01x slower                                  |
| docutils                | 2.60 sec                                               | 2.48 sec: 1.05x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.9 ms: 1.02x faster                                  |
| fannkuch                | 388 ms                                                 | 361 ms: 1.08x faster                                   |
| float                   | 76.3 ms                                                | 71.4 ms: 1.07x faster                                  |
| generators              | 72.2 ms                                                | 76.5 ms: 1.06x slower                                  |
| genshi_text             | 22.1 ms                                                | 20.6 ms: 1.07x faster                                  |
| genshi_xml              | 52.1 ms                                                | 47.1 ms: 1.10x faster                                  |
| go                      | 143 ms                                                 | 140 ms: 1.02x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                  |
| hexiom                  | 6.35 ms                                                | 5.94 ms: 1.07x faster                                  |
| html5lib                | 63.2 ms                                                | 60.1 ms: 1.05x faster                                  |
| json                    | 4.95 ms                                                | 4.66 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.57 ms: 1.32x faster                                  |
| json_loads              | 26.2 us                                                | 24.1 us: 1.09x faster                                  |
| logging_format          | 6.62 us                                                | 6.35 us: 1.04x faster                                  |
| logging_silent          | 98.5 ns                                                | 92.4 ns: 1.07x faster                                  |
| logging_simple          | 6.06 us                                                | 5.79 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.70 ms: 1.01x faster                                  |
| mdp                     | 2.62 sec                                               | 2.68 sec: 1.02x slower                                 |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                   |
| mypy                    | 669 ms                                                 | 802 ms: 1.20x slower                                   |
| nqueens                 | 85.0 ms                                                | 78.1 ms: 1.09x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.6 ms: 1.03x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.0 us: 1.01x faster                                  |
| pickle_list             | 4.17 us                                                | 4.01 us: 1.04x faster                                  |
| pickle_pure_python      | 304 us                                                 | 284 us: 1.07x faster                                   |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 675 ms: 1.02x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.39 sec: 1.04x faster                                 |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.06x faster                                 |
| pyflate                 | 417 ms                                                 | 399 ms: 1.05x faster                                   |
| python_startup          | 8.36 ms                                                | 8.90 ms: 1.07x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.44 ms: 1.08x slower                                  |
| raytrace                | 290 ms                                                 | 282 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 129 ms: 1.05x faster                                   |
| regex_dna               | 203 ms                                                 | 208 ms: 1.02x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.46 ms: 1.03x slower                                  |
| regex_v8                | 22.3 ms                                                | 21.2 ms: 1.05x faster                                  |
| richards                | 46.2 ms                                                | 42.7 ms: 1.08x faster                                  |
| scimark_fft             | 329 ms                                                 | 308 ms: 1.07x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.5 ms: 1.04x faster                                  |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.15 ms: 1.06x faster                                  |
| spectral_norm           | 99.9 ms                                                | 97.9 ms: 1.02x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.41 ms: 1.03x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.70 ms: 1.03x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.0 ms: 1.04x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.02x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 19.9 ms: 1.05x faster                                  |
| sympy_sum               | 166 ms                                                 | 155 ms: 1.07x faster                                   |
| sympy_str               | 287 ms                                                 | 272 ms: 1.06x faster                                   |
| telco                   | 6.62 ms                                                | 6.45 ms: 1.03x faster                                  |
| thrift                  | 752 us                                                 | 744 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 94.4 ms: 1.02x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 41.9 ns: 1.04x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 201 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.07x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 77.6 ms: 1.02x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 53.5 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io, bench_mp_pool, nbody, scimark_lu, unpickle, unpickle_list
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230128-3.12.0a4+-666c084/bm-20230128-linux-x86_64-python-main-3.12.0a4+-666c084.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
