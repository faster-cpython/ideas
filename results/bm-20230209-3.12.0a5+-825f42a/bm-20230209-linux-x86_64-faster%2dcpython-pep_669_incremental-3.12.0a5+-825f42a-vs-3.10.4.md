
# Results vs. 3.10.4

- fork: faster-cpython
- ref: pep_669_incremental
- machine: linux-x86_64
- commit hash: 825f42a
- commit date: 2023-02-09
- overall geometric mean: 1.31x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 246 ms: 1.35x faster                                                            |
| chameleon      | 8.86 ms                                                | 6.23 ms: 1.42x faster                                                           |
| docutils       | 3.18 sec                                               | 2.49 sec: 1.28x faster                                                          |
| html5lib       | 85.8 ms                                                | 58.7 ms: 1.46x faster                                                           |
| tornado_http   | 128 ms                                                 | 92.8 ms: 1.38x faster                                                           |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 71.4 ms: 1.51x faster                                                           |
| nbody          | 136 ms                                                 | 90.7 ms: 1.50x faster                                                           |
| pidigits       | 190 ms                                                 | 192 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 124 ms: 1.40x faster                                                            |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.15x faster                                                           |
| regex_dna      | 214 ms                                                 | 201 ms: 1.06x faster                                                            |
| regex_effbot   | 3.21 ms                                                | 3.57 ms: 1.11x slower                                                           |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 279 us: 1.63x faster                                                            |
| unpickle_pure_python | 297 us                                                 | 194 us: 1.53x faster                                                            |
| json_dumps           | 13.5 ms                                                | 9.44 ms: 1.43x faster                                                           |
| xml_etree_process    | 74.5 ms                                                | 55.1 ms: 1.35x faster                                                           |
| json_loads           | 28.9 us                                                | 23.7 us: 1.22x faster                                                           |
| xml_etree_generate   | 93.3 ms                                                | 79.6 ms: 1.17x faster                                                           |
| pickle_list          | 4.50 us                                                | 4.04 us: 1.11x faster                                                           |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                                            |
| xml_etree_iterparse  | 110 ms                                                 | 100 ms: 1.10x faster                                                            |
| unpickle             | 14.3 us                                                | 13.5 us: 1.06x faster                                                           |
| pickle               | 10.1 us                                                | 10.0 us: 1.01x faster                                                           |
| unpickle_list        | 4.99 us                                                | 5.15 us: 1.03x slower                                                           |
| pickle_dict          | 28.3 us                                                | 29.4 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.19x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.94 ms: 1.56x faster                                                           |
| python_startup_no_site | 5.76 ms                                                | 6.50 ms: 1.13x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.5 ms: 1.50x faster                                                           |
| mako            | 14.3 ms                                                | 9.79 ms: 1.46x faster                                                           |
| django_template | 46.3 ms                                                | 32.2 ms: 1.44x faster                                                           |
| genshi_xml      | 63.6 ms                                                | 45.5 ms: 1.40x faster                                                           |
| Geometric mean  | (ref)                                                  | 1.45x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.11 ms: 2.38x faster                                                           |
| scimark_sor             | 193 ms                                                 | 102 ms: 1.89x faster                                                            |
| logging_silent          | 173 ns                                                 | 93.1 ns: 1.86x faster                                                           |
| go                      | 226 ms                                                 | 129 ms: 1.76x faster                                                            |
| richards                | 71.4 ms                                                | 41.2 ms: 1.73x faster                                                           |
| raytrace                | 461 ms                                                 | 276 ms: 1.67x faster                                                            |
| chaos                   | 104 ms                                                 | 62.6 ms: 1.66x faster                                                           |
| pyflate                 | 675 ms                                                 | 410 ms: 1.65x faster                                                            |
| scimark_monte_carlo     | 105 ms                                                 | 63.8 ms: 1.64x faster                                                           |
| crypto_pyaes            | 118 ms                                                 | 72.1 ms: 1.63x faster                                                           |
| hexiom                  | 9.42 ms                                                | 5.79 ms: 1.63x faster                                                           |
| pickle_pure_python      | 453 us                                                 | 279 us: 1.63x faster                                                            |
| spectral_norm           | 148 ms                                                 | 93.3 ms: 1.59x faster                                                           |
| python_startup          | 13.9 ms                                                | 8.94 ms: 1.56x faster                                                           |
| scimark_lu              | 158 ms                                                 | 103 ms: 1.54x faster                                                            |
| unpickle_pure_python    | 297 us                                                 | 194 us: 1.53x faster                                                            |
| float                   | 108 ms                                                 | 71.4 ms: 1.51x faster                                                           |
| nbody                   | 136 ms                                                 | 90.7 ms: 1.50x faster                                                           |
| deepcopy_memo           | 50.0 us                                                | 33.3 us: 1.50x faster                                                           |
| genshi_text             | 30.6 ms                                                | 20.5 ms: 1.50x faster                                                           |
| html5lib                | 85.8 ms                                                | 58.7 ms: 1.46x faster                                                           |
| mako                    | 14.3 ms                                                | 9.79 ms: 1.46x faster                                                           |
| sqlglot_parse           | 2.04 ms                                                | 1.40 ms: 1.45x faster                                                           |
| django_template         | 46.3 ms                                                | 32.2 ms: 1.44x faster                                                           |
| pprint_pformat          | 1.97 sec                                               | 1.38 sec: 1.43x faster                                                          |
| sqlglot_transpile       | 2.42 ms                                                | 1.69 ms: 1.43x faster                                                           |
| json_dumps              | 13.5 ms                                                | 9.44 ms: 1.43x faster                                                           |
| logging_format          | 8.92 us                                                | 6.26 us: 1.43x faster                                                           |
| logging_simple          | 8.06 us                                                | 5.65 us: 1.43x faster                                                           |
| unpack_sequence         | 59.5 ns                                                | 41.8 ns: 1.42x faster                                                           |
| chameleon               | 8.86 ms                                                | 6.23 ms: 1.42x faster                                                           |
| pprint_safe_repr        | 943 ms                                                 | 668 ms: 1.41x faster                                                            |
| regex_compile           | 174 ms                                                 | 124 ms: 1.40x faster                                                            |
| pycparser               | 1.51 sec                                               | 1.08 sec: 1.40x faster                                                          |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.92 ms: 1.40x faster                                                           |
| genshi_xml              | 63.6 ms                                                | 45.5 ms: 1.40x faster                                                           |
| scimark_fft             | 414 ms                                                 | 299 ms: 1.38x faster                                                            |
| generators              | 75.8 ms                                                | 54.8 ms: 1.38x faster                                                           |
| tornado_http            | 128 ms                                                 | 92.8 ms: 1.38x faster                                                           |
| aiohttp                 | 1.34 ms                                                | 983 us: 1.36x faster                                                            |
| gunicorn                | 1.43 ms                                                | 1.05 ms: 1.36x faster                                                           |
| thrift                  | 1.03 ms                                                | 762 us: 1.35x faster                                                            |
| 2to3                    | 332 ms                                                 | 246 ms: 1.35x faster                                                            |
| xml_etree_process       | 74.5 ms                                                | 55.1 ms: 1.35x faster                                                           |
| async_tree_none         | 713 ms                                                 | 529 ms: 1.35x faster                                                            |
| deepcopy                | 429 us                                                 | 321 us: 1.34x faster                                                            |
| async_tree_memoization  | 854 ms                                                 | 643 ms: 1.33x faster                                                            |
| async_tree_io           | 1.78 sec                                               | 1.34 sec: 1.32x faster                                                          |
| sqlglot_normalize       | 135 ms                                                 | 102 ms: 1.32x faster                                                            |
| fannkuch                | 477 ms                                                 | 361 ms: 1.32x faster                                                            |
| nqueens                 | 99.3 ms                                                | 75.5 ms: 1.32x faster                                                           |
| deepcopy_reduce         | 3.75 us                                                | 2.86 us: 1.31x faster                                                           |
| sqlglot_optimize        | 65.3 ms                                                | 49.8 ms: 1.31x faster                                                           |
| docutils                | 3.18 sec                                               | 2.49 sec: 1.28x faster                                                          |
| async_tree_cpu_io_mixed | 949 ms                                                 | 767 ms: 1.24x faster                                                            |
| sqlalchemy_declarative  | 165 ms                                                 | 134 ms: 1.24x faster                                                            |
| sympy_integrate         | 23.9 ms                                                | 19.5 ms: 1.23x faster                                                           |
| dulwich_log             | 75.5 ms                                                | 61.5 ms: 1.23x faster                                                           |
| bench_thread_pool       | 943 us                                                 | 771 us: 1.22x faster                                                            |
| sympy_str               | 324 ms                                                 | 265 ms: 1.22x faster                                                            |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.3 ms: 1.22x faster                                                           |
| json_loads              | 28.9 us                                                | 23.7 us: 1.22x faster                                                           |
| sympy_expand            | 537 ms                                                 | 446 ms: 1.20x faster                                                            |
| sympy_sum               | 183 ms                                                 | 155 ms: 1.19x faster                                                            |
| json                    | 5.35 ms                                                | 4.56 ms: 1.17x faster                                                           |
| xml_etree_generate      | 93.3 ms                                                | 79.6 ms: 1.17x faster                                                           |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.15x faster                                                           |
| sqlite_synth            | 2.90 us                                                | 2.58 us: 1.13x faster                                                           |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.12x faster                                                           |
| pickle_list             | 4.50 us                                                | 4.04 us: 1.11x faster                                                           |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                                            |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                                            |
| xml_etree_iterparse     | 110 ms                                                 | 100 ms: 1.10x faster                                                            |
| regex_dna               | 214 ms                                                 | 201 ms: 1.06x faster                                                            |
| mdp                     | 2.82 sec                                               | 2.67 sec: 1.06x faster                                                          |
| unpickle                | 14.3 us                                                | 13.5 us: 1.06x faster                                                           |
| telco                   | 6.68 ms                                                | 6.35 ms: 1.05x faster                                                           |
| async_generators        | 428 ms                                                 | 420 ms: 1.02x faster                                                            |
| pickle                  | 10.1 us                                                | 10.0 us: 1.01x faster                                                           |
| pidigits                | 190 ms                                                 | 192 ms: 1.01x slower                                                            |
| unpickle_list           | 4.99 us                                                | 5.15 us: 1.03x slower                                                           |
| pickle_dict             | 28.3 us                                                | 29.4 us: 1.04x slower                                                           |
| regex_effbot            | 3.21 ms                                                | 3.57 ms: 1.11x slower                                                           |
| python_startup_no_site  | 5.76 ms                                                | 6.50 ms: 1.13x slower                                                           |
| coverage                | 75.3 ms                                                | 97.7 ms: 1.30x slower                                                           |
| coroutines              | 31.7 ms                                                | 54.8 ms: 1.73x slower                                                           |
| Geometric mean          | (ref)                                                  | 1.31x faster                                                                    |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230209-3.12.0a5+-825f42a/bm-20230209-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-825f42a.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
