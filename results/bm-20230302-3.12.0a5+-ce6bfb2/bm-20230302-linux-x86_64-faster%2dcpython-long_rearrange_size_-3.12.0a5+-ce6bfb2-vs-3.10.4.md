
# Results vs. 3.10.4

- fork: faster-cpython
- ref: long_rearrange_size_
- machine: linux-x86_64
- commit hash: ce6bfb2
- commit date: 2023-03-02
- overall geometric mean: 1.29x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 251 ms: 1.33x faster                                                             |
| chameleon      | 8.86 ms                                                | 6.43 ms: 1.38x faster                                                            |
| docutils       | 3.18 sec                                               | 2.55 sec: 1.25x faster                                                           |
| html5lib       | 85.8 ms                                                | 61.8 ms: 1.39x faster                                                            |
| tornado_http   | 128 ms                                                 | 95.0 ms: 1.35x faster                                                            |
| Geometric mean | (ref)                                                  | 1.34x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 136 ms                                                 | 91.6 ms: 1.49x faster                                                            |
| float          | 108 ms                                                 | 74.6 ms: 1.44x faster                                                            |
| pidigits       | 190 ms                                                 | 188 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.29x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 134 ms: 1.29x faster                                                             |
| regex_v8       | 25.0 ms                                                | 21.5 ms: 1.16x faster                                                            |
| regex_dna      | 214 ms                                                 | 219 ms: 1.03x slower                                                             |
| regex_effbot   | 3.21 ms                                                | 3.44 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 285 us: 1.59x faster                                                             |
| unpickle_pure_python | 297 us                                                 | 200 us: 1.48x faster                                                             |
| json_dumps           | 13.5 ms                                                | 9.41 ms: 1.43x faster                                                            |
| xml_etree_process    | 74.5 ms                                                | 55.7 ms: 1.34x faster                                                            |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                                            |
| xml_etree_generate   | 93.3 ms                                                | 80.8 ms: 1.15x faster                                                            |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                                             |
| pickle_list          | 4.50 us                                                | 4.15 us: 1.08x faster                                                            |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.08x faster                                                             |
| unpickle             | 14.3 us                                                | 13.6 us: 1.05x faster                                                            |
| pickle_dict          | 28.3 us                                                | 30.9 us: 1.09x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                                     |

