
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 30a306c
- commit date: 2023-03-25
- overall geometric mean: 1.19x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 168 ms: 1.32x faster                                   |
| chameleon      | 5.86 ms                                                | 4.51 ms: 1.30x faster                                  |
| docutils       | 1.76 sec                                               | 1.51 sec: 1.17x faster                                 |
| html5lib       | 44.0 ms                                                | 36.7 ms: 1.20x faster                                  |
| tornado_http   | 90.1 ms                                                | 69.1 ms: 1.30x faster                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 60.6 ms: 1.56x faster                                  |
| float          | 72.1 ms                                                | 53.1 ms: 1.36x faster                                  |
| pidigits       | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 77.0 ms: 1.25x faster                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.71 ms: 1.11x slower                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 194 us: 1.46x faster                                   |
| unpickle_pure_python | 204 us                                                 | 151 us: 1.35x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.24 ms: 1.34x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 37.0 ms: 1.22x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 52.0 ms: 1.05x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| unpickle             | 10.0 us                                                | 9.71 us: 1.03x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 97.8 ms: 1.02x faster                                  |
| pickle               | 7.50 us                                                | 7.45 us: 1.01x faster                                  |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| unpickle_list        | 2.66 us                                                | 2.68 us: 1.01x slower                                  |
| pickle_list          | 2.83 us                                                | 2.87 us: 1.02x slower                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.7 ms: 1.02x slower                                  |
| Geometric mean       | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.3 ms: 1.28x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 10.3 ms: 1.47x slower                                  |
| Geometric mean         | (ref)                                                  | 1.37x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.40 ms: 1.43x faster                                  |
| genshi_xml      | 37.7 ms                                                | 29.4 ms: 1.28x faster                                  |
| django_template | 27.2 ms                                                | 21.9 ms: 1.25x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.9 ms: 1.22x faster                                  |
| Geometric mean  | (ref)                                                  | 1.29x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.62 ms: 2.05x faster                                  |
| logging_silent          | 119 ns                                                 | 66.6 ns: 1.79x faster                                  |
| richards                | 51.4 ms                                                | 31.5 ms: 1.63x faster                                  |
| nbody                   | 94.6 ms                                                | 60.6 ms: 1.56x faster                                  |
| scimark_lu              | 110 ms                                                 | 71.4 ms: 1.54x faster                                  |
| async_tree_memoization  | 485 ms                                                 | 326 ms: 1.49x faster                                   |
| raytrace                | 329 ms                                                 | 222 ms: 1.48x faster                                   |
| pickle_pure_python      | 284 us                                                 | 194 us: 1.46x faster                                   |
| scimark_sor             | 126 ms                                                 | 88.0 ms: 1.43x faster                                  |
| mako                    | 10.6 ms                                                | 7.40 ms: 1.43x faster                                  |
| hexiom                  | 6.31 ms                                                | 4.42 ms: 1.43x faster                                  |
| go                      | 165 ms                                                 | 116 ms: 1.42x faster                                   |
| crypto_pyaes            | 77.9 ms                                                | 54.8 ms: 1.42x faster                                  |
| chaos                   | 66.5 ms                                                | 47.2 ms: 1.41x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 52.1 ms: 1.39x faster                                  |
| async_tree_io           | 1.01 sec                                               | 740 ms: 1.37x faster                                   |
| async_tree_none         | 396 ms                                                 | 290 ms: 1.37x faster                                   |
| float                   | 72.1 ms                                                | 53.1 ms: 1.36x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 151 us: 1.35x faster                                   |
| pycparser               | 915 ms                                                 | 680 ms: 1.35x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.24 ms: 1.34x faster                                  |
| pyflate                 | 454 ms                                                 | 343 ms: 1.32x faster                                   |
| deepcopy_memo           | 34.4 us                                                | 26.0 us: 1.32x faster                                  |
| 2to3                    | 222 ms                                                 | 168 ms: 1.32x faster                                   |
| spectral_norm           | 95.8 ms                                                | 73.1 ms: 1.31x faster                                  |
| tornado_http            | 90.1 ms                                                | 69.1 ms: 1.30x faster                                  |
| chameleon               | 5.86 ms                                                | 4.51 ms: 1.30x faster                                  |
| genshi_xml              | 37.7 ms                                                | 29.4 ms: 1.28x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 980 ms: 1.27x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 480 ms: 1.26x faster                                   |
| thrift                  | 577 us                                                 | 460 us: 1.26x faster                                   |
| regex_compile           | 96.2 ms                                                | 77.0 ms: 1.25x faster                                  |
| logging_simple          | 4.61 us                                                | 3.69 us: 1.25x faster                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.23 ms: 1.25x faster                                  |
| django_template         | 27.2 ms                                                | 21.9 ms: 1.25x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.07 ms: 1.24x faster                                  |
| logging_format          | 4.95 us                                                | 3.99 us: 1.24x faster                                  |
| deepcopy                | 278 us                                                 | 224 us: 1.24x faster                                   |
| sqlglot_transpile       | 1.54 ms                                                | 1.25 ms: 1.24x faster                                  |
| scimark_fft             | 231 ms                                                 | 189 ms: 1.23x faster                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.84 ms: 1.22x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.9 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 546 ms: 1.22x faster                                   |
| xml_etree_process       | 45.1 ms                                                | 37.0 ms: 1.22x faster                                  |
| dulwich_log             | 36.4 ms                                                | 30.2 ms: 1.21x faster                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.97 us: 1.20x faster                                  |
| html5lib                | 44.0 ms                                                | 36.7 ms: 1.20x faster                                  |
| generators              | 32.5 ms                                                | 27.1 ms: 1.20x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 32.4 ms: 1.17x faster                                  |
| fannkuch                | 318 ms                                                 | 271 ms: 1.17x faster                                   |
| docutils                | 1.76 sec                                               | 1.51 sec: 1.17x faster                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.6 ms: 1.15x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 33.3 ns: 1.15x faster                                  |
| sympy_integrate         | 13.3 ms                                                | 11.8 ms: 1.13x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 177 ms: 1.12x faster                                   |
| bench_thread_pool       | 531 us                                                 | 475 us: 1.12x faster                                   |
| json                    | 3.13 ms                                                | 2.81 ms: 1.11x faster                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                  |
| sympy_expand            | 275 ms                                                 | 250 ms: 1.10x faster                                   |
| sympy_str               | 169 ms                                                 | 156 ms: 1.08x faster                                   |
| regex_dna               | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                 |
| nqueens                 | 68.6 ms                                                | 63.7 ms: 1.08x faster                                  |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                  |
| sympy_sum               | 93.5 ms                                                | 88.6 ms: 1.05x faster                                  |
| meteor_contest          | 77.7 ms                                                | 73.8 ms: 1.05x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 52.0 ms: 1.05x faster                                  |
| telco                   | 3.63 ms                                                | 3.46 ms: 1.05x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| unpickle                | 10.0 us                                                | 9.71 us: 1.03x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 97.8 ms: 1.02x faster                                  |
| pidigits                | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| pickle                  | 7.50 us                                                | 7.45 us: 1.01x faster                                  |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| unpickle_list           | 2.66 us                                                | 2.68 us: 1.01x slower                                  |
| pickle_list             | 2.83 us                                                | 2.87 us: 1.02x slower                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.7 ms: 1.02x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.71 ms: 1.11x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 46.2 ms: 1.13x slower                                  |
| async_generators        | 231 ms                                                 | 267 ms: 1.16x slower                                   |
| pathlib                 | 22.2 ms                                                | 28.2 ms: 1.27x slower                                  |
| python_startup          | 9.59 ms                                                | 12.3 ms: 1.28x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.3 ms: 1.47x slower                                  |
| coverage                | 40.8 ms                                                | 60.8 ms: 1.49x slower                                  |
| Geometric mean          | (ref)                                                  | 1.19x faster                                           |
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230325-3.12.0a6+-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6+-30a306c.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
