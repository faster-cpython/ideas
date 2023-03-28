
# Results vs. 3.10.4

- fork: python
- ref: 3b9d793efcfd2c00c14f
- machine: darwin-arm64
- commit hash: 3b9d793
- commit date: 2022-11-14
- overall geometric mean: 1.17x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 167 ms: 1.33x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.44 ms: 1.32x faster                                                 |
| docutils       | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| html5lib       | 44.0 ms                                                | 35.9 ms: 1.22x faster                                                 |
| tornado_http   | 90.1 ms                                                | 71.3 ms: 1.26x faster                                                 |
| Geometric mean | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 65.8 ms: 1.44x faster                                                 |
| float          | 72.1 ms                                                | 56.3 ms: 1.28x faster                                                 |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.0 ms: 1.27x faster                                                 |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                 |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.60 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 205 us: 1.38x faster                                                  |
| json_dumps           | 8.34 ms                                                | 6.12 ms: 1.36x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 35.5 ms: 1.27x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 162 us: 1.26x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.7 ms: 1.12x faster                                                 |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 96.3 ms: 1.04x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.59 us: 1.03x faster                                                 |
| pickle               | 7.50 us                                                | 7.44 us: 1.01x faster                                                 |
| pickle_list          | 2.83 us                                                | 2.85 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 69.6 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x faster                                                          |

Benchmark hidden because not significant (2): unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.3 ms: 1.29x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 10.2 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.18 ms: 1.48x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 29.6 ms: 1.28x faster                                                 |
| django_template | 27.2 ms                                                | 21.4 ms: 1.27x faster                                                 |
| genshi_text     | 18.2 ms                                                | 14.8 ms: 1.23x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.31x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.68 ms: 2.00x faster                                                 |
| logging_silent          | 119 ns                                                 | 67.1 ns: 1.78x faster                                                 |
| richards                | 51.4 ms                                                | 32.0 ms: 1.61x faster                                                 |
| scimark_lu              | 110 ms                                                 | 70.0 ms: 1.57x faster                                                 |
| raytrace                | 329 ms                                                 | 214 ms: 1.54x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 51.9 ms: 1.50x faster                                                 |
| mako                    | 10.6 ms                                                | 7.18 ms: 1.48x faster                                                 |
| nbody                   | 94.6 ms                                                | 65.8 ms: 1.44x faster                                                 |
| async_tree_memoization  | 485 ms                                                 | 338 ms: 1.43x faster                                                  |
| go                      | 165 ms                                                 | 119 ms: 1.39x faster                                                  |
| pickle_pure_python      | 284 us                                                 | 205 us: 1.38x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.12 ms: 1.36x faster                                                 |
| async_tree_none         | 396 ms                                                 | 294 ms: 1.34x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 755 ms: 1.34x faster                                                  |
| 2to3                    | 222 ms                                                 | 167 ms: 1.33x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 54.6 ms: 1.32x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.01 ms: 1.32x faster                                                 |
| chameleon               | 5.86 ms                                                | 4.44 ms: 1.32x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.17 ms: 1.31x faster                                                 |
| pycparser               | 915 ms                                                 | 696 ms: 1.31x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 73.0 ms: 1.31x faster                                                 |
| thrift                  | 577 us                                                 | 442 us: 1.31x faster                                                  |
| chaos                   | 66.5 ms                                                | 51.0 ms: 1.31x faster                                                 |
| pyflate                 | 454 ms                                                 | 351 ms: 1.29x faster                                                  |
| float                   | 72.1 ms                                                | 56.3 ms: 1.28x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 29.6 ms: 1.28x faster                                                 |
| django_template         | 27.2 ms                                                | 21.4 ms: 1.27x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.63 us: 1.27x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 35.5 ms: 1.27x faster                                                 |
| regex_compile           | 96.2 ms                                                | 76.0 ms: 1.27x faster                                                 |
| tornado_http            | 90.1 ms                                                | 71.3 ms: 1.26x faster                                                 |
| logging_format          | 4.95 us                                                | 3.92 us: 1.26x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 162 us: 1.26x faster                                                  |
| hexiom                  | 6.31 ms                                                | 5.04 ms: 1.25x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.79 ms: 1.24x faster                                                 |
| genshi_text             | 18.2 ms                                                | 14.8 ms: 1.23x faster                                                 |
| pprint_pformat          | 1.24 sec                                               | 1.01 sec: 1.23x faster                                                |
| html5lib                | 44.0 ms                                                | 35.9 ms: 1.22x faster                                                 |
| pprint_safe_repr        | 608 ms                                                 | 497 ms: 1.22x faster                                                  |
| dulwich_log             | 36.4 ms                                                | 30.2 ms: 1.21x faster                                                 |
| scimark_sor             | 126 ms                                                 | 105 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 555 ms: 1.20x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.8 ms: 1.20x faster                                                 |
| docutils                | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| fannkuch                | 318 ms                                                 | 271 ms: 1.17x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 29.5 us: 1.17x faster                                                 |
| scimark_fft             | 231 ms                                                 | 198 ms: 1.16x faster                                                  |
| deepcopy                | 278 us                                                 | 243 us: 1.14x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.07 us: 1.14x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                                  |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                 |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.13x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 473 us: 1.12x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.7 ms: 1.12x faster                                                 |
| async_generators        | 231 ms                                                 | 208 ms: 1.11x faster                                                  |
| sympy_expand            | 275 ms                                                 | 248 ms: 1.11x faster                                                  |
| json                    | 3.13 ms                                                | 2.83 ms: 1.11x faster                                                 |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| sympy_str               | 169 ms                                                 | 155 ms: 1.09x faster                                                  |
| telco                   | 3.63 ms                                                | 3.35 ms: 1.08x faster                                                 |
| nqueens                 | 68.6 ms                                                | 63.9 ms: 1.07x faster                                                 |
| sqlite_synth            | 1.50 us                                                | 1.40 us: 1.07x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.55 sec: 1.07x faster                                                |
| sympy_sum               | 93.5 ms                                                | 87.7 ms: 1.07x faster                                                 |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| xml_etree_parse         | 100 ms                                                 | 96.3 ms: 1.04x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.59 us: 1.03x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 76.7 ms: 1.01x faster                                                 |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| pickle                  | 7.50 us                                                | 7.44 us: 1.01x faster                                                 |
| pickle_list             | 2.83 us                                                | 2.85 us: 1.01x slower                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 69.6 ms: 1.01x slower                                                 |
| coroutines              | 20.1 ms                                                | 20.6 ms: 1.02x slower                                                 |
| regex_effbot            | 2.45 ms                                                | 2.60 ms: 1.06x slower                                                 |
| bench_mp_pool           | 40.8 ms                                                | 44.5 ms: 1.09x slower                                                 |
| generators              | 32.5 ms                                                | 35.8 ms: 1.10x slower                                                 |
| pathlib                 | 22.2 ms                                                | 26.9 ms: 1.21x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.3 ms: 1.29x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 10.2 ms: 1.45x slower                                                 |
| coverage                | 40.8 ms                                                | 60.5 ms: 1.48x slower                                                 |
| unpack_sequence         | 38.2 ns                                                | 62.8 ns: 1.64x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.17x faster                                                          |

Benchmark hidden because not significant (2): unpickle, pickle_dict
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of public/results/bm-20221114-3.12.0a2-3b9d793/bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
