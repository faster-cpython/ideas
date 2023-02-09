
# Results vs. 3.11.0

- fork: faster-cpython
- ref: pep_669_incremental
- machine: linux-x86_64
- commit hash: 825f42a
- commit date: 2023-02-09
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 246 ms: 1.05x faster                                                            |
| chameleon      | 6.41 ms                                                | 6.23 ms: 1.03x faster                                                           |
| docutils       | 2.60 sec                                               | 2.49 sec: 1.04x faster                                                          |
| html5lib       | 63.2 ms                                                | 58.7 ms: 1.08x faster                                                           |
| tornado_http   | 96.6 ms                                                | 92.8 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.4 ms: 1.07x faster                                                           |
| nbody          | 95.0 ms                                                | 90.7 ms: 1.05x faster                                                           |
| pidigits       | 199 ms                                                 | 192 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 124 ms: 1.10x faster                                                            |
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                           |
| regex_dna      | 203 ms                                                 | 201 ms: 1.01x faster                                                            |
| regex_effbot   | 3.36 ms                                                | 3.57 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.44 ms: 1.34x faster                                                           |
| unpickle_pure_python | 225 us                                                 | 194 us: 1.16x faster                                                            |
| json_loads           | 26.2 us                                                | 23.7 us: 1.10x faster                                                           |
| pickle_pure_python   | 304 us                                                 | 279 us: 1.09x faster                                                            |
| pickle_dict          | 31.4 us                                                | 29.4 us: 1.07x faster                                                           |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                            |
| pickle_list          | 4.17 us                                                | 4.04 us: 1.03x faster                                                           |
| xml_etree_iterparse  | 103 ms                                                 | 100 ms: 1.02x faster                                                            |
| unpickle             | 13.3 us                                                | 13.5 us: 1.02x slower                                                           |
| pickle               | 9.79 us                                                | 10.0 us: 1.02x slower                                                           |
| xml_etree_process    | 53.8 ms                                                | 55.1 ms: 1.02x slower                                                           |
| unpickle_list        | 4.95 us                                                | 5.15 us: 1.04x slower                                                           |
| xml_etree_generate   | 76.2 ms                                                | 79.6 ms: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.94 ms: 1.07x slower                                                           |
| python_startup_no_site | 5.96 ms                                                | 6.50 ms: 1.09x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 45.5 ms: 1.14x faster                                                           |
| genshi_text     | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                           |
| django_template | 32.5 ms                                                | 32.2 ms: 1.01x faster                                                           |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.44 ms: 1.34x faster                                                           |
| generators              | 72.2 ms                                                | 54.8 ms: 1.32x faster                                                           |
| deltablue               | 3.64 ms                                                | 3.11 ms: 1.17x faster                                                           |
| unpickle_pure_python    | 225 us                                                 | 194 us: 1.16x faster                                                            |
| genshi_xml              | 52.1 ms                                                | 45.5 ms: 1.14x faster                                                           |
| scimark_sor             | 115 ms                                                 | 102 ms: 1.13x faster                                                            |
| nqueens                 | 85.0 ms                                                | 75.5 ms: 1.13x faster                                                           |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.92 ms: 1.12x faster                                                           |
| richards                | 46.2 ms                                                | 41.2 ms: 1.12x faster                                                           |
| go                      | 143 ms                                                 | 129 ms: 1.12x faster                                                            |
| json_loads              | 26.2 us                                                | 23.7 us: 1.10x faster                                                           |
| scimark_fft             | 329 ms                                                 | 299 ms: 1.10x faster                                                            |
| regex_compile           | 136 ms                                                 | 124 ms: 1.10x faster                                                            |
| hexiom                  | 6.35 ms                                                | 5.79 ms: 1.10x faster                                                           |
| chaos                   | 68.6 ms                                                | 62.6 ms: 1.10x faster                                                           |
| deepcopy_memo           | 36.4 us                                                | 33.3 us: 1.09x faster                                                           |
| pickle_pure_python      | 304 us                                                 | 279 us: 1.09x faster                                                            |
| pycparser               | 1.17 sec                                               | 1.08 sec: 1.09x faster                                                          |
| json                    | 4.95 ms                                                | 4.56 ms: 1.08x faster                                                           |
| sympy_str               | 287 ms                                                 | 265 ms: 1.08x faster                                                            |
| genshi_text             | 22.1 ms                                                | 20.5 ms: 1.08x faster                                                           |
| html5lib                | 63.2 ms                                                | 58.7 ms: 1.08x faster                                                           |
| fannkuch                | 388 ms                                                 | 361 ms: 1.07x faster                                                            |
| logging_simple          | 6.06 us                                                | 5.65 us: 1.07x faster                                                           |
| sympy_sum               | 166 ms                                                 | 155 ms: 1.07x faster                                                            |
| deepcopy                | 344 us                                                 | 321 us: 1.07x faster                                                            |
| spectral_norm           | 99.9 ms                                                | 93.3 ms: 1.07x faster                                                           |
| scimark_monte_carlo     | 68.3 ms                                                | 63.8 ms: 1.07x faster                                                           |
| sympy_integrate         | 20.9 ms                                                | 19.5 ms: 1.07x faster                                                           |
| pickle_dict             | 31.4 us                                                | 29.4 us: 1.07x faster                                                           |
| float                   | 76.3 ms                                                | 71.4 ms: 1.07x faster                                                           |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                            |
| gunicorn                | 1.12 ms                                                | 1.05 ms: 1.07x faster                                                           |
| aiohttp                 | 1.05 ms                                                | 983 us: 1.06x faster                                                            |
| sqlglot_optimize        | 53.0 ms                                                | 49.8 ms: 1.06x faster                                                           |
| sympy_expand            | 472 ms                                                 | 446 ms: 1.06x faster                                                            |
| logging_silent          | 98.5 ns                                                | 93.1 ns: 1.06x faster                                                           |
| logging_format          | 6.62 us                                                | 6.26 us: 1.06x faster                                                           |
| sqlglot_normalize       | 108 ms                                                 | 102 ms: 1.06x faster                                                            |
| raytrace                | 290 ms                                                 | 276 ms: 1.05x faster                                                            |
| bench_thread_pool       | 810 us                                                 | 771 us: 1.05x faster                                                            |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.05x faster                                                          |
| 2to3                    | 257 ms                                                 | 246 ms: 1.05x faster                                                            |
| nbody                   | 95.0 ms                                                | 90.7 ms: 1.05x faster                                                           |
| scimark_lu              | 107 ms                                                 | 103 ms: 1.05x faster                                                            |
| telco                   | 6.62 ms                                                | 6.35 ms: 1.04x faster                                                           |
| docutils                | 2.60 sec                                               | 2.49 sec: 1.04x faster                                                          |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.3 ms: 1.04x faster                                                           |
| tornado_http            | 96.6 ms                                                | 92.8 ms: 1.04x faster                                                           |
| unpack_sequence         | 43.4 ns                                                | 41.8 ns: 1.04x faster                                                           |
| dulwich_log             | 63.9 ms                                                | 61.5 ms: 1.04x faster                                                           |
| deepcopy_reduce         | 2.97 us                                                | 2.86 us: 1.04x faster                                                           |
| sqlalchemy_declarative  | 139 ms                                                 | 134 ms: 1.04x faster                                                            |
| pidigits                | 199 ms                                                 | 192 ms: 1.04x faster                                                            |
| pickle_list             | 4.17 us                                                | 4.04 us: 1.03x faster                                                           |
| pprint_safe_repr        | 691 ms                                                 | 668 ms: 1.03x faster                                                            |
| coverage                | 101 ms                                                 | 97.7 ms: 1.03x faster                                                           |
| chameleon               | 6.41 ms                                                | 6.23 ms: 1.03x faster                                                           |
| crypto_pyaes            | 73.9 ms                                                | 72.1 ms: 1.02x faster                                                           |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                           |
| xml_etree_iterparse     | 103 ms                                                 | 100 ms: 1.02x faster                                                            |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                           |
| pyflate                 | 417 ms                                                 | 410 ms: 1.02x faster                                                            |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.01x faster                                                            |
| regex_dna               | 203 ms                                                 | 201 ms: 1.01x faster                                                            |
| django_template         | 32.5 ms                                                | 32.2 ms: 1.01x faster                                                           |
| thrift                  | 752 us                                                 | 762 us: 1.01x slower                                                            |
| sqlglot_transpile       | 1.66 ms                                                | 1.69 ms: 1.02x slower                                                           |
| mdp                     | 2.62 sec                                               | 2.67 sec: 1.02x slower                                                          |
| unpickle                | 13.3 us                                                | 13.5 us: 1.02x slower                                                           |
| async_tree_cpu_io_mixed | 752 ms                                                 | 767 ms: 1.02x slower                                                            |
| sqlglot_parse           | 1.37 ms                                                | 1.40 ms: 1.02x slower                                                           |
| pickle                  | 9.79 us                                                | 10.0 us: 1.02x slower                                                           |
| xml_etree_process       | 53.8 ms                                                | 55.1 ms: 1.02x slower                                                           |
| async_tree_io           | 1.31 sec                                               | 1.34 sec: 1.03x slower                                                          |
| async_tree_memoization  | 625 ms                                                 | 643 ms: 1.03x slower                                                            |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.03x slower                                                           |
| unpickle_list           | 4.95 us                                                | 5.15 us: 1.04x slower                                                           |
| xml_etree_generate      | 76.2 ms                                                | 79.6 ms: 1.04x slower                                                           |
| regex_effbot            | 3.36 ms                                                | 3.57 ms: 1.06x slower                                                           |
| python_startup          | 8.36 ms                                                | 8.94 ms: 1.07x slower                                                           |
| python_startup_no_site  | 5.96 ms                                                | 6.50 ms: 1.09x slower                                                           |
| async_generators        | 359 ms                                                 | 420 ms: 1.17x slower                                                            |
| coroutines              | 26.1 ms                                                | 54.8 ms: 2.10x slower                                                           |
| Geometric mean          | (ref)                                                  | 1.04x faster                                                                    |

Benchmark hidden because not significant (3): mako, async_tree_none, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230209-3.12.0a5+-825f42a/bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
