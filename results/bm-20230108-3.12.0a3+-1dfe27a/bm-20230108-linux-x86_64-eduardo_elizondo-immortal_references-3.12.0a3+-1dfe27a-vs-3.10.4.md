
# Results vs. 3.10.4

- fork: eduardo_elizondo
- ref: immortal_references
- machine: linux-x86_64
- commit hash: 1dfe27a
- commit date: 2023-01-08
- overall geometric mean: 1.22x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 274 ms: 1.21x faster                                                            |
| chameleon      | 8.86 ms                                                | 6.83 ms: 1.30x faster                                                           |
| docutils       | 3.18 sec                                               | 2.69 sec: 1.18x faster                                                          |
| html5lib       | 85.8 ms                                                | 64.0 ms: 1.34x faster                                                           |
| Geometric mean | (ref)                                                  | 1.26x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 79.7 ms: 1.35x faster                                                           |
| nbody          | 136 ms                                                 | 96.7 ms: 1.41x faster                                                           |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                  | 1.24x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 144 ms: 1.21x faster                                                            |
| regex_dna      | 214 ms                                                 | 203 ms: 1.05x faster                                                            |
| regex_effbot   | 3.21 ms                                                | 3.39 ms: 1.06x slower                                                           |
| regex_v8       | 25.0 ms                                                | 21.1 ms: 1.18x faster                                                           |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.78 ms: 1.38x faster                                                           |
| json_loads           | 28.9 us                                                | 26.6 us: 1.08x faster                                                           |
| pickle               | 10.1 us                                                | 10.5 us: 1.04x slower                                                           |
| pickle_dict          | 28.3 us                                                | 30.5 us: 1.08x slower                                                           |
| pickle_list          | 4.50 us                                                | 4.35 us: 1.03x faster                                                           |
| pickle_pure_python   | 453 us                                                 | 309 us: 1.47x faster                                                            |
| unpickle             | 14.3 us                                                | 13.7 us: 1.04x faster                                                           |
| unpickle_list        | 4.99 us                                                | 4.79 us: 1.04x faster                                                           |
| unpickle_pure_python | 297 us                                                 | 217 us: 1.37x faster                                                            |
| xml_etree_parse      | 163 ms                                                 | 151 ms: 1.08x faster                                                            |
| xml_etree_iterparse  | 110 ms                                                 | 106 ms: 1.04x faster                                                            |
| xml_etree_generate   | 93.3 ms                                                | 79.5 ms: 1.17x faster                                                           |
| xml_etree_process    | 74.5 ms                                                | 56.7 ms: 1.31x faster                                                           |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.77 ms: 1.59x faster                                                           |
| python_startup_no_site | 5.76 ms                                                | 6.21 ms: 1.08x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.22x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| django_template | 46.3 ms                                                | 34.8 ms: 1.33x faster                                                           |
| genshi_text     | 30.6 ms                                                | 22.2 ms: 1.38x faster                                                           |
| genshi_xml      | 63.6 ms                                                | 51.0 ms: 1.25x faster                                                           |
| mako            | 14.3 ms                                                | 10.5 ms: 1.36x faster                                                           |
| Geometric mean  | (ref)                                                  | 1.33x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 274 ms: 1.21x faster                                                            |
| async_generators        | 428 ms                                                 | 375 ms: 1.14x faster                                                            |
| async_tree_none         | 713 ms                                                 | 536 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed | 949 ms                                                 | 765 ms: 1.24x faster                                                            |
| async_tree_io           | 1.78 sec                                               | 1.34 sec: 1.33x faster                                                          |
| async_tree_memoization  | 854 ms                                                 | 688 ms: 1.24x faster                                                            |
| chameleon               | 8.86 ms                                                | 6.83 ms: 1.30x faster                                                           |
| chaos                   | 104 ms                                                 | 69.2 ms: 1.51x faster                                                           |
| bench_thread_pool       | 943 us                                                 | 834 us: 1.13x faster                                                            |
| coroutines              | 31.7 ms                                                | 26.6 ms: 1.19x faster                                                           |
| coverage                | 75.3 ms                                                | 102 ms: 1.36x slower                                                            |
| crypto_pyaes            | 118 ms                                                 | 79.0 ms: 1.49x faster                                                           |
| deepcopy                | 429 us                                                 | 366 us: 1.17x faster                                                            |
| deepcopy_reduce         | 3.75 us                                                | 3.21 us: 1.17x faster                                                           |
| deepcopy_memo           | 50.0 us                                                | 38.0 us: 1.32x faster                                                           |
| deltablue               | 7.39 ms                                                | 3.68 ms: 2.01x faster                                                           |
| django_template         | 46.3 ms                                                | 34.8 ms: 1.33x faster                                                           |
| docutils                | 3.18 sec                                               | 2.69 sec: 1.18x faster                                                          |
| dulwich_log             | 75.5 ms                                                | 68.7 ms: 1.10x faster                                                           |
| fannkuch                | 477 ms                                                 | 387 ms: 1.23x faster                                                            |
| float                   | 108 ms                                                 | 79.7 ms: 1.35x faster                                                           |
| generators              | 75.8 ms                                                | 80.5 ms: 1.06x slower                                                           |
| genshi_text             | 30.6 ms                                                | 22.2 ms: 1.38x faster                                                           |
| genshi_xml              | 63.6 ms                                                | 51.0 ms: 1.25x faster                                                           |
| go                      | 226 ms                                                 | 134 ms: 1.69x faster                                                            |
| hexiom                  | 9.42 ms                                                | 6.38 ms: 1.48x faster                                                           |
| html5lib                | 85.8 ms                                                | 64.0 ms: 1.34x faster                                                           |
| json                    | 5.35 ms                                                | 5.00 ms: 1.07x faster                                                           |
| json_dumps              | 13.5 ms                                                | 9.78 ms: 1.38x faster                                                           |
| json_loads              | 28.9 us                                                | 26.6 us: 1.08x faster                                                           |
| logging_format          | 8.92 us                                                | 6.96 us: 1.28x faster                                                           |
| logging_silent          | 173 ns                                                 | 101 ns: 1.72x faster                                                            |
| logging_simple          | 8.06 us                                                | 6.31 us: 1.28x faster                                                           |
| mako                    | 14.3 ms                                                | 10.5 ms: 1.36x faster                                                           |
| mdp                     | 2.82 sec                                               | 2.61 sec: 1.08x faster                                                          |
| meteor_contest          | 114 ms                                                 | 116 ms: 1.02x slower                                                            |
| mypy                    | 1.01 sec                                               | 876 ms: 1.16x faster                                                            |
| nbody                   | 136 ms                                                 | 96.7 ms: 1.41x faster                                                           |
| nqueens                 | 99.3 ms                                                | 80.1 ms: 1.24x faster                                                           |
| pathlib                 | 20.0 ms                                                | 18.4 ms: 1.09x faster                                                           |
| pickle                  | 10.1 us                                                | 10.5 us: 1.04x slower                                                           |
| pickle_dict             | 28.3 us                                                | 30.5 us: 1.08x slower                                                           |
| pickle_list             | 4.50 us                                                | 4.35 us: 1.03x faster                                                           |
| pickle_pure_python      | 453 us                                                 | 309 us: 1.47x faster                                                            |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                                            |
| pprint_safe_repr        | 943 ms                                                 | 729 ms: 1.29x faster                                                            |
| pprint_pformat          | 1.97 sec                                               | 1.49 sec: 1.33x faster                                                          |
| pycparser               | 1.51 sec                                               | 1.15 sec: 1.31x faster                                                          |
| pyflate                 | 675 ms                                                 | 429 ms: 1.57x faster                                                            |
| python_startup          | 13.9 ms                                                | 8.77 ms: 1.59x faster                                                           |
| python_startup_no_site  | 5.76 ms                                                | 6.21 ms: 1.08x slower                                                           |
| raytrace                | 461 ms                                                 | 309 ms: 1.49x faster                                                            |
| regex_compile           | 174 ms                                                 | 144 ms: 1.21x faster                                                            |
| regex_dna               | 214 ms                                                 | 203 ms: 1.05x faster                                                            |
| regex_effbot            | 3.21 ms                                                | 3.39 ms: 1.06x slower                                                           |
| regex_v8                | 25.0 ms                                                | 21.1 ms: 1.18x faster                                                           |
| richards                | 71.4 ms                                                | 44.9 ms: 1.59x faster                                                           |
| scimark_fft             | 414 ms                                                 | 359 ms: 1.15x faster                                                            |
| scimark_lu              | 158 ms                                                 | 115 ms: 1.37x faster                                                            |
| scimark_monte_carlo     | 105 ms                                                 | 69.6 ms: 1.51x faster                                                           |
| scimark_sor             | 193 ms                                                 | 121 ms: 1.60x faster                                                            |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.34 ms: 1.26x faster                                                           |
| spectral_norm           | 148 ms                                                 | 106 ms: 1.40x faster                                                            |
| sqlglot_parse           | 2.04 ms                                                | 1.55 ms: 1.32x faster                                                           |
| sqlglot_transpile       | 2.42 ms                                                | 1.87 ms: 1.29x faster                                                           |
| sqlglot_optimize        | 65.3 ms                                                | 55.2 ms: 1.18x faster                                                           |
| sqlglot_normalize       | 135 ms                                                 | 114 ms: 1.19x faster                                                            |
| sqlite_synth            | 2.90 us                                                | 2.65 us: 1.10x faster                                                           |
| sympy_expand            | 537 ms                                                 | 501 ms: 1.07x faster                                                            |
| sympy_integrate         | 23.9 ms                                                | 22.0 ms: 1.09x faster                                                           |
| sympy_sum               | 183 ms                                                 | 182 ms: 1.01x faster                                                            |
| sympy_str               | 324 ms                                                 | 311 ms: 1.04x faster                                                            |
| telco                   | 6.68 ms                                                | 6.64 ms: 1.01x faster                                                           |
| thrift                  | 1.03 ms                                                | 775 us: 1.33x faster                                                            |
| unpack_sequence         | 59.5 ns                                                | 51.6 ns: 1.15x faster                                                           |
| unpickle                | 14.3 us                                                | 13.7 us: 1.04x faster                                                           |
| unpickle_list           | 4.99 us                                                | 4.79 us: 1.04x faster                                                           |
| unpickle_pure_python    | 297 us                                                 | 217 us: 1.37x faster                                                            |
| xml_etree_parse         | 163 ms                                                 | 151 ms: 1.08x faster                                                            |
| xml_etree_iterparse     | 110 ms                                                 | 106 ms: 1.04x faster                                                            |
| xml_etree_generate      | 93.3 ms                                                | 79.5 ms: 1.17x faster                                                           |
| xml_etree_process       | 74.5 ms                                                | 56.7 ms: 1.31x faster                                                           |
| Geometric mean          | (ref)                                                  | 1.22x faster                                                                    |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (5) of public/results/bm-20230108-3.12.0a3+-1dfe27a/bm-20230108-linux-x86_64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
