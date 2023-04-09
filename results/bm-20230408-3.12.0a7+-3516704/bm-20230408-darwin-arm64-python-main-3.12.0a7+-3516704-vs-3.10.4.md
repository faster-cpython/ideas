
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 3516704
- commit date: 2023-04-08
- overall geometric mean: 1.20x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 168 ms: 1.32x faster                                   |
| chameleon      | 5.86 ms                                                | 4.50 ms: 1.30x faster                                  |
| docutils       | 1.76 sec                                               | 1.50 sec: 1.18x faster                                 |
| html5lib       | 44.0 ms                                                | 36.6 ms: 1.20x faster                                  |
| tornado_http   | 90.1 ms                                                | 71.0 ms: 1.27x faster                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 60.4 ms: 1.57x faster                                  |
| float          | 72.1 ms                                                | 52.9 ms: 1.36x faster                                  |
| pidigits       | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.7 ms: 1.26x faster                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.67 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 194 us: 1.46x faster                                   |
| unpickle_pure_python | 204 us                                                 | 149 us: 1.37x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.27 ms: 1.33x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 36.8 ms: 1.22x faster                                  |
| unpickle             | 10.0 us                                                | 9.11 us: 1.10x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 51.5 ms: 1.06x faster                                  |
| json_loads           | 17.0 us                                                | 16.4 us: 1.04x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 98.0 ms: 1.02x faster                                  |
| pickle_list          | 2.83 us                                                | 2.87 us: 1.02x slower                                  |
| pickle_dict          | 18.0 us                                                | 18.4 us: 1.03x slower                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 71.2 ms: 1.03x slower                                  |
| Geometric mean       | (ref)                                                  | 1.11x faster                                           |

