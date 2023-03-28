
# Results vs. 3.10.4

- fork: python
- ref: b6bd7ffcbc1ffaa68e34
- machine: darwin-arm64
- commit hash: b6bd7ff
- commit date: 2022-12-06
- overall geometric mean: 1.09x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 178 ms: 1.25x faster                                                  |
| chameleon      | 5.86 ms                                                | 5.09 ms: 1.15x faster                                                 |
| docutils       | 1.76 sec                                               | 1.53 sec: 1.15x faster                                                |
| html5lib       | 44.0 ms                                                | 38.5 ms: 1.14x faster                                                 |
| Geometric mean | (ref)                                                  | 1.17x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 65.2 ms: 1.45x faster                                                 |
| float          | 72.1 ms                                                | 59.1 ms: 1.22x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.21x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 83.2 ms: 1.16x faster                                                 |
| regex_v8       | 17.7 ms                                                | 15.8 ms: 1.12x faster                                                 |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.61 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.32 ms: 1.32x faster                                                 |
| pickle_pure_python   | 284 us                                                 | 229 us: 1.24x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 177 us: 1.15x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 40.4 ms: 1.11x faster                                                 |
| unpickle             | 10.0 us                                                | 9.61 us: 1.04x faster                                                 |
| json_loads           | 17.0 us                                                | 16.4 us: 1.04x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.57 us: 1.04x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 97.6 ms: 1.02x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 53.8 ms: 1.01x faster                                                 |
| pickle_dict          | 18.0 us                                                | 17.9 us: 1.00x faster                                                 |
| pickle               | 7.50 us                                                | 7.61 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 74.3 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.3 ms: 1.28x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 10.2 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.37 ms: 1.44x faster                                                 |
| django_template | 27.2 ms                                                | 24.6 ms: 1.11x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 34.6 ms: 1.09x faster                                                 |
| genshi_text     | 18.2 ms                                                | 17.5 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.16x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 3.06 ms: 1.76x faster                                                 |
| nbody                   | 94.6 ms                                                | 65.2 ms: 1.45x faster                                                 |
| raytrace                | 329 ms                                                 | 228 ms: 1.44x faster                                                  |
| mako                    | 10.6 ms                                                | 7.37 ms: 1.44x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 55.1 ms: 1.41x faster                                                 |
| richards                | 51.4 ms                                                | 37.0 ms: 1.39x faster                                                 |
| logging_silent          | 119 ns                                                 | 86.1 ns: 1.38x faster                                                 |
| go                      | 165 ms                                                 | 125 ms: 1.32x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.32 ms: 1.32x faster                                                 |
| async_tree_io           | 1.01 sec                                               | 792 ms: 1.28x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 384 ms: 1.26x faster                                                  |
| async_tree_none         | 396 ms                                                 | 316 ms: 1.25x faster                                                  |
| 2to3                    | 222 ms                                                 | 178 ms: 1.25x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.78 ms: 1.25x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 57.9 ms: 1.25x faster                                                 |
| chaos                   | 66.5 ms                                                | 53.3 ms: 1.25x faster                                                 |
| pycparser               | 915 ms                                                 | 734 ms: 1.25x faster                                                  |
| pyflate                 | 454 ms                                                 | 366 ms: 1.24x faster                                                  |
| scimark_lu              | 110 ms                                                 | 88.5 ms: 1.24x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 229 us: 1.24x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.09 ms: 1.22x faster                                                 |
| float                   | 72.1 ms                                                | 59.1 ms: 1.22x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.27 ms: 1.21x faster                                                 |
| thrift                  | 577 us                                                 | 478 us: 1.21x faster                                                  |
| scimark_fft             | 231 ms                                                 | 198 ms: 1.17x faster                                                  |
| fannkuch                | 318 ms                                                 | 273 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 573 ms: 1.16x faster                                                  |
| scimark_sor             | 126 ms                                                 | 109 ms: 1.16x faster                                                  |
| regex_compile           | 96.2 ms                                                | 83.2 ms: 1.16x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 177 us: 1.15x faster                                                  |
| chameleon               | 5.86 ms                                                | 5.09 ms: 1.15x faster                                                 |
| docutils                | 1.76 sec                                               | 1.53 sec: 1.15x faster                                                |
| pprint_safe_repr        | 608 ms                                                 | 531 ms: 1.14x faster                                                  |
| html5lib                | 44.0 ms                                                | 38.5 ms: 1.14x faster                                                 |
| pprint_pformat          | 1.24 sec                                               | 1.08 sec: 1.14x faster                                                |
| spectral_norm           | 95.8 ms                                                | 84.2 ms: 1.14x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 32.0 ms: 1.14x faster                                                 |
| hexiom                  | 6.31 ms                                                | 5.60 ms: 1.13x faster                                                 |
| regex_v8                | 17.7 ms                                                | 15.8 ms: 1.12x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 40.4 ms: 1.11x faster                                                 |
| logging_format          | 4.95 us                                                | 4.46 us: 1.11x faster                                                 |
| django_template         | 27.2 ms                                                | 24.6 ms: 1.11x faster                                                 |
| logging_simple          | 4.61 us                                                | 4.16 us: 1.11x faster                                                 |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 34.6 ms: 1.09x faster                                                 |
| json                    | 3.13 ms                                                | 2.88 ms: 1.09x faster                                                 |
| telco                   | 3.63 ms                                                | 3.37 ms: 1.08x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 35.8 ms: 1.06x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 32.6 us: 1.05x faster                                                 |
| sqlite_synth            | 1.50 us                                                | 1.42 us: 1.05x faster                                                 |
| unpickle                | 10.0 us                                                | 9.61 us: 1.04x faster                                                 |
| genshi_text             | 18.2 ms                                                | 17.5 ms: 1.04x faster                                                 |
| sympy_integrate         | 13.3 ms                                                | 12.8 ms: 1.04x faster                                                 |
| json_loads              | 17.0 us                                                | 16.4 us: 1.04x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.57 us: 1.04x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 516 us: 1.03x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 97.6 ms: 1.02x faster                                                 |
| deepcopy                | 278 us                                                 | 272 us: 1.02x faster                                                  |
| sympy_expand            | 275 ms                                                 | 270 ms: 1.02x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.32 us: 1.02x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 92.1 ms: 1.01x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 53.8 ms: 1.01x faster                                                 |
| sympy_str               | 169 ms                                                 | 168 ms: 1.01x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 197 ms: 1.01x faster                                                  |
| pickle_dict             | 18.0 us                                                | 17.9 us: 1.00x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.67 sec: 1.01x slower                                                |
| async_generators        | 231 ms                                                 | 233 ms: 1.01x slower                                                  |
| pickle                  | 7.50 us                                                | 7.61 us: 1.01x slower                                                 |
| nqueens                 | 68.6 ms                                                | 70.0 ms: 1.02x slower                                                 |
| meteor_contest          | 77.7 ms                                                | 79.4 ms: 1.02x slower                                                 |
| regex_effbot            | 2.45 ms                                                | 2.61 ms: 1.07x slower                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 74.3 ms: 1.08x slower                                                 |
| bench_mp_pool           | 40.8 ms                                                | 44.8 ms: 1.10x slower                                                 |
| coroutines              | 20.1 ms                                                | 24.5 ms: 1.22x slower                                                 |
| pathlib                 | 22.2 ms                                                | 28.0 ms: 1.26x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.3 ms: 1.28x slower                                                 |
| generators              | 32.5 ms                                                | 42.2 ms: 1.30x slower                                                 |
| unpack_sequence         | 38.2 ns                                                | 52.7 ns: 1.38x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 10.2 ms: 1.45x slower                                                 |
| coverage                | 40.8 ms                                                | 64.8 ms: 1.59x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (8) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (6) of public/results/bm-20221206-3.12.0a3-b6bd7ff/bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
