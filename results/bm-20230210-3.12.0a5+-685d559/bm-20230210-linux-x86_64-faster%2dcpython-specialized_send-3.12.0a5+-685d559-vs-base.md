
# Results vs. base

- fork: faster-cpython
- ref: specialized_send
- machine: linux-x86_64
- commit hash: 685d559
- commit date: 2023-02-10
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 246 ms: 1.02x faster                                                         |
| docutils       | 2.52 sec                                                               | 2.54 sec: 1.01x slower                                                       |
| tornado_http   | 93.6 ms                                                                | 95.1 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): chameleon, html5lib

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 93.8 ms                                                                | 93.0 ms: 1.01x faster                                                        |
| pidigits       | 189 ms                                                                 | 197 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.73 ms                                                                | 3.38 ms: 1.10x faster                                                        |
| regex_compile  | 129 ms                                                                 | 131 ms: 1.01x slower                                                         |
| regex_dna      | 207 ms                                                                 | 211 ms: 1.02x slower                                                         |
| regex_v8       | 21.0 ms                                                                | 22.3 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_list        | 5.14 us                                                                | 4.97 us: 1.03x faster                                                        |
| pickle_list          | 4.22 us                                                                | 4.12 us: 1.02x faster                                                        |
| json_dumps           | 9.59 ms                                                                | 9.46 ms: 1.01x faster                                                        |
| xml_etree_iterparse  | 102 ms                                                                 | 102 ms: 1.01x faster                                                         |
| pickle_dict          | 31.1 us                                                                | 30.9 us: 1.00x faster                                                        |
| unpickle_pure_python | 198 us                                                                 | 199 us: 1.01x slower                                                         |
| xml_etree_generate   | 79.9 ms                                                                | 80.6 ms: 1.01x slower                                                        |
| xml_etree_process    | 55.0 ms                                                                | 55.9 ms: 1.02x slower                                                        |
| unpickle             | 13.0 us                                                                | 13.7 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (4): pickle, pickle_pure_python, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.52 ms                                                                | 6.49 ms: 1.00x faster                                                        |
| python_startup         | 8.98 ms                                                                | 8.96 ms: 1.00x faster                                                        |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 21.3 ms                                                                | 20.8 ms: 1.03x faster                                                        |
| django_template | 33.3 ms                                                                | 32.5 ms: 1.02x faster                                                        |
| mako            | 9.77 ms                                                                | 9.75 ms: 1.00x faster                                                        |
| genshi_xml      | 46.8 ms                                                                | 48.1 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark               | bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5+-d40a23c | bm-20230210-linux-x86_64-faster%2dcpython-specialized_send-3.12.0a5+-685d559 |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| generators              | 77.3 ms                                                                | 31.1 ms: 2.48x faster                                                        |
| coroutines              | 25.3 ms                                                                | 22.3 ms: 1.14x faster                                                        |
| regex_effbot            | 3.73 ms                                                                | 3.38 ms: 1.10x faster                                                        |
| async_generators        | 425 ms                                                                 | 410 ms: 1.04x faster                                                         |
| unpickle_list           | 5.14 us                                                                | 4.97 us: 1.03x faster                                                        |
| spectral_norm           | 98.5 ms                                                                | 95.8 ms: 1.03x faster                                                        |
| genshi_text             | 21.3 ms                                                                | 20.8 ms: 1.03x faster                                                        |
| logging_simple          | 5.81 us                                                                | 5.67 us: 1.03x faster                                                        |
| pickle_list             | 4.22 us                                                                | 4.12 us: 1.02x faster                                                        |
| django_template         | 33.3 ms                                                                | 32.5 ms: 1.02x faster                                                        |
| logging_format          | 6.40 us                                                                | 6.26 us: 1.02x faster                                                        |
| 2to3                    | 251 ms                                                                 | 246 ms: 1.02x faster                                                         |
| fannkuch                | 384 ms                                                                 | 376 ms: 1.02x faster                                                         |
| sqlglot_normalize       | 105 ms                                                                 | 103 ms: 1.02x faster                                                         |
| crypto_pyaes            | 74.9 ms                                                                | 73.7 ms: 1.02x faster                                                        |
| json_dumps              | 9.59 ms                                                                | 9.46 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult | 3.92 ms                                                                | 3.87 ms: 1.01x faster                                                        |
| deepcopy_reduce         | 2.95 us                                                                | 2.92 us: 1.01x faster                                                        |
| async_tree_cpu_io_mixed | 756 ms                                                                 | 750 ms: 1.01x faster                                                         |
| sqlglot_optimize        | 51.1 ms                                                                | 50.6 ms: 1.01x faster                                                        |
| nbody                   | 93.8 ms                                                                | 93.0 ms: 1.01x faster                                                        |
| asyncio_tcp             | 499 ms                                                                 | 495 ms: 1.01x faster                                                         |
| create_gc_cycles        | 1.49 ms                                                                | 1.48 ms: 1.01x faster                                                        |
| xml_etree_iterparse     | 102 ms                                                                 | 102 ms: 1.01x faster                                                         |
| deepcopy_memo           | 34.7 us                                                                | 34.5 us: 1.01x faster                                                        |
| pickle_dict             | 31.1 us                                                                | 30.9 us: 1.00x faster                                                        |
| python_startup_no_site  | 6.52 ms                                                                | 6.49 ms: 1.00x faster                                                        |
| mako                    | 9.77 ms                                                                | 9.75 ms: 1.00x faster                                                        |
| python_startup          | 8.98 ms                                                                | 8.96 ms: 1.00x faster                                                        |
| gc_traversal            | 3.91 ms                                                                | 3.91 ms: 1.00x faster                                                        |
| sympy_integrate         | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                        |
| go                      | 133 ms                                                                 | 134 ms: 1.01x slower                                                         |
| unpickle_pure_python    | 198 us                                                                 | 199 us: 1.01x slower                                                         |
| sympy_expand            | 453 ms                                                                 | 456 ms: 1.01x slower                                                         |
| docutils                | 2.52 sec                                                               | 2.54 sec: 1.01x slower                                                       |
| thrift                  | 760 us                                                                 | 766 us: 1.01x slower                                                         |
| bench_thread_pool       | 782 us                                                                 | 789 us: 1.01x slower                                                         |
| deepcopy                | 330 us                                                                 | 333 us: 1.01x slower                                                         |
| sympy_sum               | 156 ms                                                                 | 158 ms: 1.01x slower                                                         |
| xml_etree_generate      | 79.9 ms                                                                | 80.6 ms: 1.01x slower                                                        |
| sqlglot_transpile       | 1.71 ms                                                                | 1.72 ms: 1.01x slower                                                        |
| gunicorn                | 1.07 ms                                                                | 1.08 ms: 1.01x slower                                                        |
| pprint_pformat          | 1.39 sec                                                               | 1.41 sec: 1.01x slower                                                       |
| sqlglot_parse           | 1.41 ms                                                                | 1.43 ms: 1.01x slower                                                        |
| dulwich_log             | 62.6 ms                                                                | 63.4 ms: 1.01x slower                                                        |
| raytrace                | 282 ms                                                                 | 285 ms: 1.01x slower                                                         |
| aiohttp                 | 997 us                                                                 | 1.01 ms: 1.01x slower                                                        |
| pycparser               | 1.09 sec                                                               | 1.11 sec: 1.01x slower                                                       |
| scimark_fft             | 309 ms                                                                 | 313 ms: 1.01x slower                                                         |
| deltablue               | 3.14 ms                                                                | 3.19 ms: 1.01x slower                                                        |
| pprint_safe_repr        | 680 ms                                                                 | 690 ms: 1.01x slower                                                         |
| regex_compile           | 129 ms                                                                 | 131 ms: 1.01x slower                                                         |
| sqlalchemy_declarative  | 136 ms                                                                 | 138 ms: 1.02x slower                                                         |
| xml_etree_process       | 55.0 ms                                                                | 55.9 ms: 1.02x slower                                                        |
| tornado_http            | 93.6 ms                                                                | 95.1 ms: 1.02x slower                                                        |
| chaos                   | 65.1 ms                                                                | 66.1 ms: 1.02x slower                                                        |
| regex_dna               | 207 ms                                                                 | 211 ms: 1.02x slower                                                         |
| hexiom                  | 6.03 ms                                                                | 6.14 ms: 1.02x slower                                                        |
| coverage                | 95.9 ms                                                                | 98.1 ms: 1.02x slower                                                        |
| richards                | 42.0 ms                                                                | 42.9 ms: 1.02x slower                                                        |
| unpack_sequence         | 42.3 ns                                                                | 43.4 ns: 1.03x slower                                                        |
| genshi_xml              | 46.8 ms                                                                | 48.1 ms: 1.03x slower                                                        |
| scimark_sor             | 106 ms                                                                 | 109 ms: 1.03x slower                                                         |
| nqueens                 | 78.8 ms                                                                | 81.2 ms: 1.03x slower                                                        |
| logging_silent          | 90.9 ns                                                                | 94.0 ns: 1.03x slower                                                        |
| pidigits                | 189 ms                                                                 | 197 ms: 1.04x slower                                                         |
| unpickle                | 13.0 us                                                                | 13.7 us: 1.05x slower                                                        |
| regex_v8                | 21.0 ms                                                                | 22.3 ms: 1.06x slower                                                        |
| mdp                     | 2.51 sec                                                               | 2.75 sec: 1.09x slower                                                       |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                 |

Benchmark hidden because not significant (23): sqlalchemy_imperative, pickle, json, meteor_contest, scimark_monte_carlo, pickle_pure_python, sqlite_synth, pyflate, xml_etree_parse, json_loads, bench_mp_pool, float, chameleon, pathlib, async_tree_io, telco, sympy_str, mypy2, scimark_lu, async_tree_none, html5lib, djangocms, async_tree_memoization
