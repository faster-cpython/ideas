
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: eff9f43
- commit date: 2023-03-04
- overall geometric mean: 1.02x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| docutils       | 2.60 sec                                               | 2.56 sec: 1.02x faster                                 |
| html5lib       | 63.2 ms                                                | 61.4 ms: 1.03x faster                                  |
| tornado_http   | 96.6 ms                                                | 94.9 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| float          | 76.3 ms                                                | 74.6 ms: 1.02x faster                                  |
| nbody          | 95.0 ms                                                | 94.0 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                  |
| regex_compile  | 136 ms                                                 | 133 ms: 1.02x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.40 ms: 1.01x slower                                  |
| regex_dna      | 203 ms                                                 | 209 ms: 1.03x slower                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.56 ms: 1.32x faster                                  |
| unpickle_pure_python | 225 us                                                 | 199 us: 1.13x faster                                   |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| pickle_pure_python   | 304 us                                                 | 291 us: 1.04x faster                                   |
| pickle_list          | 4.17 us                                                | 4.05 us: 1.03x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_process    | 53.8 ms                                                | 55.4 ms: 1.03x slower                                  |
| unpickle             | 13.3 us                                                | 13.7 us: 1.03x slower                                  |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| unpickle_list        | 4.95 us                                                | 5.22 us: 1.05x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 81.3 ms: 1.07x slower                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.03 ms: 1.08x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.55 ms: 1.10x slower                                  |
| Geometric mean         | (ref)                                                  | 1.09x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 48.6 ms: 1.07x faster                                  |
| genshi_text     | 22.1 ms                                                | 21.2 ms: 1.04x faster                                  |
| mako            | 9.85 ms                                                | 10.1 ms: 1.02x slower                                  |
| django_template | 32.5 ms                                                | 33.2 ms: 1.02x slower                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 72.2 ms                                                | 30.6 ms: 2.36x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.56 ms: 1.32x faster                                  |
| deltablue               | 3.64 ms                                                | 3.20 ms: 1.14x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 199 us: 1.13x faster                                   |
| coroutines              | 26.1 ms                                                | 23.5 ms: 1.11x faster                                  |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                  |
| richards                | 46.2 ms                                                | 42.6 ms: 1.08x faster                                  |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                   |
| json                    | 4.95 ms                                                | 4.59 ms: 1.08x faster                                  |
| genshi_xml              | 52.1 ms                                                | 48.6 ms: 1.07x faster                                  |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.06x faster                                 |
| deepcopy_memo           | 36.4 us                                                | 34.4 us: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 109 ms: 1.06x faster                                   |
| logging_silent          | 98.5 ns                                                | 93.2 ns: 1.06x faster                                  |
| mdp                     | 2.62 sec                                               | 2.49 sec: 1.05x faster                                 |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| fannkuch                | 388 ms                                                 | 371 ms: 1.05x faster                                   |
| pickle_pure_python      | 304 us                                                 | 291 us: 1.04x faster                                   |
| deepcopy                | 344 us                                                 | 329 us: 1.04x faster                                   |
| genshi_text             | 22.1 ms                                                | 21.2 ms: 1.04x faster                                  |
| logging_simple          | 6.06 us                                                | 5.83 us: 1.04x faster                                  |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                  |
| nqueens                 | 85.0 ms                                                | 82.2 ms: 1.03x faster                                  |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.03x faster                                   |
| sqlglot_optimize        | 53.0 ms                                                | 51.3 ms: 1.03x faster                                  |
| pickle_list             | 4.17 us                                                | 4.05 us: 1.03x faster                                  |
| html5lib                | 63.2 ms                                                | 61.4 ms: 1.03x faster                                  |
| 2to3                    | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.18 ms: 1.03x faster                                  |
| spectral_norm           | 99.9 ms                                                | 97.3 ms: 1.03x faster                                  |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.03x faster                                 |
| coverage                | 101 ms                                                 | 98.3 ms: 1.02x faster                                  |
| float                   | 76.3 ms                                                | 74.6 ms: 1.02x faster                                  |
| scimark_fft             | 329 ms                                                 | 322 ms: 1.02x faster                                   |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                  |
| logging_format          | 6.62 us                                                | 6.48 us: 1.02x faster                                  |
| regex_compile           | 136 ms                                                 | 133 ms: 1.02x faster                                   |
| bench_thread_pool       | 810 us                                                 | 794 us: 1.02x faster                                   |
| tornado_http            | 96.6 ms                                                | 94.9 ms: 1.02x faster                                  |
| docutils                | 2.60 sec                                               | 2.56 sec: 1.02x faster                                 |
| async_tree_none         | 529 ms                                                 | 522 ms: 1.01x faster                                   |
| sympy_expand            | 472 ms                                                 | 466 ms: 1.01x faster                                   |
| nbody                   | 95.0 ms                                                | 94.0 ms: 1.01x faster                                  |
| dulwich_log             | 63.9 ms                                                | 63.2 ms: 1.01x faster                                  |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                  |
| async_tree_cpu_io_mixed | 752 ms                                                 | 745 ms: 1.01x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.30 sec: 1.01x faster                                 |
| sympy_integrate         | 20.9 ms                                                | 20.7 ms: 1.01x faster                                  |
| pathlib                 | 18.2 ms                                                | 18.0 ms: 1.01x faster                                  |
| chaos                   | 68.6 ms                                                | 68.1 ms: 1.01x faster                                  |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| meteor_contest          | 105 ms                                                 | 104 ms: 1.01x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 687 ms: 1.00x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.40 ms: 1.01x slower                                  |
| sympy_sum               | 166 ms                                                 | 168 ms: 1.01x slower                                   |
| pyflate                 | 417 ms                                                 | 424 ms: 1.02x slower                                   |
| crypto_pyaes            | 73.9 ms                                                | 75.2 ms: 1.02x slower                                  |
| mako                    | 9.85 ms                                                | 10.1 ms: 1.02x slower                                  |
| django_template         | 32.5 ms                                                | 33.2 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 298 ms: 1.03x slower                                   |
| regex_dna               | 203 ms                                                 | 209 ms: 1.03x slower                                   |
| xml_etree_process       | 53.8 ms                                                | 55.4 ms: 1.03x slower                                  |
| thrift                  | 752 us                                                 | 777 us: 1.03x slower                                   |
| unpickle                | 13.3 us                                                | 13.7 us: 1.03x slower                                  |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.60 ms: 1.04x slower                                  |
| async_tree_memoization  | 625 ms                                                 | 653 ms: 1.04x slower                                   |
| scimark_lu              | 107 ms                                                 | 112 ms: 1.05x slower                                   |
| sqlglot_transpile       | 1.66 ms                                                | 1.74 ms: 1.05x slower                                  |
| unpickle_list           | 4.95 us                                                | 5.22 us: 1.05x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.63 us: 1.06x slower                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.45 ms: 1.06x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 81.3 ms: 1.07x slower                                  |
| python_startup          | 8.36 ms                                                | 9.03 ms: 1.08x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.55 ms: 1.10x slower                                  |
| async_generators        | 359 ms                                                 | 421 ms: 1.17x slower                                   |
| Geometric mean          | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (9): sqlalchemy_declarative, unpack_sequence, scimark_monte_carlo, telco, bench_mp_pool, sqlalchemy_imperative, pickle_dict, sympy_str, chameleon
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230304-3.12.0a5+-eff9f43/bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
