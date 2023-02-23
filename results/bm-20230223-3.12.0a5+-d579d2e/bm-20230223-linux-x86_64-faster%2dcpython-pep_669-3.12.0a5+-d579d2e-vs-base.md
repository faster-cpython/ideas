
# Results vs. base

- fork: faster-cpython
- ref: pep_669
- machine: linux-x86_64
- commit hash: d579d2e
- commit date: 2023-02-23
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 247 ms: 1.01x faster                                                |
| chameleon      | 6.42 ms                                                                | 6.26 ms: 1.03x faster                                               |
| docutils       | 2.54 sec                                                               | 2.51 sec: 1.01x faster                                              |
| html5lib       | 61.6 ms                                                                | 59.8 ms: 1.03x faster                                               |
| tornado_http   | 94.8 ms                                                                | 93.8 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.6 ms                                                                | 92.2 ms: 1.05x faster                                               |
| pidigits       | 190 ms                                                                 | 192 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 206 ms                                                                 | 200 ms: 1.03x faster                                                |
| regex_compile  | 132 ms                                                                 | 129 ms: 1.03x faster                                                |
| regex_v8       | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 32.3 us                                                                | 31.7 us: 1.02x faster                                               |
| unpickle_pure_python | 198 us                                                                 | 194 us: 1.02x faster                                                |
| unpickle_list        | 5.06 us                                                                | 4.98 us: 1.02x faster                                               |
| pickle_pure_python   | 281 us                                                                 | 277 us: 1.01x faster                                                |
| xml_etree_process    | 55.1 ms                                                                | 54.4 ms: 1.01x faster                                               |
| xml_etree_generate   | 80.2 ms                                                                | 79.4 ms: 1.01x faster                                               |
| json_dumps           | 9.48 ms                                                                | 9.40 ms: 1.01x faster                                               |
| pickle_list          | 4.30 us                                                                | 4.27 us: 1.01x faster                                               |
| unpickle             | 13.4 us                                                                | 13.9 us: 1.03x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (4): xml_etree_parse, json_loads, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 9.00 ms                                                                | 9.06 ms: 1.01x slower                                               |
| python_startup_no_site | 6.52 ms                                                                | 6.58 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 21.2 ms                                                                | 20.5 ms: 1.03x faster                                               |
| genshi_xml      | 47.1 ms                                                                | 45.9 ms: 1.03x faster                                               |
| mako            | 9.95 ms                                                                | 9.75 ms: 1.02x faster                                               |
| django_template | 33.1 ms                                                                | 32.8 ms: 1.01x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5+-22b8d77 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| scimark_fft             | 318 ms                                                                 | 302 ms: 1.05x faster                                                |
| deepcopy_memo           | 34.7 us                                                                | 33.1 us: 1.05x faster                                               |
| scimark_sparse_mat_mult | 4.55 ms                                                                | 4.34 ms: 1.05x faster                                               |
| nbody                   | 96.6 ms                                                                | 92.2 ms: 1.05x faster                                               |
| scimark_monte_carlo     | 67.1 ms                                                                | 64.2 ms: 1.04x faster                                               |
| go                      | 135 ms                                                                 | 130 ms: 1.04x faster                                                |
| genshi_text             | 21.2 ms                                                                | 20.5 ms: 1.03x faster                                               |
| scimark_lu              | 110 ms                                                                 | 106 ms: 1.03x faster                                                |
| telco                   | 6.55 ms                                                                | 6.35 ms: 1.03x faster                                               |
| coroutines              | 22.8 ms                                                                | 22.0 ms: 1.03x faster                                               |
| html5lib                | 61.6 ms                                                                | 59.8 ms: 1.03x faster                                               |
| nqueens                 | 80.6 ms                                                                | 78.4 ms: 1.03x faster                                               |
| regex_dna               | 206 ms                                                                 | 200 ms: 1.03x faster                                                |
| pprint_safe_repr        | 681 ms                                                                 | 662 ms: 1.03x faster                                                |
| genshi_xml              | 47.1 ms                                                                | 45.9 ms: 1.03x faster                                               |
| chameleon               | 6.42 ms                                                                | 6.26 ms: 1.03x faster                                               |
| regex_compile           | 132 ms                                                                 | 129 ms: 1.03x faster                                                |
| sqlglot_parse           | 1.43 ms                                                                | 1.39 ms: 1.02x faster                                               |
| chaos                   | 67.8 ms                                                                | 66.2 ms: 1.02x faster                                               |
| pprint_pformat          | 1.40 sec                                                               | 1.37 sec: 1.02x faster                                              |
| mako                    | 9.95 ms                                                                | 9.75 ms: 1.02x faster                                               |
| pickle_dict             | 32.3 us                                                                | 31.7 us: 1.02x faster                                               |
| sqlglot_transpile       | 1.71 ms                                                                | 1.68 ms: 1.02x faster                                               |
| dask                    | 500 ms                                                                 | 490 ms: 1.02x faster                                                |
| unpickle_pure_python    | 198 us                                                                 | 194 us: 1.02x faster                                                |
| pathlib                 | 18.0 ms                                                                | 17.6 ms: 1.02x faster                                               |
| dulwich_log             | 62.7 ms                                                                | 61.6 ms: 1.02x faster                                               |
| hexiom                  | 6.10 ms                                                                | 6.00 ms: 1.02x faster                                               |
| sqlalchemy_imperative   | 17.9 ms                                                                | 17.6 ms: 1.02x faster                                               |
| sqlglot_normalize       | 103 ms                                                                 | 102 ms: 1.02x faster                                                |
| unpickle_list           | 5.06 us                                                                | 4.98 us: 1.02x faster                                               |
| scimark_sor             | 105 ms                                                                 | 104 ms: 1.02x faster                                                |
| sympy_str               | 283 ms                                                                 | 279 ms: 1.01x faster                                                |
| deepcopy                | 327 us                                                                 | 323 us: 1.01x faster                                                |
| sympy_integrate         | 20.5 ms                                                                | 20.2 ms: 1.01x faster                                               |
| docutils                | 2.54 sec                                                               | 2.51 sec: 1.01x faster                                              |
| mypy2                   | 331 ms                                                                 | 327 ms: 1.01x faster                                                |
| sqlglot_optimize        | 50.8 ms                                                                | 50.1 ms: 1.01x faster                                               |
| raytrace                | 284 ms                                                                 | 280 ms: 1.01x faster                                                |
| pyflate                 | 406 ms                                                                 | 401 ms: 1.01x faster                                                |
| logging_silent          | 92.8 ns                                                                | 91.7 ns: 1.01x faster                                               |
| pickle_pure_python      | 281 us                                                                 | 277 us: 1.01x faster                                                |
| xml_etree_process       | 55.1 ms                                                                | 54.4 ms: 1.01x faster                                               |
| sympy_expand            | 456 ms                                                                 | 451 ms: 1.01x faster                                                |
| tornado_http            | 94.8 ms                                                                | 93.8 ms: 1.01x faster                                               |
| thrift                  | 764 us                                                                 | 756 us: 1.01x faster                                                |
| 2to3                    | 249 ms                                                                 | 247 ms: 1.01x faster                                                |
| deepcopy_reduce         | 2.95 us                                                                | 2.92 us: 1.01x faster                                               |
| pycparser               | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                              |
| django_template         | 33.1 ms                                                                | 32.8 ms: 1.01x faster                                               |
| xml_etree_generate      | 80.2 ms                                                                | 79.4 ms: 1.01x faster                                               |
| spectral_norm           | 95.5 ms                                                                | 94.6 ms: 1.01x faster                                               |
| richards                | 42.0 ms                                                                | 41.6 ms: 1.01x faster                                               |
| json_dumps              | 9.48 ms                                                                | 9.40 ms: 1.01x faster                                               |
| aiohttp                 | 1.01 ms                                                                | 1.00 ms: 1.01x faster                                               |
| logging_simple          | 5.83 us                                                                | 5.78 us: 1.01x faster                                               |
| gunicorn                | 1.09 ms                                                                | 1.08 ms: 1.01x faster                                               |
| deltablue               | 3.16 ms                                                                | 3.14 ms: 1.01x faster                                               |
| bench_thread_pool       | 788 us                                                                 | 782 us: 1.01x faster                                                |
| sympy_sum               | 166 ms                                                                 | 165 ms: 1.01x faster                                                |
| pickle_list             | 4.30 us                                                                | 4.27 us: 1.01x faster                                               |
| crypto_pyaes            | 72.8 ms                                                                | 72.4 ms: 1.01x faster                                               |
| asyncio_tcp             | 500 ms                                                                 | 498 ms: 1.00x faster                                                |
| logging_format          | 6.42 us                                                                | 6.46 us: 1.01x slower                                               |
| python_startup          | 9.00 ms                                                                | 9.06 ms: 1.01x slower                                               |
| python_startup_no_site  | 6.52 ms                                                                | 6.58 ms: 1.01x slower                                               |
| regex_v8                | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                               |
| json                    | 4.52 ms                                                                | 4.58 ms: 1.01x slower                                               |
| pidigits                | 190 ms                                                                 | 192 ms: 1.01x slower                                                |
| async_tree_io           | 1.28 sec                                                               | 1.30 sec: 1.02x slower                                              |
| coverage                | 94.8 ms                                                                | 96.9 ms: 1.02x slower                                               |
| create_gc_cycles        | 1.48 ms                                                                | 1.51 ms: 1.03x slower                                               |
| async_generators        | 416 ms                                                                 | 430 ms: 1.03x slower                                                |
| unpickle                | 13.4 us                                                                | 13.9 us: 1.03x slower                                               |
| sqlite_synth            | 2.62 us                                                                | 2.73 us: 1.04x slower                                               |
| gc_traversal            | 3.66 ms                                                                | 3.83 ms: 1.05x slower                                               |
| mdp                     | 2.49 sec                                                               | 2.60 sec: 1.05x slower                                              |
| generators              | 29.9 ms                                                                | 31.6 ms: 1.06x slower                                               |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (15): djangocms, sqlalchemy_declarative, unpack_sequence, xml_etree_parse, json_loads, pickle, bench_mp_pool, meteor_contest, xml_etree_iterparse, regex_effbot, fannkuch, float, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none
