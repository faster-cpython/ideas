
# Results vs. base

- fork: faster-cpython
- ref: pep_669_incremental
- machine: linux-x86_64
- commit hash: 5629a3e
- commit date: 2023-02-17
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                 | 244 ms: 1.01x faster                                                            |
| chameleon      | 6.39 ms                                                                | 6.33 ms: 1.01x faster                                                           |
| docutils       | 2.56 sec                                                               | 2.50 sec: 1.02x faster                                                          |
| html5lib       | 61.5 ms                                                                | 59.7 ms: 1.03x faster                                                           |
| tornado_http   | 95.5 ms                                                                | 93.3 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 73.4 ms                                                                | 72.4 ms: 1.01x faster                                                           |
| nbody          | 93.6 ms                                                                | 92.4 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 216 ms                                                                 | 205 ms: 1.06x faster                                                            |
| regex_compile  | 130 ms                                                                 | 125 ms: 1.04x faster                                                            |
| regex_v8       | 21.8 ms                                                                | 22.5 ms: 1.03x slower                                                           |
| regex_effbot   | 3.49 ms                                                                | 3.65 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.63 ms                                                                | 9.37 ms: 1.03x faster                                                           |
| pickle_pure_python   | 285 us                                                                 | 279 us: 1.02x faster                                                            |
| unpickle_pure_python | 197 us                                                                 | 193 us: 1.02x faster                                                            |
| xml_etree_process    | 55.8 ms                                                                | 55.0 ms: 1.02x faster                                                           |
| xml_etree_generate   | 81.2 ms                                                                | 80.3 ms: 1.01x faster                                                           |
| xml_etree_parse      | 148 ms                                                                 | 148 ms: 1.00x faster                                                            |
| json_loads           | 23.6 us                                                                | 23.7 us: 1.00x slower                                                           |
| pickle               | 10.1 us                                                                | 10.3 us: 1.02x slower                                                           |
| pickle_dict          | 30.0 us                                                                | 30.8 us: 1.03x slower                                                           |
| pickle_list          | 4.09 us                                                                | 4.25 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                    |

