
# Results vs. 3.10.4

- fork: faster_cpython
- ref: nogil
- machine: linux-x86_64
- commit hash: 258cab1
- commit date: 2022-12-21
- overall geometric mean: 1.00x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 382 ms: 1.15x slower                                         |
| chameleon      | 8.86 ms                                                | 8.20 ms: 1.08x faster                                        |
| docutils       | 3.18 sec                                               | 5.20 sec: 1.63x slower                                       |
| html5lib       | 85.8 ms                                                | 81.7 ms: 1.05x faster                                        |
| tornado_http   | 128 ms                                                 | 124 ms: 1.03x faster                                         |
| Geometric mean | (ref)                                                  | 1.10x slower                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 108 ms                                                 | 104 ms: 1.03x faster                                         |
| nbody          | 136 ms                                                 | 172 ms: 1.26x slower                                         |
| pidigits       | 190 ms                                                 | 186 ms: 1.02x faster                                         |
| Geometric mean | (ref)                                                  | 1.06x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 186 ms: 1.07x slower                                         |
| regex_dna      | 214 ms                                                 | 218 ms: 1.02x slower                                         |
| regex_effbot   | 3.21 ms                                                | 3.35 ms: 1.04x slower                                        |
| regex_v8       | 25.0 ms                                                | 24.1 ms: 1.03x faster                                        |
| Geometric mean | (ref)                                                  | 1.02x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| json_loads           | 28.9 us                                                | 32.5 us: 1.12x slower                                        |
| pickle               | 10.1 us                                                | 10.0 us: 1.01x faster                                        |
| pickle_dict          | 28.3 us                                                | 25.3 us: 1.12x faster                                        |
| pickle_list          | 4.50 us                                                | 4.17 us: 1.08x faster                                        |
| pickle_pure_python   | 453 us                                                 | 346 us: 1.31x faster                                         |
| unpickle             | 14.3 us                                                | 18.6 us: 1.30x slower                                        |
| unpickle_list        | 4.99 us                                                | 5.80 us: 1.16x slower                                        |
| unpickle_pure_python | 297 us                                                 | 262 us: 1.13x faster                                         |
| xml_etree_parse      | 163 ms                                                 | 149 ms: 1.09x faster                                         |
| xml_etree_iterparse  | 110 ms                                                 | 95.5 ms: 1.16x faster                                        |
| xml_etree_generate   | 93.3 ms                                                | 87.8 ms: 1.06x faster                                        |
| xml_etree_process    | 74.5 ms                                                | 71.4 ms: 1.04x faster                                        |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.41 ms: 1.48x faster                                        |
| python_startup_no_site | 5.76 ms                                                | 5.91 ms: 1.03x slower                                        |
| Geometric mean         | (ref)                                                  | 1.20x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 46.3 ms                                                | 42.6 ms: 1.09x faster                                        |
| genshi_text     | 30.6 ms                                                | 52.1 ms: 1.70x slower                                        |
| genshi_xml      | 63.6 ms                                                | 73.6 ms: 1.16x slower                                        |
| mako            | 14.3 ms                                                | 16.4 ms: 1.15x slower                                        |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                 |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 382 ms: 1.15x slower                                         |
| aiohttp                 | 1.34 ms                                                | 1.44 ms: 1.07x slower                                        |
| async_generators        | 428 ms                                                 | 626 ms: 1.47x slower                                         |
| async_tree_none         | 713 ms                                                 | 372 ms: 1.91x faster                                         |
| async_tree_cpu_io_mixed | 949 ms                                                 | 614 ms: 1.55x faster                                         |
| async_tree_io           | 1.78 sec                                               | 829 ms: 2.14x faster                                         |
| async_tree_memoization  | 854 ms                                                 | 460 ms: 1.86x faster                                         |
| chameleon               | 8.86 ms                                                | 8.20 ms: 1.08x faster                                        |
| chaos                   | 104 ms                                                 | 102 ms: 1.02x faster                                         |
| bench_mp_pool           | 24.0 ms                                                | 23.8 ms: 1.01x faster                                        |
| bench_thread_pool       | 943 us                                                 | 1.19 ms: 1.26x slower                                        |
| coroutines              | 31.7 ms                                                | 72.5 ms: 2.29x slower                                        |
| coverage                | 75.3 ms                                                | 553 ms: 7.34x slower                                         |
| crypto_pyaes            | 118 ms                                                 | 122 ms: 1.04x slower                                         |
| deepcopy                | 429 us                                                 | 393 us: 1.09x faster                                         |
| deepcopy_reduce         | 3.75 us                                                | 3.63 us: 1.03x faster                                        |
| deepcopy_memo           | 50.0 us                                                | 40.1 us: 1.25x faster                                        |
| deltablue               | 7.39 ms                                                | 5.41 ms: 1.37x faster                                        |
| django_template         | 46.3 ms                                                | 42.6 ms: 1.09x faster                                        |
| docutils                | 3.18 sec                                               | 5.20 sec: 1.63x slower                                       |
| dulwich_log             | 75.5 ms                                                | 77.0 ms: 1.02x slower                                        |
| fannkuch                | 477 ms                                                 | 490 ms: 1.03x slower                                         |
| flaskblogging           | 8.38 ms                                                | 12.1 ms: 1.45x slower                                        |
| float                   | 108 ms                                                 | 104 ms: 1.03x faster                                         |
| generators              | 75.8 ms                                                | 81.6 ms: 1.08x slower                                        |
| genshi_text             | 30.6 ms                                                | 52.1 ms: 1.70x slower                                        |
| genshi_xml              | 63.6 ms                                                | 73.6 ms: 1.16x slower                                        |
| go                      | 226 ms                                                 | 159 ms: 1.42x faster                                         |
| gunicorn                | 1.43 ms                                                | 1.52 ms: 1.06x slower                                        |
| hexiom                  | 9.42 ms                                                | 7.74 ms: 1.22x faster                                        |
| html5lib                | 85.8 ms                                                | 81.7 ms: 1.05x faster                                        |
| json_loads              | 28.9 us                                                | 32.5 us: 1.12x slower                                        |
| logging_format          | 8.92 us                                                | 7.69 us: 1.16x faster                                        |
| logging_silent          | 173 ns                                                 | 96.0 ns: 1.80x faster                                        |
| logging_simple          | 8.06 us                                                | 6.95 us: 1.16x faster                                        |
| mako                    | 14.3 ms                                                | 16.4 ms: 1.15x slower                                        |
| mdp                     | 2.82 sec                                               | 3.10 sec: 1.10x slower                                       |
| meteor_contest          | 114 ms                                                 | 127 ms: 1.12x slower                                         |
| mypy                    | 1.01 sec                                               | 1.13 sec: 1.11x slower                                       |
| nbody                   | 136 ms                                                 | 172 ms: 1.26x slower                                         |
| nqueens                 | 99.3 ms                                                | 109 ms: 1.10x slower                                         |
| pathlib                 | 20.0 ms                                                | 20.6 ms: 1.03x slower                                        |
| pickle                  | 10.1 us                                                | 10.0 us: 1.01x faster                                        |
| pickle_dict             | 28.3 us                                                | 25.3 us: 1.12x faster                                        |
| pickle_list             | 4.50 us                                                | 4.17 us: 1.08x faster                                        |
| pickle_pure_python      | 453 us                                                 | 346 us: 1.31x faster                                         |
| pidigits                | 190 ms                                                 | 186 ms: 1.02x faster                                         |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                       |
| pycparser               | 1.51 sec                                               | 1.35 sec: 1.12x faster                                       |
| pyflate                 | 675 ms                                                 | 636 ms: 1.06x faster                                         |
| pylint                  | 519 ms                                                 | 626 ms: 1.21x slower                                         |
| python_startup          | 13.9 ms                                                | 9.41 ms: 1.48x faster                                        |
| python_startup_no_site  | 5.76 ms                                                | 5.91 ms: 1.03x slower                                        |
| raytrace                | 461 ms                                                 | 416 ms: 1.11x faster                                         |
| regex_compile           | 174 ms                                                 | 186 ms: 1.07x slower                                         |
| regex_dna               | 214 ms                                                 | 218 ms: 1.02x slower                                         |
| regex_effbot            | 3.21 ms                                                | 3.35 ms: 1.04x slower                                        |
| regex_v8                | 25.0 ms                                                | 24.1 ms: 1.03x faster                                        |
| richards                | 71.4 ms                                                | 39.3 ms: 1.81x faster                                        |
| scimark_fft             | 414 ms                                                 | 430 ms: 1.04x slower                                         |
| scimark_lu              | 158 ms                                                 | 149 ms: 1.06x faster                                         |
| scimark_monte_carlo     | 105 ms                                                 | 101 ms: 1.04x faster                                         |
| scimark_sor             | 193 ms                                                 | 144 ms: 1.34x faster                                         |
| scimark_sparse_mat_mult | 5.48 ms                                                | 6.09 ms: 1.11x slower                                        |
| spectral_norm           | 148 ms                                                 | 143 ms: 1.04x faster                                         |
| sqlglot_parse           | 2.04 ms                                                | 2.18 ms: 1.07x slower                                        |
| sqlglot_transpile       | 2.42 ms                                                | 2.55 ms: 1.06x slower                                        |
| sqlglot_optimize        | 65.3 ms                                                | 69.3 ms: 1.06x slower                                        |
| sqlglot_normalize       | 135 ms                                                 | 144 ms: 1.07x slower                                         |
| sqlite_synth            | 2.90 us                                                | 3.24 us: 1.12x slower                                        |
| sympy_integrate         | 23.9 ms                                                | 25.4 ms: 1.06x slower                                        |
| sympy_sum               | 183 ms                                                 | 212 ms: 1.15x slower                                         |
| sympy_str               | 324 ms                                                 | 335 ms: 1.03x slower                                         |
| telco                   | 6.68 ms                                                | 7.15 ms: 1.07x slower                                        |
| thrift                  | 1.03 ms                                                | 992 us: 1.04x faster                                         |
| tornado_http            | 128 ms                                                 | 124 ms: 1.03x faster                                         |
| unpack_sequence         | 59.5 ns                                                | 52.4 ns: 1.13x faster                                        |
| unpickle                | 14.3 us                                                | 18.6 us: 1.30x slower                                        |
| unpickle_list           | 4.99 us                                                | 5.80 us: 1.16x slower                                        |
| unpickle_pure_python    | 297 us                                                 | 262 us: 1.13x faster                                         |
| xml_etree_parse         | 163 ms                                                 | 149 ms: 1.09x faster                                         |
| xml_etree_iterparse     | 110 ms                                                 | 95.5 ms: 1.16x faster                                        |
| xml_etree_generate      | 93.3 ms                                                | 87.8 ms: 1.06x faster                                        |
| xml_etree_process       | 74.5 ms                                                | 71.4 ms: 1.04x faster                                        |
| Geometric mean          | (ref)                                                  | 1.00x faster                                                 |

Benchmark hidden because not significant (3): json, json_dumps, sympy_expand
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: pprint_safe_repr, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of public/results/bm-20221221-3.9.10-258cab1/bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1.json: djangocms
