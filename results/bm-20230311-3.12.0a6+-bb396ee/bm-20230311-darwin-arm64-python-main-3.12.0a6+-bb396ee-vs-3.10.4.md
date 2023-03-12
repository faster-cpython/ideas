
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: bb396ee
- commit date: 2023-03-11
- overall geometric mean: 1.19x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 166 ms: 1.34x faster                                   |
| chameleon      | 5.86 ms                                                | 4.51 ms: 1.30x faster                                  |
| docutils       | 1.76 sec                                               | 1.49 sec: 1.18x faster                                 |
| html5lib       | 44.0 ms                                                | 35.8 ms: 1.23x faster                                  |
| tornado_http   | 90.1 ms                                                | 68.7 ms: 1.31x faster                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.1 ms: 1.48x faster                                  |
| float          | 72.1 ms                                                | 53.6 ms: 1.34x faster                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.7 ms: 1.27x faster                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.69 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 190 us: 1.49x faster                                   |
| unpickle_pure_python | 204 us                                                 | 145 us: 1.40x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.30 ms: 1.32x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 36.8 ms: 1.23x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 51.0 ms: 1.07x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 97.2 ms: 1.03x faster                                  |
| unpickle             | 10.0 us                                                | 9.76 us: 1.03x faster                                  |
| pickle_list          | 2.83 us                                                | 2.81 us: 1.01x faster                                  |
| pickle               | 7.50 us                                                | 7.48 us: 1.00x faster                                  |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| unpickle_list        | 2.66 us                                                | 2.69 us: 1.01x slower                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.8 ms: 1.03x slower                                  |
| Geometric mean       | (ref)                                                  | 1.11x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 11.1 ms: 1.15x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 8.93 ms: 1.28x slower                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.47 ms: 1.42x faster                                  |
| genshi_xml      | 37.7 ms                                                | 29.4 ms: 1.28x faster                                  |
| django_template | 27.2 ms                                                | 21.7 ms: 1.26x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.9 ms: 1.22x faster                                  |
| Geometric mean  | (ref)                                                  | 1.29x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.59 ms: 2.08x faster                                  |
| logging_silent          | 119 ns                                                 | 68.9 ns: 1.73x faster                                  |
| richards                | 51.4 ms                                                | 30.7 ms: 1.67x faster                                  |
| pickle_pure_python      | 284 us                                                 | 190 us: 1.49x faster                                   |
| go                      | 165 ms                                                 | 111 ms: 1.49x faster                                   |
| nbody                   | 94.6 ms                                                | 64.1 ms: 1.48x faster                                  |
| scimark_lu              | 110 ms                                                 | 75.0 ms: 1.46x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.7 ms: 1.45x faster                                  |
| raytrace                | 329 ms                                                 | 228 ms: 1.44x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 336 ms: 1.44x faster                                   |
| scimark_sor             | 126 ms                                                 | 88.4 ms: 1.43x faster                                  |
| hexiom                  | 6.31 ms                                                | 4.45 ms: 1.42x faster                                  |
| mako                    | 10.6 ms                                                | 7.47 ms: 1.42x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 51.3 ms: 1.41x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 145 us: 1.40x faster                                   |
| chaos                   | 66.5 ms                                                | 47.9 ms: 1.39x faster                                  |
| pyflate                 | 454 ms                                                 | 332 ms: 1.37x faster                                   |
| async_tree_none         | 396 ms                                                 | 290 ms: 1.37x faster                                   |
| async_tree_io           | 1.01 sec                                               | 745 ms: 1.36x faster                                   |
| pycparser               | 915 ms                                                 | 678 ms: 1.35x faster                                   |
| float                   | 72.1 ms                                                | 53.6 ms: 1.34x faster                                  |
| 2to3                    | 222 ms                                                 | 166 ms: 1.34x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.30 ms: 1.32x faster                                  |
| tornado_http            | 90.1 ms                                                | 68.7 ms: 1.31x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 26.3 us: 1.31x faster                                  |
| chameleon               | 5.86 ms                                                | 4.51 ms: 1.30x faster                                  |
| genshi_xml              | 37.7 ms                                                | 29.4 ms: 1.28x faster                                  |
| spectral_norm           | 95.8 ms                                                | 75.0 ms: 1.28x faster                                  |
| thrift                  | 577 us                                                 | 453 us: 1.28x faster                                   |
| regex_compile           | 96.2 ms                                                | 75.7 ms: 1.27x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 979 ms: 1.27x faster                                   |
| logging_simple          | 4.61 us                                                | 3.64 us: 1.26x faster                                  |
| pprint_safe_repr        | 608 ms                                                 | 481 ms: 1.26x faster                                   |
| sqlglot_parse           | 1.33 ms                                                | 1.06 ms: 1.26x faster                                  |
| django_template         | 27.2 ms                                                | 21.7 ms: 1.26x faster                                  |
| logging_format          | 4.95 us                                                | 3.94 us: 1.26x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.23 ms: 1.26x faster                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.18 ms: 1.25x faster                                  |
| fannkuch                | 318 ms                                                 | 257 ms: 1.24x faster                                   |
| deepcopy                | 278 us                                                 | 225 us: 1.23x faster                                   |
| html5lib                | 44.0 ms                                                | 35.8 ms: 1.23x faster                                  |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 36.8 ms: 1.23x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.9 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 548 ms: 1.21x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.97 us: 1.20x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 32.2 ms: 1.18x faster                                  |
| docutils                | 1.76 sec                                               | 1.49 sec: 1.18x faster                                 |
| scimark_fft             | 231 ms                                                 | 196 ms: 1.18x faster                                   |
| unpack_sequence         | 38.2 ns                                                | 32.8 ns: 1.17x faster                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.3 ms: 1.16x faster                                  |
| generators              | 32.5 ms                                                | 28.2 ms: 1.15x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 175 ms: 1.14x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.8 ms: 1.13x faster                                  |
| bench_thread_pool       | 531 us                                                 | 473 us: 1.12x faster                                   |
| coroutines              | 20.1 ms                                                | 18.1 ms: 1.11x faster                                  |
| mdp                     | 1.66 sec                                               | 1.50 sec: 1.11x faster                                 |
| sympy_expand            | 275 ms                                                 | 248 ms: 1.11x faster                                   |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| json                    | 3.13 ms                                                | 2.84 ms: 1.10x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.17 ms: 1.09x faster                                  |
| sympy_str               | 169 ms                                                 | 155 ms: 1.09x faster                                   |
| nqueens                 | 68.6 ms                                                | 62.9 ms: 1.09x faster                                  |
| regex_dna               | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| xml_etree_generate      | 54.5 ms                                                | 51.0 ms: 1.07x faster                                  |
| telco                   | 3.63 ms                                                | 3.40 ms: 1.07x faster                                  |
| sympy_sum               | 93.5 ms                                                | 88.7 ms: 1.05x faster                                  |
| meteor_contest          | 77.7 ms                                                | 73.8 ms: 1.05x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 97.2 ms: 1.03x faster                                  |
| unpickle                | 10.0 us                                                | 9.76 us: 1.03x faster                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                   |
| pickle_list             | 2.83 us                                                | 2.81 us: 1.01x faster                                  |
| pickle                  | 7.50 us                                                | 7.48 us: 1.00x faster                                  |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| unpickle_list           | 2.66 us                                                | 2.69 us: 1.01x slower                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.8 ms: 1.03x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.69 ms: 1.10x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 45.2 ms: 1.11x slower                                  |
| python_startup          | 9.59 ms                                                | 11.1 ms: 1.15x slower                                  |
| async_generators        | 231 ms                                                 | 267 ms: 1.16x slower                                   |
| pathlib                 | 22.2 ms                                                | 27.5 ms: 1.24x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 8.93 ms: 1.28x slower                                  |
| coverage                | 40.8 ms                                                | 59.7 ms: 1.46x slower                                  |
| Geometric mean          | (ref)                                                  | 1.19x faster                                           |
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230311-3.12.0a6+-bb396ee/bm-20230311-darwin-arm64-python-main-3.12.0a6+-bb396ee.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
