
# Results vs. 3.11.0

- fork: faster-cpython
- ref: pep_669_incremental
- machine: linux-x86_64
- commit hash: 5629a3e
- commit date: 2023-02-17
- overall geometric mean: 1.05x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 244 ms: 1.05x faster                                                            |
| chameleon      | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                           |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                          |
| html5lib       | 63.2 ms                                                | 59.7 ms: 1.06x faster                                                           |
| tornado_http   | 96.6 ms                                                | 93.3 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.4 ms: 1.05x faster                                                           |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                                            |
| nbody          | 95.0 ms                                                | 92.4 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 125 ms: 1.09x faster                                                            |
| regex_v8       | 22.3 ms                                                | 22.5 ms: 1.01x slower                                                           |
| regex_dna      | 203 ms                                                 | 205 ms: 1.01x slower                                                            |
| regex_effbot   | 3.36 ms                                                | 3.65 ms: 1.09x slower                                                           |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.37 ms: 1.35x faster                                                           |
| unpickle_pure_python | 225 us                                                 | 193 us: 1.16x faster                                                            |
| json_loads           | 26.2 us                                                | 23.7 us: 1.11x faster                                                           |
| pickle_pure_python   | 304 us                                                 | 279 us: 1.09x faster                                                            |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                            |
| xml_etree_iterparse  | 103 ms                                                 | 100 ms: 1.03x faster                                                            |
| pickle_dict          | 31.4 us                                                | 30.8 us: 1.02x faster                                                           |
| pickle_list          | 4.17 us                                                | 4.25 us: 1.02x slower                                                           |
| xml_etree_process    | 53.8 ms                                                | 55.0 ms: 1.02x slower                                                           |
| unpickle_list        | 4.95 us                                                | 5.08 us: 1.02x slower                                                           |
| unpickle             | 13.3 us                                                | 13.7 us: 1.04x slower                                                           |
| xml_etree_generate   | 76.2 ms                                                | 80.3 ms: 1.05x slower                                                           |
| pickle               | 9.79 us                                                | 10.3 us: 1.06x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.97 ms: 1.07x slower                                                           |
| python_startup_no_site | 5.96 ms                                                | 6.52 ms: 1.09x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 46.0 ms: 1.13x faster                                                           |
| genshi_text     | 22.1 ms                                                | 20.6 ms: 1.08x faster                                                           |
| mako            | 9.85 ms                                                | 9.76 ms: 1.01x faster                                                           |
| django_template | 32.5 ms                                                | 33.1 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 30.8 ms: 2.34x faster                                                           |
| json_dumps              | 12.7 ms                                                | 9.37 ms: 1.35x faster                                                           |
| coroutines              | 26.1 ms                                                | 21.1 ms: 1.24x faster                                                           |
| unpickle_pure_python    | 225 us                                                 | 193 us: 1.16x faster                                                            |
| deltablue               | 3.64 ms                                                | 3.13 ms: 1.16x faster                                                           |
| genshi_xml              | 52.1 ms                                                | 46.0 ms: 1.13x faster                                                           |
| json_loads              | 26.2 us                                                | 23.7 us: 1.11x faster                                                           |
| nqueens                 | 85.0 ms                                                | 76.9 ms: 1.11x faster                                                           |
| richards                | 46.2 ms                                                | 41.9 ms: 1.10x faster                                                           |
| deepcopy_memo           | 36.4 us                                                | 33.4 us: 1.09x faster                                                           |
| fannkuch                | 388 ms                                                 | 356 ms: 1.09x faster                                                            |
| pickle_pure_python      | 304 us                                                 | 279 us: 1.09x faster                                                            |
| scimark_sor             | 115 ms                                                 | 106 ms: 1.09x faster                                                            |
| regex_compile           | 136 ms                                                 | 125 ms: 1.09x faster                                                            |
| sympy_str               | 287 ms                                                 | 265 ms: 1.08x faster                                                            |
| scimark_fft             | 329 ms                                                 | 305 ms: 1.08x faster                                                            |
| spectral_norm           | 99.9 ms                                                | 92.7 ms: 1.08x faster                                                           |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                                            |
| genshi_text             | 22.1 ms                                                | 20.6 ms: 1.08x faster                                                           |
| json                    | 4.95 ms                                                | 4.62 ms: 1.07x faster                                                           |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                            |
| sympy_integrate         | 20.9 ms                                                | 19.5 ms: 1.07x faster                                                           |
| sympy_sum               | 166 ms                                                 | 155 ms: 1.07x faster                                                            |
| mdp                     | 2.62 sec                                               | 2.46 sec: 1.07x faster                                                          |
| chaos                   | 68.6 ms                                                | 64.5 ms: 1.06x faster                                                           |
| logging_simple          | 6.06 us                                                | 5.72 us: 1.06x faster                                                           |
| hexiom                  | 6.35 ms                                                | 5.99 ms: 1.06x faster                                                           |
| html5lib                | 63.2 ms                                                | 59.7 ms: 1.06x faster                                                           |
| deepcopy                | 344 us                                                 | 325 us: 1.06x faster                                                            |
| gunicorn                | 1.12 ms                                                | 1.06 ms: 1.05x faster                                                           |
| 2to3                    | 257 ms                                                 | 244 ms: 1.05x faster                                                            |
| float                   | 76.3 ms                                                | 72.4 ms: 1.05x faster                                                           |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                                            |
| sympy_expand            | 472 ms                                                 | 449 ms: 1.05x faster                                                            |
| logging_silent          | 98.5 ns                                                | 93.8 ns: 1.05x faster                                                           |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.20 ms: 1.05x faster                                                           |
| pprint_pformat          | 1.44 sec                                               | 1.38 sec: 1.05x faster                                                          |
| sqlglot_optimize        | 53.0 ms                                                | 50.6 ms: 1.05x faster                                                           |
| scimark_monte_carlo     | 68.3 ms                                                | 65.2 ms: 1.05x faster                                                           |
| aiohttp                 | 1.05 ms                                                | 1000 us: 1.05x faster                                                           |
| logging_format          | 6.62 us                                                | 6.33 us: 1.05x faster                                                           |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.04x faster                                                            |
| dulwich_log             | 63.9 ms                                                | 61.2 ms: 1.04x faster                                                           |
| pyflate                 | 417 ms                                                 | 401 ms: 1.04x faster                                                            |
| bench_thread_pool       | 810 us                                                 | 779 us: 1.04x faster                                                            |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                                          |
| telco                   | 6.62 ms                                                | 6.38 ms: 1.04x faster                                                           |
| pycparser               | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                          |
| raytrace                | 290 ms                                                 | 280 ms: 1.04x faster                                                            |
| tornado_http            | 96.6 ms                                                | 93.3 ms: 1.04x faster                                                           |
| sqlalchemy_declarative  | 139 ms                                                 | 135 ms: 1.03x faster                                                            |
| pprint_safe_repr        | 691 ms                                                 | 671 ms: 1.03x faster                                                            |
| nbody                   | 95.0 ms                                                | 92.4 ms: 1.03x faster                                                           |
| xml_etree_iterparse     | 103 ms                                                 | 100 ms: 1.03x faster                                                            |
| unpack_sequence         | 43.4 ns                                                | 42.4 ns: 1.02x faster                                                           |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.6 ms: 1.02x faster                                                           |
| deepcopy_reduce         | 2.97 us                                                | 2.90 us: 1.02x faster                                                           |
| async_tree_none         | 529 ms                                                 | 518 ms: 1.02x faster                                                            |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.02x faster                                                            |
| pickle_dict             | 31.4 us                                                | 30.8 us: 1.02x faster                                                           |
| crypto_pyaes            | 73.9 ms                                                | 72.6 ms: 1.02x faster                                                           |
| coverage                | 101 ms                                                 | 99.2 ms: 1.01x faster                                                           |
| chameleon               | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                           |
| async_tree_io           | 1.31 sec                                               | 1.29 sec: 1.01x faster                                                          |
| mako                    | 9.85 ms                                                | 9.76 ms: 1.01x faster                                                           |
| regex_v8                | 22.3 ms                                                | 22.5 ms: 1.01x slower                                                           |
| regex_dna               | 203 ms                                                 | 205 ms: 1.01x slower                                                            |
| thrift                  | 752 us                                                 | 761 us: 1.01x slower                                                            |
| pickle_list             | 4.17 us                                                | 4.25 us: 1.02x slower                                                           |
| django_template         | 32.5 ms                                                | 33.1 ms: 1.02x slower                                                           |
| sqlglot_transpile       | 1.66 ms                                                | 1.69 ms: 1.02x slower                                                           |
| xml_etree_process       | 53.8 ms                                                | 55.0 ms: 1.02x slower                                                           |
| unpickle_list           | 4.95 us                                                | 5.08 us: 1.02x slower                                                           |
| sqlglot_parse           | 1.37 ms                                                | 1.41 ms: 1.03x slower                                                           |
| unpickle                | 13.3 us                                                | 13.7 us: 1.04x slower                                                           |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                                           |
| async_tree_memoization  | 625 ms                                                 | 655 ms: 1.05x slower                                                            |
| xml_etree_generate      | 76.2 ms                                                | 80.3 ms: 1.05x slower                                                           |
| pickle                  | 9.79 us                                                | 10.3 us: 1.06x slower                                                           |
| python_startup          | 8.36 ms                                                | 8.97 ms: 1.07x slower                                                           |
| regex_effbot            | 3.36 ms                                                | 3.65 ms: 1.09x slower                                                           |
| python_startup_no_site  | 5.96 ms                                                | 6.52 ms: 1.09x slower                                                           |
| async_generators        | 359 ms                                                 | 422 ms: 1.17x slower                                                            |
| Geometric mean          | (ref)                                                  | 1.05x faster                                                                    |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, bench_mp_pool, pathlib, scimark_lu
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230217-3.12.0a5+-5629a3e/bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