Benchmark hidden because not significant (3): unpickle, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.51 ms                                                                | 6.52 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                | 46.0 ms: 1.04x faster                                                           |
| genshi_text     | 21.2 ms                                                                | 20.6 ms: 1.03x faster                                                           |
| django_template | 33.5 ms                                                                | 33.1 ms: 1.01x faster                                                           |
| mako            | 9.83 ms                                                                | 9.76 ms: 1.01x faster                                                           |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5+-d919917 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mdp                     | 2.72 sec                                                               | 2.46 sec: 1.10x faster                                                          |
| gc_traversal            | 3.91 ms                                                                | 3.59 ms: 1.09x faster                                                           |
| coroutines              | 22.3 ms                                                                | 21.1 ms: 1.06x faster                                                           |
| spectral_norm           | 98.0 ms                                                                | 92.7 ms: 1.06x faster                                                           |
| regex_dna               | 216 ms                                                                 | 205 ms: 1.06x faster                                                            |
| raytrace                | 295 ms                                                                 | 280 ms: 1.05x faster                                                            |
| meteor_contest          | 107 ms                                                                 | 102 ms: 1.04x faster                                                            |
| regex_compile           | 130 ms                                                                 | 125 ms: 1.04x faster                                                            |
| genshi_xml              | 47.8 ms                                                                | 46.0 ms: 1.04x faster                                                           |
| sympy_str               | 275 ms                                                                 | 265 ms: 1.04x faster                                                            |
| genshi_text             | 21.2 ms                                                                | 20.6 ms: 1.03x faster                                                           |
| crypto_pyaes            | 75.0 ms                                                                | 72.6 ms: 1.03x faster                                                           |
| nqueens                 | 79.4 ms                                                                | 76.9 ms: 1.03x faster                                                           |
| deepcopy_memo           | 34.5 us                                                                | 33.4 us: 1.03x faster                                                           |
| deltablue               | 3.23 ms                                                                | 3.13 ms: 1.03x faster                                                           |
| html5lib                | 61.5 ms                                                                | 59.7 ms: 1.03x faster                                                           |
| dulwich_log             | 63.0 ms                                                                | 61.2 ms: 1.03x faster                                                           |
| scimark_sor             | 109 ms                                                                 | 106 ms: 1.03x faster                                                            |
| sympy_expand            | 462 ms                                                                 | 449 ms: 1.03x faster                                                            |
| deepcopy                | 334 us                                                                 | 325 us: 1.03x faster                                                            |
| json_dumps              | 9.63 ms                                                                | 9.37 ms: 1.03x faster                                                           |
| sympy_sum               | 160 ms                                                                 | 155 ms: 1.03x faster                                                            |
| deepcopy_reduce         | 2.97 us                                                                | 2.90 us: 1.03x faster                                                           |
| sympy_integrate         | 20.0 ms                                                                | 19.5 ms: 1.03x faster                                                           |
| scimark_fft             | 312 ms                                                                 | 305 ms: 1.02x faster                                                            |
| pprint_pformat          | 1.41 sec                                                               | 1.38 sec: 1.02x faster                                                          |
| chaos                   | 66.0 ms                                                                | 64.5 ms: 1.02x faster                                                           |
| sqlalchemy_imperative   | 18.0 ms                                                                | 17.6 ms: 1.02x faster                                                           |
| tornado_http            | 95.5 ms                                                                | 93.3 ms: 1.02x faster                                                           |
| docutils                | 2.56 sec                                                               | 2.50 sec: 1.02x faster                                                          |
| hexiom                  | 6.12 ms                                                                | 5.99 ms: 1.02x faster                                                           |
| pickle_pure_python      | 285 us                                                                 | 279 us: 1.02x faster                                                            |
| sqlglot_parse           | 1.44 ms                                                                | 1.41 ms: 1.02x faster                                                           |
| sqlglot_transpile       | 1.73 ms                                                                | 1.69 ms: 1.02x faster                                                           |
| async_tree_io           | 1.32 sec                                                               | 1.29 sec: 1.02x faster                                                          |
| sqlglot_normalize       | 105 ms                                                                 | 103 ms: 1.02x faster                                                            |
| pprint_safe_repr        | 684 ms                                                                 | 671 ms: 1.02x faster                                                            |
| gunicorn                | 1.08 ms                                                                | 1.06 ms: 1.02x faster                                                           |
| mypy2                   | 331 ms                                                                 | 325 ms: 1.02x faster                                                            |
| async_tree_none         | 527 ms                                                                 | 518 ms: 1.02x faster                                                            |
| unpickle_pure_python    | 197 us                                                                 | 193 us: 1.02x faster                                                            |
| bench_thread_pool       | 792 us                                                                 | 779 us: 1.02x faster                                                            |
| go                      | 135 ms                                                                 | 133 ms: 1.02x faster                                                            |
| asyncio_tcp             | 510 ms                                                                 | 501 ms: 1.02x faster                                                            |
| sqlalchemy_declarative  | 137 ms                                                                 | 135 ms: 1.02x faster                                                            |
| sqlglot_optimize        | 51.4 ms                                                                | 50.6 ms: 1.02x faster                                                           |
| sqlite_synth            | 2.63 us                                                                | 2.59 us: 1.02x faster                                                           |
| richards                | 42.6 ms                                                                | 41.9 ms: 1.02x faster                                                           |
| async_tree_cpu_io_mixed | 762 ms                                                                 | 750 ms: 1.02x faster                                                            |
| xml_etree_process       | 55.8 ms                                                                | 55.0 ms: 1.02x faster                                                           |
| float                   | 73.4 ms                                                                | 72.4 ms: 1.01x faster                                                           |
| nbody                   | 93.6 ms                                                                | 92.4 ms: 1.01x faster                                                           |
| xml_etree_generate      | 81.2 ms                                                                | 80.3 ms: 1.01x faster                                                           |
| django_template         | 33.5 ms                                                                | 33.1 ms: 1.01x faster                                                           |
| thrift                  | 769 us                                                                 | 761 us: 1.01x faster                                                            |
| chameleon               | 6.39 ms                                                                | 6.33 ms: 1.01x faster                                                           |
| scimark_lu              | 109 ms                                                                 | 108 ms: 1.01x faster                                                            |
| 2to3                    | 246 ms                                                                 | 244 ms: 1.01x faster                                                            |
| aiohttp                 | 1.01 ms                                                                | 1000 us: 1.01x faster                                                           |
| unpack_sequence         | 42.7 ns                                                                | 42.4 ns: 1.01x faster                                                           |
| mako                    | 9.83 ms                                                                | 9.76 ms: 1.01x faster                                                           |
| logging_simple          | 5.76 us                                                                | 5.72 us: 1.01x faster                                                           |
| xml_etree_parse         | 148 ms                                                                 | 148 ms: 1.00x faster                                                            |
| create_gc_cycles        | 1.48 ms                                                                | 1.48 ms: 1.00x faster                                                           |
| python_startup_no_site  | 6.51 ms                                                                | 6.52 ms: 1.00x slower                                                           |
| json_loads              | 23.6 us                                                                | 23.7 us: 1.00x slower                                                           |
| telco                   | 6.34 ms                                                                | 6.38 ms: 1.01x slower                                                           |
| pathlib                 | 18.0 ms                                                                | 18.2 ms: 1.01x slower                                                           |
| scimark_sparse_mat_mult | 4.13 ms                                                                | 4.20 ms: 1.02x slower                                                           |
| async_generators        | 415 ms                                                                 | 422 ms: 1.02x slower                                                            |
| pickle                  | 10.1 us                                                                | 10.3 us: 1.02x slower                                                           |
| logging_silent          | 91.7 ns                                                                | 93.8 ns: 1.02x slower                                                           |
| pycparser               | 1.10 sec                                                               | 1.13 sec: 1.02x slower                                                          |
| pickle_dict             | 30.0 us                                                                | 30.8 us: 1.03x slower                                                           |
| regex_v8                | 21.8 ms                                                                | 22.5 ms: 1.03x slower                                                           |
| pickle_list             | 4.09 us                                                                | 4.25 us: 1.04x slower                                                           |
| regex_effbot            | 3.49 ms                                                                | 3.65 ms: 1.04x slower                                                           |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (15): unpickle, coverage, scimark_monte_carlo, json, generators, djangocms, unpickle_list, pyflate, async_tree_memoization, python_startup, bench_mp_pool, pidigits, logging_format, fannkuch, xml_etree_iterparse