Benchmark hidden because not significant (2): unpickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 11.2 ms: 1.16x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 9.23 ms: 1.32x slower                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.39 ms: 1.43x faster                                  |
| genshi_xml      | 37.7 ms                                                | 29.5 ms: 1.28x faster                                  |
| django_template | 27.2 ms                                                | 21.7 ms: 1.25x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.7 ms: 1.23x faster                                  |
| Geometric mean  | (ref)                                                  | 1.30x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.60 ms: 2.07x faster                                  |
| logging_silent          | 119 ns                                                 | 67.3 ns: 1.77x faster                                  |
| richards                | 51.4 ms                                                | 31.4 ms: 1.64x faster                                  |
| nbody                   | 94.6 ms                                                | 60.4 ms: 1.57x faster                                  |
| scimark_lu              | 110 ms                                                 | 71.5 ms: 1.53x faster                                  |
| raytrace                | 329 ms                                                 | 221 ms: 1.49x faster                                   |
| sqlglot_parse           | 1.33 ms                                                | 906 us: 1.46x faster                                   |
| pickle_pure_python      | 284 us                                                 | 194 us: 1.46x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 335 ms: 1.45x faster                                   |
| mako                    | 10.6 ms                                                | 7.39 ms: 1.43x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.08 ms: 1.43x faster                                  |
| scimark_sor             | 126 ms                                                 | 88.2 ms: 1.43x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 54.7 ms: 1.42x faster                                  |
| go                      | 165 ms                                                 | 116 ms: 1.42x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.46 ms: 1.42x faster                                  |
| chaos                   | 66.5 ms                                                | 47.3 ms: 1.41x faster                                  |
| async_tree_none         | 396 ms                                                 | 286 ms: 1.38x faster                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 52.5 ms: 1.38x faster                                  |
| async_tree_io           | 1.01 sec                                               | 735 ms: 1.37x faster                                   |
| unpickle_pure_python    | 204 us                                                 | 149 us: 1.37x faster                                   |
| float                   | 72.1 ms                                                | 52.9 ms: 1.36x faster                                  |
| pycparser               | 915 ms                                                 | 682 ms: 1.34x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.27 ms: 1.33x faster                                  |
| pyflate                 | 454 ms                                                 | 342 ms: 1.33x faster                                   |
| deepcopy_memo           | 34.4 us                                                | 25.9 us: 1.33x faster                                  |
| 2to3                    | 222 ms                                                 | 168 ms: 1.32x faster                                   |
| spectral_norm           | 95.8 ms                                                | 73.1 ms: 1.31x faster                                  |
| chameleon               | 5.86 ms                                                | 4.50 ms: 1.30x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 968 ms: 1.28x faster                                   |
| genshi_xml              | 37.7 ms                                                | 29.5 ms: 1.28x faster                                  |
| pprint_safe_repr        | 608 ms                                                 | 475 ms: 1.28x faster                                   |
| tornado_http            | 90.1 ms                                                | 71.0 ms: 1.27x faster                                  |
| thrift                  | 577 us                                                 | 458 us: 1.26x faster                                   |
| regex_compile           | 96.2 ms                                                | 76.7 ms: 1.26x faster                                  |
| django_template         | 27.2 ms                                                | 21.7 ms: 1.25x faster                                  |
| deepcopy                | 278 us                                                 | 223 us: 1.25x faster                                   |
| logging_simple          | 4.61 us                                                | 3.71 us: 1.24x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.7 ms: 1.23x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.82 ms: 1.23x faster                                  |
| scimark_fft             | 231 ms                                                 | 189 ms: 1.22x faster                                   |
| xml_etree_process       | 45.1 ms                                                | 36.8 ms: 1.22x faster                                  |
| logging_format          | 4.95 us                                                | 4.05 us: 1.22x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 545 ms: 1.22x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.95 us: 1.21x faster                                  |
| dulwich_log             | 36.4 ms                                                | 30.1 ms: 1.21x faster                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.47 ms: 1.21x faster                                  |
| html5lib                | 44.0 ms                                                | 36.6 ms: 1.20x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 32.0 ms: 1.19x faster                                  |
| fannkuch                | 318 ms                                                 | 269 ms: 1.18x faster                                   |
| docutils                | 1.76 sec                                               | 1.50 sec: 1.18x faster                                 |
| unpack_sequence         | 38.2 ns                                                | 32.9 ns: 1.16x faster                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.6 ms: 1.15x faster                                  |
| generators              | 32.5 ms                                                | 28.2 ms: 1.15x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 176 ms: 1.13x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.8 ms: 1.13x faster                                  |
| bench_thread_pool       | 531 us                                                 | 472 us: 1.12x faster                                   |
| json                    | 3.13 ms                                                | 2.80 ms: 1.12x faster                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| sympy_expand            | 275 ms                                                 | 250 ms: 1.10x faster                                   |
| unpickle                | 10.0 us                                                | 9.11 us: 1.10x faster                                  |
| sqlite_synth            | 1.50 us                                                | 1.37 us: 1.10x faster                                  |
| sympy_str               | 169 ms                                                 | 156 ms: 1.09x faster                                   |
| regex_dna               | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| nqueens                 | 68.6 ms                                                | 63.4 ms: 1.08x faster                                  |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                 |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                  |
| meteor_contest          | 77.7 ms                                                | 73.2 ms: 1.06x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 51.5 ms: 1.06x faster                                  |
| telco                   | 3.63 ms                                                | 3.44 ms: 1.06x faster                                  |
| sympy_sum               | 93.5 ms                                                | 88.6 ms: 1.06x faster                                  |
| json_loads              | 17.0 us                                                | 16.4 us: 1.04x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 98.0 ms: 1.02x faster                                  |
| pidigits                | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| pickle_list             | 2.83 us                                                | 2.87 us: 1.02x slower                                  |
| pickle_dict             | 18.0 us                                                | 18.4 us: 1.03x slower                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 71.2 ms: 1.03x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.67 ms: 1.09x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 45.4 ms: 1.11x slower                                  |
| async_generators        | 231 ms                                                 | 264 ms: 1.14x slower                                   |
| python_startup          | 9.59 ms                                                | 11.2 ms: 1.16x slower                                  |
| pathlib                 | 22.2 ms                                                | 28.1 ms: 1.27x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 9.23 ms: 1.32x slower                                  |
| coverage                | 40.8 ms                                                | 60.9 ms: 1.49x slower                                  |
| Geometric mean          | (ref)                                                  | 1.20x faster                                           |

Benchmark hidden because not significant (2): unpickle_list, pickle
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230408-3.12.0a7+-3516704/bm-20230408-darwin-arm64-python-main-3.12.0a7+-3516704.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
