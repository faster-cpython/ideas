
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: eff9f43
- commit date: 2023-03-04
- overall geometric mean: 1.29x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| chameleon      | 8.86 ms                                                | 6.42 ms: 1.38x faster                                  |
| docutils       | 3.18 sec                                               | 2.56 sec: 1.24x faster                                 |
| html5lib       | 85.8 ms                                                | 61.4 ms: 1.40x faster                                  |
| tornado_http   | 128 ms                                                 | 94.9 ms: 1.35x faster                                  |
| Geometric mean | (ref)                                                  | 1.34x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 136 ms                                                 | 94.0 ms: 1.45x faster                                  |
| float          | 108 ms                                                 | 74.6 ms: 1.44x faster                                  |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 133 ms: 1.30x faster                                   |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.14x faster                                  |
| regex_dna      | 214 ms                                                 | 209 ms: 1.02x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.40 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 291 us: 1.56x faster                                   |
| unpickle_pure_python | 297 us                                                 | 199 us: 1.49x faster                                   |
| json_dumps           | 13.5 ms                                                | 9.56 ms: 1.41x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 55.4 ms: 1.34x faster                                  |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 81.3 ms: 1.15x faster                                  |
| pickle_list          | 4.50 us                                                | 4.05 us: 1.11x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| unpickle             | 14.3 us                                                | 13.7 us: 1.04x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.22 us: 1.04x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.5 us: 1.11x slower                                  |
| Geometric mean       | (ref)                                                  | 1.16x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.03 ms: 1.54x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.55 ms: 1.14x slower                                  |
| Geometric mean         | (ref)                                                  | 1.16x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.2 ms: 1.44x faster                                  |
| mako            | 14.3 ms                                                | 10.1 ms: 1.42x faster                                  |
| django_template | 46.3 ms                                                | 33.2 ms: 1.39x faster                                  |
| genshi_xml      | 63.6 ms                                                | 48.6 ms: 1.31x faster                                  |
| Geometric mean  | (ref)                                                  | 1.39x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.8 ms                                                | 30.6 ms: 2.48x faster                                  |
| deltablue               | 7.39 ms                                                | 3.20 ms: 2.31x faster                                  |
| logging_silent          | 173 ns                                                 | 93.2 ns: 1.86x faster                                  |
| scimark_sor             | 193 ms                                                 | 109 ms: 1.78x faster                                   |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                   |
| richards                | 71.4 ms                                                | 42.6 ms: 1.68x faster                                  |
| pyflate                 | 675 ms                                                 | 424 ms: 1.59x faster                                   |
| crypto_pyaes            | 118 ms                                                 | 75.2 ms: 1.56x faster                                  |
| pickle_pure_python      | 453 us                                                 | 291 us: 1.56x faster                                   |
| raytrace                | 461 ms                                                 | 298 ms: 1.55x faster                                   |
| python_startup          | 13.9 ms                                                | 9.03 ms: 1.54x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 68.0 ms: 1.54x faster                                  |
| chaos                   | 104 ms                                                 | 68.1 ms: 1.53x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.18 ms: 1.52x faster                                  |
| spectral_norm           | 148 ms                                                 | 97.3 ms: 1.52x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 199 us: 1.49x faster                                   |
| deepcopy_memo           | 50.0 us                                                | 34.4 us: 1.45x faster                                  |
| nbody                   | 136 ms                                                 | 94.0 ms: 1.45x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.2 ms: 1.44x faster                                  |
| float                   | 108 ms                                                 | 74.6 ms: 1.44x faster                                  |
| mako                    | 14.3 ms                                                | 10.1 ms: 1.42x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.56 ms: 1.41x faster                                  |
| scimark_lu              | 158 ms                                                 | 112 ms: 1.41x faster                                   |
| sqlglot_parse           | 2.04 ms                                                | 1.45 ms: 1.40x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.41 sec: 1.40x faster                                 |
| html5lib                | 85.8 ms                                                | 61.4 ms: 1.40x faster                                  |
| django_template         | 46.3 ms                                                | 33.2 ms: 1.39x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.74 ms: 1.39x faster                                  |
| logging_simple          | 8.06 us                                                | 5.83 us: 1.38x faster                                  |
| chameleon               | 8.86 ms                                                | 6.42 ms: 1.38x faster                                  |
| logging_format          | 8.92 us                                                | 6.48 us: 1.38x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 43.2 ns: 1.38x faster                                  |
| pprint_safe_repr        | 943 ms                                                 | 687 ms: 1.37x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.37x faster                                 |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.37x faster                                 |
| async_tree_none         | 713 ms                                                 | 522 ms: 1.37x faster                                   |
| tornado_http            | 128 ms                                                 | 94.9 ms: 1.35x faster                                  |
| coroutines              | 31.7 ms                                                | 23.5 ms: 1.35x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 55.4 ms: 1.34x faster                                  |
| thrift                  | 1.03 ms                                                | 777 us: 1.33x faster                                   |
| 2to3                    | 332 ms                                                 | 250 ms: 1.33x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.32x faster                                  |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.32x faster                                  |
| async_tree_memoization  | 854 ms                                                 | 653 ms: 1.31x faster                                   |
| genshi_xml              | 63.6 ms                                                | 48.6 ms: 1.31x faster                                  |
| regex_compile           | 174 ms                                                 | 133 ms: 1.30x faster                                   |
| deepcopy                | 429 us                                                 | 329 us: 1.30x faster                                   |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.29x faster                                   |
| scimark_fft             | 414 ms                                                 | 322 ms: 1.29x faster                                   |
| fannkuch                | 477 ms                                                 | 371 ms: 1.29x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.28x faster                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 745 ms: 1.27x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                | 51.3 ms: 1.27x faster                                  |
| docutils                | 3.18 sec                                               | 2.56 sec: 1.24x faster                                 |
| nqueens                 | 99.3 ms                                                | 82.2 ms: 1.21x faster                                  |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| sqlalchemy_declarative  | 165 ms                                                 | 138 ms: 1.20x faster                                   |
| dulwich_log             | 75.5 ms                                                | 63.2 ms: 1.19x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.60 ms: 1.19x faster                                  |
| bench_thread_pool       | 943 us                                                 | 794 us: 1.19x faster                                   |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.0 ms: 1.17x faster                                  |
| json                    | 5.35 ms                                                | 4.59 ms: 1.17x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.7 ms: 1.16x faster                                  |
| sympy_expand            | 537 ms                                                 | 466 ms: 1.15x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 81.3 ms: 1.15x faster                                  |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.14x faster                                  |
| mdp                     | 2.82 sec                                               | 2.49 sec: 1.14x faster                                 |
| sympy_str               | 324 ms                                                 | 288 ms: 1.13x faster                                   |
| pickle_list             | 4.50 us                                                | 4.05 us: 1.11x faster                                  |
| pathlib                 | 20.0 ms                                                | 18.0 ms: 1.11x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.63 us: 1.10x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                   |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.09x faster                                   |
| sympy_sum               | 183 ms                                                 | 168 ms: 1.09x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                   |
| unpickle                | 14.3 us                                                | 13.7 us: 1.04x faster                                  |
| regex_dna               | 214 ms                                                 | 209 ms: 1.02x faster                                   |
| async_generators        | 428 ms                                                 | 421 ms: 1.02x faster                                   |
| telco                   | 6.68 ms                                                | 6.62 ms: 1.01x faster                                  |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| unpickle_list           | 4.99 us                                                | 5.22 us: 1.04x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.40 ms: 1.06x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.5 us: 1.11x slower                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.55 ms: 1.14x slower                                  |
| coverage                | 75.3 ms                                                | 98.3 ms: 1.30x slower                                  |
| Geometric mean          | (ref)                                                  | 1.29x faster                                           |

Benchmark hidden because not significant (2): bench_mp_pool, pickle
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230304-3.12.0a5+-eff9f43/bm-20230304-linux-x86_64-python-main-3.12.0a5+-eff9f43.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
