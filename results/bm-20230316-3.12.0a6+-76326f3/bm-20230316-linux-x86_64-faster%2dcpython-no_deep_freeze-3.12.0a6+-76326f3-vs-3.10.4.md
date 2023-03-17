
# Results vs. 3.10.4

- fork: faster-cpython
- ref: no_deep_freeze
- machine: linux-x86_64
- commit hash: 76326f3
- commit date: 2023-03-16
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                                       |
| chameleon      | 8.86 ms                                                | 6.36 ms: 1.39x faster                                                      |
| docutils       | 3.18 sec                                               | 2.52 sec: 1.26x faster                                                     |
| html5lib       | 85.8 ms                                                | 59.2 ms: 1.45x faster                                                      |
| tornado_http   | 128 ms                                                 | 90.9 ms: 1.41x faster                                                      |
| Geometric mean | (ref)                                                  | 1.37x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 136 ms                                                 | 88.2 ms: 1.54x faster                                                      |
| float          | 108 ms                                                 | 73.7 ms: 1.46x faster                                                      |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                  | 1.31x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 133 ms: 1.31x faster                                                       |
| regex_dna      | 214 ms                                                 | 204 ms: 1.05x faster                                                       |
| regex_v8       | 25.0 ms                                                | 25.6 ms: 1.02x slower                                                      |
| regex_effbot   | 3.21 ms                                                | 3.45 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                  | 1.06x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 282 us: 1.61x faster                                                       |
| unpickle_pure_python | 297 us                                                 | 199 us: 1.49x faster                                                       |
| json_dumps           | 13.5 ms                                                | 9.62 ms: 1.40x faster                                                      |
| xml_etree_process    | 74.5 ms                                                | 56.4 ms: 1.32x faster                                                      |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                                      |
| xml_etree_generate   | 93.3 ms                                                | 81.8 ms: 1.14x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                 | 99.7 ms: 1.11x faster                                                      |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                                       |
| pickle_list          | 4.50 us                                                | 4.21 us: 1.07x faster                                                      |
| pickle               | 10.1 us                                                | 10.2 us: 1.01x slower                                                      |
| pickle_dict          | 28.3 us                                                | 30.0 us: 1.06x slower                                                      |
| unpickle_list        | 4.99 us                                                | 5.32 us: 1.07x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                               |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.51 ms: 1.46x faster                                                      |
| python_startup_no_site | 5.76 ms                                                | 6.48 ms: 1.12x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.14x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.2 ms: 1.45x faster                                                      |
| mako            | 14.3 ms                                                | 10.2 ms: 1.40x faster                                                      |
| django_template | 46.3 ms                                                | 33.1 ms: 1.40x faster                                                      |
| genshi_xml      | 63.6 ms                                                | 47.7 ms: 1.33x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.9 ms: 2.53x faster                                                      |
| deltablue               | 7.39 ms                                                | 3.15 ms: 2.35x faster                                                      |
| logging_silent          | 173 ns                                                 | 93.4 ns: 1.85x faster                                                      |
| scimark_sor             | 193 ms                                                 | 106 ms: 1.83x faster                                                       |
| go                      | 226 ms                                                 | 132 ms: 1.71x faster                                                       |
| richards                | 71.4 ms                                                | 42.6 ms: 1.67x faster                                                      |
| raytrace                | 461 ms                                                 | 282 ms: 1.64x faster                                                       |
| spectral_norm           | 148 ms                                                 | 90.6 ms: 1.63x faster                                                      |
| pickle_pure_python      | 453 us                                                 | 282 us: 1.61x faster                                                       |
| pyflate                 | 675 ms                                                 | 423 ms: 1.60x faster                                                       |
| crypto_pyaes            | 118 ms                                                 | 74.4 ms: 1.58x faster                                                      |
| scimark_monte_carlo     | 105 ms                                                 | 67.0 ms: 1.56x faster                                                      |
| chaos                   | 104 ms                                                 | 66.7 ms: 1.56x faster                                                      |
| nbody                   | 136 ms                                                 | 88.2 ms: 1.54x faster                                                      |
| hexiom                  | 9.42 ms                                                | 6.10 ms: 1.54x faster                                                      |
| unpickle_pure_python    | 297 us                                                 | 199 us: 1.49x faster                                                       |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.49x faster                                                       |
| deepcopy_memo           | 50.0 us                                                | 33.7 us: 1.49x faster                                                      |
| python_startup          | 13.9 ms                                                | 9.51 ms: 1.46x faster                                                      |
| float                   | 108 ms                                                 | 73.7 ms: 1.46x faster                                                      |
| html5lib                | 85.8 ms                                                | 59.2 ms: 1.45x faster                                                      |
| genshi_text             | 30.6 ms                                                | 21.2 ms: 1.45x faster                                                      |
| sqlglot_parse           | 2.04 ms                                                | 1.42 ms: 1.43x faster                                                      |
| coroutines              | 31.7 ms                                                | 22.2 ms: 1.42x faster                                                      |
| logging_simple          | 8.06 us                                                | 5.69 us: 1.42x faster                                                      |
| sqlglot_transpile       | 2.42 ms                                                | 1.71 ms: 1.41x faster                                                      |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                                     |
| tornado_http            | 128 ms                                                 | 90.9 ms: 1.41x faster                                                      |
| async_tree_memoization  | 854 ms                                                 | 606 ms: 1.41x faster                                                       |
| logging_format          | 8.92 us                                                | 6.34 us: 1.41x faster                                                      |
| json_dumps              | 13.5 ms                                                | 9.62 ms: 1.40x faster                                                      |
| mako                    | 14.3 ms                                                | 10.2 ms: 1.40x faster                                                      |
| django_template         | 46.3 ms                                                | 33.1 ms: 1.40x faster                                                      |
| chameleon               | 8.86 ms                                                | 6.36 ms: 1.39x faster                                                      |
| unpack_sequence         | 59.5 ns                                                | 42.8 ns: 1.39x faster                                                      |
| pprint_safe_repr        | 943 ms                                                 | 687 ms: 1.37x faster                                                       |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.36x faster                                                     |
| scimark_fft             | 414 ms                                                 | 304 ms: 1.36x faster                                                       |
| aiohttp                 | 1.34 ms                                                | 996 us: 1.34x faster                                                       |
| thrift                  | 1.03 ms                                                | 772 us: 1.34x faster                                                       |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                                      |
| genshi_xml              | 63.6 ms                                                | 47.7 ms: 1.33x faster                                                      |
| async_tree_none         | 713 ms                                                 | 535 ms: 1.33x faster                                                       |
| xml_etree_process       | 74.5 ms                                                | 56.4 ms: 1.32x faster                                                      |
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                                       |
| regex_compile           | 174 ms                                                 | 133 ms: 1.31x faster                                                       |
| deepcopy                | 429 us                                                 | 328 us: 1.31x faster                                                       |
| pycparser               | 1.51 sec                                               | 1.17 sec: 1.29x faster                                                     |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.29x faster                                                       |
| fannkuch                | 477 ms                                                 | 371 ms: 1.28x faster                                                       |
| sqlglot_optimize        | 65.3 ms                                                | 51.4 ms: 1.27x faster                                                      |
| deepcopy_reduce         | 3.75 us                                                | 2.96 us: 1.27x faster                                                      |
| docutils                | 3.18 sec                                               | 2.52 sec: 1.26x faster                                                     |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.37 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed | 949 ms                                                 | 770 ms: 1.23x faster                                                       |
| nqueens                 | 99.3 ms                                                | 81.1 ms: 1.22x faster                                                      |
| sqlalchemy_declarative  | 165 ms                                                 | 136 ms: 1.22x faster                                                       |
| dulwich_log             | 75.5 ms                                                | 62.3 ms: 1.21x faster                                                      |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                                      |
| bench_thread_pool       | 943 us                                                 | 791 us: 1.19x faster                                                       |
| json                    | 5.35 ms                                                | 4.54 ms: 1.18x faster                                                      |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.8 ms: 1.18x faster                                                      |
| mdp                     | 2.82 sec                                               | 2.40 sec: 1.18x faster                                                     |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                                      |
| sympy_expand            | 537 ms                                                 | 464 ms: 1.16x faster                                                       |
| sympy_str               | 324 ms                                                 | 284 ms: 1.14x faster                                                       |
| xml_etree_generate      | 93.3 ms                                                | 81.8 ms: 1.14x faster                                                      |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.12x faster                                                      |
| xml_etree_iterparse     | 110 ms                                                 | 99.7 ms: 1.11x faster                                                      |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                                       |
| sympy_sum               | 183 ms                                                 | 166 ms: 1.11x faster                                                       |
| sqlite_synth            | 2.90 us                                                | 2.65 us: 1.10x faster                                                      |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.10x faster                                                       |
| pickle_list             | 4.50 us                                                | 4.21 us: 1.07x faster                                                      |
| regex_dna               | 214 ms                                                 | 204 ms: 1.05x faster                                                       |
| async_generators        | 428 ms                                                 | 411 ms: 1.04x faster                                                       |
| telco                   | 6.68 ms                                                | 6.56 ms: 1.02x faster                                                      |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                                       |
| pickle                  | 10.1 us                                                | 10.2 us: 1.01x slower                                                      |
| regex_v8                | 25.0 ms                                                | 25.6 ms: 1.02x slower                                                      |
| pickle_dict             | 28.3 us                                                | 30.0 us: 1.06x slower                                                      |
| unpickle_list           | 4.99 us                                                | 5.32 us: 1.07x slower                                                      |
| regex_effbot            | 3.21 ms                                                | 3.45 ms: 1.07x slower                                                      |
| python_startup_no_site  | 5.76 ms                                                | 6.48 ms: 1.12x slower                                                      |
| coverage                | 75.3 ms                                                | 91.6 ms: 1.22x slower                                                      |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                               |

Benchmark hidden because not significant (2): bench_mp_pool, unpickle
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230316-3.12.0a6+-76326f3/bm-20230316-linux-x86_64-faster%2dcpython-no_deep_freeze-3.12.0a6+-76326f3.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