Benchmark hidden because not significant (2): pickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.02 ms: 1.55x faster                                                            |
| python_startup_no_site | 5.76 ms                                                | 6.53 ms: 1.13x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.2 ms: 1.45x faster                                                            |
| mako            | 14.3 ms                                                | 9.86 ms: 1.45x faster                                                            |
| django_template | 46.3 ms                                                | 32.7 ms: 1.41x faster                                                            |
| genshi_xml      | 63.6 ms                                                | 48.2 ms: 1.32x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.41x faster                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 31.0 ms: 2.44x faster                                                            |
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.30x faster                                                            |
| logging_silent          | 173 ns                                                 | 94.3 ns: 1.84x faster                                                            |
| scimark_sor             | 193 ms                                                 | 110 ms: 1.76x faster                                                             |
| go                      | 226 ms                                                 | 136 ms: 1.67x faster                                                             |
| pyflate                 | 675 ms                                                 | 409 ms: 1.65x faster                                                             |
| richards                | 71.4 ms                                                | 43.9 ms: 1.63x faster                                                            |
| raytrace                | 461 ms                                                 | 289 ms: 1.60x faster                                                             |
| pickle_pure_python      | 453 us                                                 | 285 us: 1.59x faster                                                             |
| crypto_pyaes            | 118 ms                                                 | 74.5 ms: 1.58x faster                                                            |
| scimark_monte_carlo     | 105 ms                                                 | 67.1 ms: 1.56x faster                                                            |
| python_startup          | 13.9 ms                                                | 9.02 ms: 1.55x faster                                                            |
| chaos                   | 104 ms                                                 | 67.6 ms: 1.54x faster                                                            |
| hexiom                  | 9.42 ms                                                | 6.21 ms: 1.52x faster                                                            |
| spectral_norm           | 148 ms                                                 | 98.4 ms: 1.50x faster                                                            |
| nbody                   | 136 ms                                                 | 91.6 ms: 1.49x faster                                                            |
| unpickle_pure_python    | 297 us                                                 | 200 us: 1.48x faster                                                             |
| deepcopy_memo           | 50.0 us                                                | 34.4 us: 1.45x faster                                                            |
| genshi_text             | 30.6 ms                                                | 21.2 ms: 1.45x faster                                                            |
| mako                    | 14.3 ms                                                | 9.86 ms: 1.45x faster                                                            |
| float                   | 108 ms                                                 | 74.6 ms: 1.44x faster                                                            |
| json_dumps              | 13.5 ms                                                | 9.41 ms: 1.43x faster                                                            |
| scimark_lu              | 158 ms                                                 | 111 ms: 1.42x faster                                                             |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                                           |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.42x faster                                                            |
| unpack_sequence         | 59.5 ns                                                | 41.9 ns: 1.42x faster                                                            |
| logging_format          | 8.92 us                                                | 6.30 us: 1.42x faster                                                            |
| django_template         | 46.3 ms                                                | 32.7 ms: 1.41x faster                                                            |
| pprint_safe_repr        | 943 ms                                                 | 672 ms: 1.40x faster                                                             |
| sqlglot_transpile       | 2.42 ms                                                | 1.73 ms: 1.40x faster                                                            |
| logging_simple          | 8.06 us                                                | 5.78 us: 1.39x faster                                                            |
| html5lib                | 85.8 ms                                                | 61.8 ms: 1.39x faster                                                            |
| chameleon               | 8.86 ms                                                | 6.43 ms: 1.38x faster                                                            |
| coroutines              | 31.7 ms                                                | 23.1 ms: 1.37x faster                                                            |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.37x faster                                                           |
| async_tree_none         | 713 ms                                                 | 526 ms: 1.36x faster                                                             |
| tornado_http            | 128 ms                                                 | 95.0 ms: 1.35x faster                                                            |
| xml_etree_process       | 74.5 ms                                                | 55.7 ms: 1.34x faster                                                            |
| 2to3                    | 332 ms                                                 | 251 ms: 1.33x faster                                                             |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                                            |
| fannkuch                | 477 ms                                                 | 360 ms: 1.33x faster                                                             |
| pycparser               | 1.51 sec                                               | 1.14 sec: 1.33x faster                                                           |
| thrift                  | 1.03 ms                                                | 781 us: 1.32x faster                                                             |
| genshi_xml              | 63.6 ms                                                | 48.2 ms: 1.32x faster                                                            |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.31x faster                                                            |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                                             |
| deepcopy                | 429 us                                                 | 331 us: 1.30x faster                                                             |
| regex_compile           | 174 ms                                                 | 134 ms: 1.29x faster                                                             |
| async_tree_memoization  | 854 ms                                                 | 661 ms: 1.29x faster                                                             |
| scimark_fft             | 414 ms                                                 | 324 ms: 1.28x faster                                                             |
| async_tree_cpu_io_mixed | 949 ms                                                 | 744 ms: 1.28x faster                                                             |
| sqlglot_optimize        | 65.3 ms                                                | 51.2 ms: 1.28x faster                                                            |
| deepcopy_reduce         | 3.75 us                                                | 3.01 us: 1.25x faster                                                            |
| docutils                | 3.18 sec                                               | 2.55 sec: 1.25x faster                                                           |
| nqueens                 | 99.3 ms                                                | 80.4 ms: 1.23x faster                                                            |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                                            |
| sqlalchemy_declarative  | 165 ms                                                 | 138 ms: 1.20x faster                                                             |
| dulwich_log             | 75.5 ms                                                | 63.8 ms: 1.18x faster                                                            |
| bench_thread_pool       | 943 us                                                 | 800 us: 1.18x faster                                                             |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.9 ms: 1.17x faster                                                            |
| json                    | 5.35 ms                                                | 4.57 ms: 1.17x faster                                                            |
| sympy_expand            | 537 ms                                                 | 460 ms: 1.17x faster                                                             |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.71 ms: 1.16x faster                                                            |
| sympy_integrate         | 23.9 ms                                                | 20.6 ms: 1.16x faster                                                            |
| regex_v8                | 25.0 ms                                                | 21.5 ms: 1.16x faster                                                            |
| xml_etree_generate      | 93.3 ms                                                | 80.8 ms: 1.15x faster                                                            |
| sympy_str               | 324 ms                                                 | 286 ms: 1.13x faster                                                             |
| mdp                     | 2.82 sec                                               | 2.50 sec: 1.13x faster                                                           |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                                            |
| sqlite_synth            | 2.90 us                                                | 2.62 us: 1.11x faster                                                            |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                                             |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.11x faster                                                             |
| sympy_sum               | 183 ms                                                 | 167 ms: 1.10x faster                                                             |
| pickle_list             | 4.50 us                                                | 4.15 us: 1.08x faster                                                            |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.08x faster                                                             |
| unpickle                | 14.3 us                                                | 13.6 us: 1.05x faster                                                            |
| telco                   | 6.68 ms                                                | 6.50 ms: 1.03x faster                                                            |
| async_generators        | 428 ms                                                 | 421 ms: 1.01x faster                                                             |
| pidigits                | 190 ms                                                 | 188 ms: 1.01x faster                                                             |
| regex_dna               | 214 ms                                                 | 219 ms: 1.03x slower                                                             |
| regex_effbot            | 3.21 ms                                                | 3.44 ms: 1.07x slower                                                            |
| pickle_dict             | 28.3 us                                                | 30.9 us: 1.09x slower                                                            |
| python_startup_no_site  | 5.76 ms                                                | 6.53 ms: 1.13x slower                                                            |
| coverage                | 75.3 ms                                                | 95.7 ms: 1.27x slower                                                            |
| Geometric mean          | (ref)                                                  | 1.29x faster                                                                     |

Benchmark hidden because not significant (3): bench_mp_pool, pickle, unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230302-3.12.0a5+-ce6bfb2/bm-20230302-linux-x86_64-faster%2dcpython-long_rearrange_size_-3.12.0a5+-ce6bfb2.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
