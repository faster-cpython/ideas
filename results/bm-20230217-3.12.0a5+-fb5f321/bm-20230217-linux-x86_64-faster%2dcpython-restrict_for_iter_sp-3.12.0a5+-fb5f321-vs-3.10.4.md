
# Results vs. 3.10.4

- fork: faster-cpython
- ref: restrict_for_iter_sp
- machine: linux-x86_64
- commit hash: fb5f321
- commit date: 2023-02-17
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 247 ms: 1.34x faster                                                             |
| chameleon      | 8.86 ms                                                | 6.39 ms: 1.39x faster                                                            |
| docutils       | 3.18 sec                                               | 2.53 sec: 1.26x faster                                                           |
| html5lib       | 85.8 ms                                                | 61.2 ms: 1.40x faster                                                            |
| tornado_http   | 128 ms                                                 | 94.8 ms: 1.35x faster                                                            |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 73.7 ms: 1.46x faster                                                            |
| nbody          | 136 ms                                                 | 95.5 ms: 1.43x faster                                                            |
| pidigits       | 190 ms                                                 | 198 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.26x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 132 ms: 1.31x faster                                                             |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.14x faster                                                            |
| regex_dna      | 214 ms                                                 | 199 ms: 1.08x faster                                                             |
| regex_effbot   | 3.21 ms                                                | 3.65 ms: 1.14x slower                                                            |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 281 us: 1.61x faster                                                             |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.51x faster                                                             |
| json_dumps           | 13.5 ms                                                | 9.50 ms: 1.42x faster                                                            |
| xml_etree_process    | 74.5 ms                                                | 55.7 ms: 1.34x faster                                                            |
| json_loads           | 28.9 us                                                | 24.0 us: 1.20x faster                                                            |
| xml_etree_generate   | 93.3 ms                                                | 81.2 ms: 1.15x faster                                                            |
| pickle_list          | 4.50 us                                                | 4.01 us: 1.12x faster                                                            |
| xml_etree_iterparse  | 110 ms                                                 | 99.7 ms: 1.11x faster                                                            |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                                             |
| unpickle             | 14.3 us                                                | 13.7 us: 1.04x faster                                                            |
| pickle               | 10.1 us                                                | 9.98 us: 1.02x faster                                                            |
| unpickle_list        | 4.99 us                                                | 5.04 us: 1.01x slower                                                            |
| pickle_dict          | 28.3 us                                                | 30.2 us: 1.07x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.92 ms: 1.56x faster                                                            |
| python_startup_no_site | 5.76 ms                                                | 6.47 ms: 1.12x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.2 ms: 1.45x faster                                                            |
| mako            | 14.3 ms                                                | 9.89 ms: 1.44x faster                                                            |
| django_template | 46.3 ms                                                | 33.0 ms: 1.40x faster                                                            |
| genshi_xml      | 63.6 ms                                                | 48.4 ms: 1.31x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.40x faster                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 30.6 ms: 2.48x faster                                                            |
| deltablue               | 7.39 ms                                                | 3.19 ms: 2.32x faster                                                            |
| logging_silent          | 173 ns                                                 | 95.7 ns: 1.81x faster                                                            |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                                             |
| richards                | 71.4 ms                                                | 42.2 ms: 1.69x faster                                                            |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                                             |
| pyflate                 | 675 ms                                                 | 402 ms: 1.68x faster                                                             |
| pickle_pure_python      | 453 us                                                 | 281 us: 1.61x faster                                                             |
| raytrace                | 461 ms                                                 | 290 ms: 1.59x faster                                                             |
| crypto_pyaes            | 118 ms                                                 | 74.2 ms: 1.58x faster                                                            |
| spectral_norm           | 148 ms                                                 | 94.1 ms: 1.57x faster                                                            |
| python_startup          | 13.9 ms                                                | 8.92 ms: 1.56x faster                                                            |
| scimark_monte_carlo     | 105 ms                                                 | 67.1 ms: 1.56x faster                                                            |
| chaos                   | 104 ms                                                 | 68.0 ms: 1.53x faster                                                            |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.51x faster                                                             |
| hexiom                  | 9.42 ms                                                | 6.27 ms: 1.50x faster                                                            |
| float                   | 108 ms                                                 | 73.7 ms: 1.46x faster                                                            |
| genshi_text             | 30.6 ms                                                | 21.2 ms: 1.45x faster                                                            |
| deepcopy_memo           | 50.0 us                                                | 34.6 us: 1.44x faster                                                            |
| mako                    | 14.3 ms                                                | 9.89 ms: 1.44x faster                                                            |
| scimark_lu              | 158 ms                                                 | 110 ms: 1.44x faster                                                             |
| coroutines              | 31.7 ms                                                | 22.1 ms: 1.43x faster                                                            |
| nbody                   | 136 ms                                                 | 95.5 ms: 1.43x faster                                                            |
| unpack_sequence         | 59.5 ns                                                | 41.9 ns: 1.42x faster                                                            |
| json_dumps              | 13.5 ms                                                | 9.50 ms: 1.42x faster                                                            |
| sqlglot_parse           | 2.04 ms                                                | 1.44 ms: 1.41x faster                                                            |
| pprint_pformat          | 1.97 sec                                               | 1.41 sec: 1.40x faster                                                           |
| logging_simple          | 8.06 us                                                | 5.74 us: 1.40x faster                                                            |
| html5lib                | 85.8 ms                                                | 61.2 ms: 1.40x faster                                                            |
| django_template         | 46.3 ms                                                | 33.0 ms: 1.40x faster                                                            |
| logging_format          | 8.92 us                                                | 6.37 us: 1.40x faster                                                            |
| sqlglot_transpile       | 2.42 ms                                                | 1.73 ms: 1.40x faster                                                            |
| pprint_safe_repr        | 943 ms                                                 | 680 ms: 1.39x faster                                                             |
| chameleon               | 8.86 ms                                                | 6.39 ms: 1.39x faster                                                            |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.38x faster                                                           |
| tornado_http            | 128 ms                                                 | 94.8 ms: 1.35x faster                                                            |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.35x faster                                                           |
| async_tree_none         | 713 ms                                                 | 529 ms: 1.35x faster                                                             |
| 2to3                    | 332 ms                                                 | 247 ms: 1.34x faster                                                             |
| thrift                  | 1.03 ms                                                | 769 us: 1.34x faster                                                             |
| xml_etree_process       | 74.5 ms                                                | 55.7 ms: 1.34x faster                                                            |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.32x faster                                                            |
| scimark_fft             | 414 ms                                                 | 314 ms: 1.32x faster                                                             |
| fannkuch                | 477 ms                                                 | 362 ms: 1.32x faster                                                             |
| regex_compile           | 174 ms                                                 | 132 ms: 1.31x faster                                                             |
| genshi_xml              | 63.6 ms                                                | 48.4 ms: 1.31x faster                                                            |
| gunicorn                | 1.43 ms                                                | 1.10 ms: 1.31x faster                                                            |
| deepcopy                | 429 us                                                 | 333 us: 1.29x faster                                                             |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                                             |
| sqlglot_optimize        | 65.3 ms                                                | 51.1 ms: 1.28x faster                                                            |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.28x faster                                                            |
| async_tree_memoization  | 854 ms                                                 | 677 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed | 949 ms                                                 | 752 ms: 1.26x faster                                                             |
| docutils                | 3.18 sec                                               | 2.53 sec: 1.26x faster                                                           |
| nqueens                 | 99.3 ms                                                | 81.7 ms: 1.22x faster                                                            |
| sqlalchemy_declarative  | 165 ms                                                 | 137 ms: 1.21x faster                                                             |
| json_loads              | 28.9 us                                                | 24.0 us: 1.20x faster                                                            |
| dulwich_log             | 75.5 ms                                                | 62.8 ms: 1.20x faster                                                            |
| sympy_integrate         | 23.9 ms                                                | 20.0 ms: 1.20x faster                                                            |
| bench_thread_pool       | 943 us                                                 | 791 us: 1.19x faster                                                             |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.60 ms: 1.19x faster                                                            |
| sympy_str               | 324 ms                                                 | 273 ms: 1.19x faster                                                             |
| sympy_expand            | 537 ms                                                 | 455 ms: 1.18x faster                                                             |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.0 ms: 1.17x faster                                                            |
| json                    | 5.35 ms                                                | 4.60 ms: 1.16x faster                                                            |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                                             |
| xml_etree_generate      | 93.3 ms                                                | 81.2 ms: 1.15x faster                                                            |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.14x faster                                                            |
| pickle_list             | 4.50 us                                                | 4.01 us: 1.12x faster                                                            |
| xml_etree_iterparse     | 110 ms                                                 | 99.7 ms: 1.11x faster                                                            |
| pathlib                 | 20.0 ms                                                | 18.1 ms: 1.10x faster                                                            |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.10x faster                                                             |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                                             |
| sqlite_synth            | 2.90 us                                                | 2.66 us: 1.09x faster                                                            |
| regex_dna               | 214 ms                                                 | 199 ms: 1.08x faster                                                             |
| mdp                     | 2.82 sec                                               | 2.66 sec: 1.06x faster                                                           |
| async_generators        | 428 ms                                                 | 410 ms: 1.04x faster                                                             |
| unpickle                | 14.3 us                                                | 13.7 us: 1.04x faster                                                            |
| pickle                  | 10.1 us                                                | 9.98 us: 1.02x faster                                                            |
| telco                   | 6.68 ms                                                | 6.58 ms: 1.02x faster                                                            |
| unpickle_list           | 4.99 us                                                | 5.04 us: 1.01x slower                                                            |
| pidigits                | 190 ms                                                 | 198 ms: 1.04x slower                                                             |
| pickle_dict             | 28.3 us                                                | 30.2 us: 1.07x slower                                                            |
| python_startup_no_site  | 5.76 ms                                                | 6.47 ms: 1.12x slower                                                            |
| regex_effbot            | 3.21 ms                                                | 3.65 ms: 1.14x slower                                                            |
| coverage                | 75.3 ms                                                | 97.9 ms: 1.30x slower                                                            |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                                     |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230217-3.12.0a5+-fb5f321/bm-20230217-linux-x86_64-faster%2dcpython-restrict_for_iter_sp-3.12.0a5+-fb5f321.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
