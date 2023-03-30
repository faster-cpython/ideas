
# Results vs. base

- fork: faster-cpython
- ref: pep_669
- machine: linux-x86_64
- commit hash: 662c16c
- commit date: 2023-03-25
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 247 ms: 1.02x faster                                                |
| chameleon      | 6.52 ms                                                                | 6.20 ms: 1.05x faster                                               |
| docutils       | 2.55 sec                                                               | 2.51 sec: 1.02x faster                                              |
| html5lib       | 62.3 ms                                                                | 60.5 ms: 1.03x faster                                               |
| tornado_http   | 91.1 ms                                                                | 90.0 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 87.8 ms                                                                | 84.3 ms: 1.04x faster                                               |
| float          | 73.9 ms                                                                | 71.2 ms: 1.04x faster                                               |
| pidigits       | 188 ms                                                                 | 188 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.66 ms                                                                | 3.47 ms: 1.05x faster                                               |
| regex_compile  | 135 ms                                                                 | 129 ms: 1.04x faster                                                |
| regex_dna      | 208 ms                                                                 | 203 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 202 us                                                                 | 197 us: 1.02x faster                                                |
| xml_etree_process    | 56.0 ms                                                                | 54.8 ms: 1.02x faster                                               |
| pickle_dict          | 31.0 us                                                                | 30.6 us: 1.01x faster                                               |
| unpickle_list        | 5.01 us                                                                | 4.94 us: 1.01x faster                                               |
| xml_etree_generate   | 80.3 ms                                                                | 79.2 ms: 1.01x faster                                               |
| pickle_list          | 4.27 us                                                                | 4.22 us: 1.01x faster                                               |
| pickle_pure_python   | 285 us                                                                 | 282 us: 1.01x faster                                                |
| pickle               | 10.4 us                                                                | 10.3 us: 1.01x faster                                               |
| json_loads           | 24.2 us                                                                | 24.0 us: 1.01x faster                                               |
| unpickle             | 13.2 us                                                                | 14.1 us: 1.07x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 8.79 ms                                                                | 8.86 ms: 1.01x slower                                               |
| python_startup_no_site | 6.50 ms                                                                | 6.57 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                                | 20.4 ms: 1.05x faster                                               |
| genshi_xml      | 47.6 ms                                                                | 46.0 ms: 1.04x faster                                               |
| django_template | 33.0 ms                                                                | 32.6 ms: 1.01x faster                                               |
| mako            | 9.89 ms                                                                | 9.85 ms: 1.00x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6+-2cdc518 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal            | 4.31 ms                                                                | 3.64 ms: 1.18x faster                                               |
| coroutines              | 23.9 ms                                                                | 22.1 ms: 1.08x faster                                               |
| generators              | 29.4 ms                                                                | 27.5 ms: 1.07x faster                                               |
| spectral_norm           | 94.0 ms                                                                | 88.8 ms: 1.06x faster                                               |
| regex_effbot            | 3.66 ms                                                                | 3.47 ms: 1.05x faster                                               |
| async_tree_memoization  | 652 ms                                                                 | 620 ms: 1.05x faster                                                |
| genshi_text             | 21.5 ms                                                                | 20.4 ms: 1.05x faster                                               |
| chameleon               | 6.52 ms                                                                | 6.20 ms: 1.05x faster                                               |
| logging_silent          | 96.5 ns                                                                | 92.5 ns: 1.04x faster                                               |
| regex_compile           | 135 ms                                                                 | 129 ms: 1.04x faster                                                |
| dask                    | 511 ms                                                                 | 490 ms: 1.04x faster                                                |
| telco                   | 6.67 ms                                                                | 6.41 ms: 1.04x faster                                               |
| nbody                   | 87.8 ms                                                                | 84.3 ms: 1.04x faster                                               |
| scimark_monte_carlo     | 67.8 ms                                                                | 65.2 ms: 1.04x faster                                               |
| float                   | 73.9 ms                                                                | 71.2 ms: 1.04x faster                                               |
| scimark_sor             | 112 ms                                                                 | 108 ms: 1.04x faster                                                |
| sqlglot_normalize       | 107 ms                                                                 | 104 ms: 1.04x faster                                                |
| pyflate                 | 421 ms                                                                 | 406 ms: 1.04x faster                                                |
| genshi_xml              | 47.6 ms                                                                | 46.0 ms: 1.04x faster                                               |
| pycparser               | 1.17 sec                                                               | 1.13 sec: 1.04x faster                                              |
| html5lib                | 62.3 ms                                                                | 60.5 ms: 1.03x faster                                               |
| sympy_str               | 285 ms                                                                 | 277 ms: 1.03x faster                                                |
| sympy_expand            | 463 ms                                                                 | 449 ms: 1.03x faster                                                |
| pathlib                 | 17.9 ms                                                                | 17.4 ms: 1.03x faster                                               |
| deepcopy                | 328 us                                                                 | 319 us: 1.03x faster                                                |
| sympy_integrate         | 20.6 ms                                                                | 20.0 ms: 1.03x faster                                               |
| sympy_sum               | 166 ms                                                                 | 162 ms: 1.03x faster                                                |
| richards                | 43.5 ms                                                                | 42.4 ms: 1.03x faster                                               |
| deepcopy_memo           | 34.1 us                                                                | 33.3 us: 1.02x faster                                               |
| sqlalchemy_imperative   | 17.6 ms                                                                | 17.1 ms: 1.02x faster                                               |
| regex_dna               | 208 ms                                                                 | 203 ms: 1.02x faster                                                |
| sqlglot_parse           | 1.43 ms                                                                | 1.40 ms: 1.02x faster                                               |
| mdp                     | 2.54 sec                                                               | 2.48 sec: 1.02x faster                                              |
| 2to3                    | 253 ms                                                                 | 247 ms: 1.02x faster                                                |
| sqlglot_transpile       | 1.72 ms                                                                | 1.68 ms: 1.02x faster                                               |
| unpickle_pure_python    | 202 us                                                                 | 197 us: 1.02x faster                                                |
| sqlalchemy_declarative  | 136 ms                                                                 | 133 ms: 1.02x faster                                                |
| xml_etree_process       | 56.0 ms                                                                | 54.8 ms: 1.02x faster                                               |
| mypy2                   | 333 ms                                                                 | 326 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed | 746 ms                                                                 | 731 ms: 1.02x faster                                                |
| sqlglot_optimize        | 51.3 ms                                                                | 50.4 ms: 1.02x faster                                               |
| crypto_pyaes            | 74.0 ms                                                                | 72.7 ms: 1.02x faster                                               |
| hexiom                  | 6.01 ms                                                                | 5.90 ms: 1.02x faster                                               |
| pprint_safe_repr        | 685 ms                                                                 | 673 ms: 1.02x faster                                                |
| dulwich_log             | 63.1 ms                                                                | 62.1 ms: 1.02x faster                                               |
| docutils                | 2.55 sec                                                               | 2.51 sec: 1.02x faster                                              |
| gunicorn                | 1.09 ms                                                                | 1.07 ms: 1.02x faster                                               |
| aiohttp                 | 1.01 ms                                                                | 991 us: 1.02x faster                                                |
| deepcopy_reduce         | 2.95 us                                                                | 2.90 us: 1.02x faster                                               |
| comprehensions          | 23.7 us                                                                | 23.3 us: 1.02x faster                                               |
| pickle_dict             | 31.0 us                                                                | 30.6 us: 1.01x faster                                               |
| unpickle_list           | 5.01 us                                                                | 4.94 us: 1.01x faster                                               |
| xml_etree_generate      | 80.3 ms                                                                | 79.2 ms: 1.01x faster                                               |
| bench_thread_pool       | 789 us                                                                 | 779 us: 1.01x faster                                                |
| pprint_pformat          | 1.40 sec                                                               | 1.38 sec: 1.01x faster                                              |
| unpack_sequence         | 43.7 ns                                                                | 43.1 ns: 1.01x faster                                               |
| tornado_http            | 91.1 ms                                                                | 90.0 ms: 1.01x faster                                               |
| pickle_list             | 4.27 us                                                                | 4.22 us: 1.01x faster                                               |
| pickle_pure_python      | 285 us                                                                 | 282 us: 1.01x faster                                                |
| deltablue               | 3.19 ms                                                                | 3.15 ms: 1.01x faster                                               |
| django_template         | 33.0 ms                                                                | 32.6 ms: 1.01x faster                                               |
| async_tree_io           | 1.29 sec                                                               | 1.28 sec: 1.01x faster                                              |
| pickle                  | 10.4 us                                                                | 10.3 us: 1.01x faster                                               |
| nqueens                 | 80.8 ms                                                                | 80.1 ms: 1.01x faster                                               |
| logging_format          | 6.28 us                                                                | 6.23 us: 1.01x faster                                               |
| json_loads              | 24.2 us                                                                | 24.0 us: 1.01x faster                                               |
| raytrace                | 280 ms                                                                 | 278 ms: 1.01x faster                                                |
| mako                    | 9.89 ms                                                                | 9.85 ms: 1.00x faster                                               |
| asyncio_tcp             | 503 ms                                                                 | 501 ms: 1.00x faster                                                |
| pidigits                | 188 ms                                                                 | 188 ms: 1.00x faster                                                |
| go                      | 137 ms                                                                 | 137 ms: 1.00x slower                                                |
| create_gc_cycles        | 1.46 ms                                                                | 1.47 ms: 1.01x slower                                               |
| python_startup          | 8.79 ms                                                                | 8.86 ms: 1.01x slower                                               |
| meteor_contest          | 102 ms                                                                 | 103 ms: 1.01x slower                                                |
| python_startup_no_site  | 6.50 ms                                                                | 6.57 ms: 1.01x slower                                               |
| coverage                | 95.5 ms                                                                | 96.7 ms: 1.01x slower                                               |
| scimark_sparse_mat_mult | 4.13 ms                                                                | 4.24 ms: 1.03x slower                                               |
| async_generators        | 408 ms                                                                 | 422 ms: 1.03x slower                                                |
| unpickle                | 13.2 us                                                                | 14.1 us: 1.07x slower                                               |
| Geometric mean          | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (15): async_tree_none, scimark_lu, djangocms, scimark_fft, xml_etree_parse, xml_etree_iterparse, json_dumps, bench_mp_pool, logging_simple, regex_v8, sqlite_synth, chaos, fannkuch, json, thrift
