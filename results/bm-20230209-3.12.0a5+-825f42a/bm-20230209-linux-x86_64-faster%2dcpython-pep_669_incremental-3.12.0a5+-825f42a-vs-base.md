
# Results vs. base

- fork: faster-cpython
- ref: pep_669_incremental
- machine: linux-x86_64
- commit hash: 825f42a
- commit date: 2023-02-09
- overall geometric mean: 1.01x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 246 ms: 1.02x faster                                                            |
| chameleon      | 6.40 ms                                                                | 6.23 ms: 1.03x faster                                                           |
| docutils       | 2.52 sec                                                               | 2.49 sec: 1.01x faster                                                          |
| html5lib       | 60.8 ms                                                                | 58.7 ms: 1.04x faster                                                           |
| tornado_http   | 94.2 ms                                                                | 92.8 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 94.2 ms                                                                | 90.7 ms: 1.04x faster                                                           |
| float          | 72.5 ms                                                                | 71.4 ms: 1.02x faster                                                           |
| pidigits       | 189 ms                                                                 | 192 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 219 ms                                                                 | 201 ms: 1.09x faster                                                            |
| regex_compile  | 127 ms                                                                 | 124 ms: 1.03x faster                                                            |
| regex_v8       | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                           |
| regex_effbot   | 3.45 ms                                                                | 3.57 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_dict          | 31.6 us                                                                | 29.4 us: 1.08x faster                                                           |
| unpickle_pure_python | 198 us                                                                 | 194 us: 1.02x faster                                                            |
| pickle               | 10.2 us                                                                | 10.0 us: 1.02x faster                                                           |
| pickle_pure_python   | 283 us                                                                 | 279 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 102 ms                                                                 | 100 ms: 1.01x faster                                                            |
| json_loads           | 23.9 us                                                                | 23.7 us: 1.01x faster                                                           |
| xml_etree_generate   | 80.1 ms                                                                | 79.6 ms: 1.01x faster                                                           |
| pickle_list          | 3.97 us                                                                | 4.04 us: 1.02x slower                                                           |
| unpickle             | 13.1 us                                                                | 13.5 us: 1.03x slower                                                           |
| unpickle_list        | 4.98 us                                                                | 5.15 us: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (3): xml_etree_process, json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.91 ms                                                                | 8.94 ms: 1.00x slower                                                           |
| python_startup_no_site | 6.47 ms                                                                | 6.50 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| django_template | 33.1 ms                                                                | 32.2 ms: 1.03x faster                                                           |
| genshi_xml      | 46.8 ms                                                                | 45.5 ms: 1.03x faster                                                           |
| genshi_text     | 20.8 ms                                                                | 20.5 ms: 1.02x faster                                                           |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5+-feec49c | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators              | 79.4 ms                                                                | 54.8 ms: 1.45x faster                                                           |
| regex_dna               | 219 ms                                                                 | 201 ms: 1.09x faster                                                            |
| pickle_dict             | 31.6 us                                                                | 29.4 us: 1.08x faster                                                           |
| scimark_lu              | 108 ms                                                                 | 103 ms: 1.05x faster                                                            |
| sqlglot_normalize       | 107 ms                                                                 | 102 ms: 1.05x faster                                                            |
| sqlalchemy_imperative   | 18.0 ms                                                                | 17.3 ms: 1.04x faster                                                           |
| nbody                   | 94.2 ms                                                                | 90.7 ms: 1.04x faster                                                           |
| go                      | 133 ms                                                                 | 129 ms: 1.04x faster                                                            |
| html5lib                | 60.8 ms                                                                | 58.7 ms: 1.04x faster                                                           |
| nqueens                 | 78.2 ms                                                                | 75.5 ms: 1.04x faster                                                           |
| sqlglot_optimize        | 51.4 ms                                                                | 49.8 ms: 1.03x faster                                                           |
| chaos                   | 64.5 ms                                                                | 62.6 ms: 1.03x faster                                                           |
| hexiom                  | 5.96 ms                                                                | 5.79 ms: 1.03x faster                                                           |
| django_template         | 33.1 ms                                                                | 32.2 ms: 1.03x faster                                                           |
| scimark_sor             | 105 ms                                                                 | 102 ms: 1.03x faster                                                            |
| logging_simple          | 5.81 us                                                                | 5.65 us: 1.03x faster                                                           |
| deltablue               | 3.20 ms                                                                | 3.11 ms: 1.03x faster                                                           |
| regex_compile           | 127 ms                                                                 | 124 ms: 1.03x faster                                                            |
| raytrace                | 283 ms                                                                 | 276 ms: 1.03x faster                                                            |
| genshi_xml              | 46.8 ms                                                                | 45.5 ms: 1.03x faster                                                           |
| chameleon               | 6.40 ms                                                                | 6.23 ms: 1.03x faster                                                           |
| sympy_expand            | 457 ms                                                                 | 446 ms: 1.03x faster                                                            |
| deepcopy                | 329 us                                                                 | 321 us: 1.02x faster                                                            |
| deepcopy_reduce         | 2.93 us                                                                | 2.86 us: 1.02x faster                                                           |
| gunicorn                | 1.08 ms                                                                | 1.05 ms: 1.02x faster                                                           |
| async_generators        | 430 ms                                                                 | 420 ms: 1.02x faster                                                            |
| sqlalchemy_declarative  | 137 ms                                                                 | 134 ms: 1.02x faster                                                            |
| unpickle_pure_python    | 198 us                                                                 | 194 us: 1.02x faster                                                            |
| pprint_safe_repr        | 683 ms                                                                 | 668 ms: 1.02x faster                                                            |
| mypy2                   | 329 ms                                                                 | 322 ms: 1.02x faster                                                            |
| pickle                  | 10.2 us                                                                | 10.0 us: 1.02x faster                                                           |
| sympy_sum               | 158 ms                                                                 | 155 ms: 1.02x faster                                                            |
| deepcopy_memo           | 34.0 us                                                                | 33.3 us: 1.02x faster                                                           |
| logging_format          | 6.39 us                                                                | 6.26 us: 1.02x faster                                                           |
| meteor_contest          | 105 ms                                                                 | 103 ms: 1.02x faster                                                            |
| json                    | 4.65 ms                                                                | 4.56 ms: 1.02x faster                                                           |
| 2to3                    | 250 ms                                                                 | 246 ms: 1.02x faster                                                            |
| pathlib                 | 18.2 ms                                                                | 17.8 ms: 1.02x faster                                                           |
| sympy_str               | 271 ms                                                                 | 265 ms: 1.02x faster                                                            |
| richards                | 42.0 ms                                                                | 41.2 ms: 1.02x faster                                                           |
| sqlglot_transpile       | 1.72 ms                                                                | 1.69 ms: 1.02x faster                                                           |
| dulwich_log             | 62.7 ms                                                                | 61.5 ms: 1.02x faster                                                           |
| aiohttp                 | 1.00 ms                                                                | 983 us: 1.02x faster                                                            |
| async_tree_memoization  | 654 ms                                                                 | 643 ms: 1.02x faster                                                            |
| pprint_pformat          | 1.40 sec                                                               | 1.38 sec: 1.02x faster                                                          |
| scimark_fft             | 304 ms                                                                 | 299 ms: 1.02x faster                                                            |
| pickle_pure_python      | 283 us                                                                 | 279 us: 1.02x faster                                                            |
| sqlite_synth            | 2.62 us                                                                | 2.58 us: 1.02x faster                                                           |
| float                   | 72.5 ms                                                                | 71.4 ms: 1.02x faster                                                           |
| bench_thread_pool       | 783 us                                                                 | 771 us: 1.02x faster                                                            |
| sympy_integrate         | 19.8 ms                                                                | 19.5 ms: 1.02x faster                                                           |
| genshi_text             | 20.8 ms                                                                | 20.5 ms: 1.02x faster                                                           |
| tornado_http            | 94.2 ms                                                                | 92.8 ms: 1.01x faster                                                           |
| sqlglot_parse           | 1.42 ms                                                                | 1.40 ms: 1.01x faster                                                           |
| docutils                | 2.52 sec                                                               | 2.49 sec: 1.01x faster                                                          |
| scimark_monte_carlo     | 64.6 ms                                                                | 63.8 ms: 1.01x faster                                                           |
| xml_etree_iterparse     | 102 ms                                                                 | 100 ms: 1.01x faster                                                            |
| crypto_pyaes            | 72.9 ms                                                                | 72.1 ms: 1.01x faster                                                           |
| pycparser               | 1.09 sec                                                               | 1.08 sec: 1.01x faster                                                          |
| json_loads              | 23.9 us                                                                | 23.7 us: 1.01x faster                                                           |
| xml_etree_generate      | 80.1 ms                                                                | 79.6 ms: 1.01x faster                                                           |
| mdp                     | 2.67 sec                                                               | 2.67 sec: 1.00x slower                                                          |
| create_gc_cycles        | 1.46 ms                                                                | 1.47 ms: 1.00x slower                                                           |
| python_startup          | 8.91 ms                                                                | 8.94 ms: 1.00x slower                                                           |
| python_startup_no_site  | 6.47 ms                                                                | 6.50 ms: 1.00x slower                                                           |
| regex_v8                | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                           |
| asyncio_tcp             | 499 ms                                                                 | 504 ms: 1.01x slower                                                            |
| thrift                  | 753 us                                                                 | 762 us: 1.01x slower                                                            |
| coverage                | 96.5 ms                                                                | 97.7 ms: 1.01x slower                                                           |
| async_tree_none         | 521 ms                                                                 | 529 ms: 1.01x slower                                                            |
| pickle_list             | 3.97 us                                                                | 4.04 us: 1.02x slower                                                           |
| pidigits                | 189 ms                                                                 | 192 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed | 747 ms                                                                 | 767 ms: 1.03x slower                                                            |
| unpickle                | 13.1 us                                                                | 13.5 us: 1.03x slower                                                           |
| async_tree_io           | 1.30 sec                                                               | 1.34 sec: 1.03x slower                                                          |
| pyflate                 | 397 ms                                                                 | 410 ms: 1.03x slower                                                            |
| unpickle_list           | 4.98 us                                                                | 5.15 us: 1.03x slower                                                           |
| regex_effbot            | 3.45 ms                                                                | 3.57 ms: 1.04x slower                                                           |
| coroutines              | 26.2 ms                                                                | 54.8 ms: 2.09x slower                                                           |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (13): djangocms, spectral_norm, unpack_sequence, telco, scimark_sparse_mat_mult, fannkuch, bench_mp_pool, gc_traversal, xml_etree_process, json_dumps, mako, xml_etree_parse, logging_silent
