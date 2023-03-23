
# Results vs. 3.10.4

- fork: python
- ref: b1b375e2670a58fc37cb
- machine: darwin-arm64
- commit hash: b1b375e
- commit date: 2023-02-19
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 162 ms: 1.38x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.44 ms: 1.32x faster                                                  |
| docutils       | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                 |
| html5lib       | 44.0 ms                                                | 35.8 ms: 1.23x faster                                                  |
| tornado_http   | 90.1 ms                                                | 70.3 ms: 1.28x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.1 ms: 1.48x faster                                                  |
| float          | 72.1 ms                                                | 52.4 ms: 1.38x faster                                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 73.0 ms: 1.32x faster                                                  |
| regex_v8       | 17.7 ms                                                | 15.8 ms: 1.12x faster                                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 195 us: 1.46x faster                                                   |
| unpickle_pure_python | 204 us                                                 | 143 us: 1.43x faster                                                   |
| json_dumps           | 8.34 ms                                                | 6.15 ms: 1.36x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 36.0 ms: 1.25x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 50.3 ms: 1.08x faster                                                  |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| unpickle             | 10.0 us                                                | 9.65 us: 1.04x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.57 us: 1.04x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 97.6 ms: 1.03x faster                                                  |
| pickle_dict          | 18.0 us                                                | 18.1 us: 1.01x slower                                                  |
| pickle               | 7.50 us                                                | 7.56 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.9 ms: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                  |
| python_startup_no_site | 7.00 ms                                                | 10.4 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.39x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.36 ms: 1.44x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 28.3 ms: 1.33x faster                                                  |
| django_template | 27.2 ms                                                | 21.3 ms: 1.28x faster                                                  |
| genshi_text     | 18.2 ms                                                | 14.3 ms: 1.27x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.33x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.57 ms: 2.09x faster                                                  |
| logging_silent          | 119 ns                                                 | 65.8 ns: 1.81x faster                                                  |
| richards                | 51.4 ms                                                | 30.0 ms: 1.71x faster                                                  |
| go                      | 165 ms                                                 | 109 ms: 1.51x faster                                                   |
| scimark_lu              | 110 ms                                                 | 73.3 ms: 1.50x faster                                                  |
| raytrace                | 329 ms                                                 | 223 ms: 1.48x faster                                                   |
| nbody                   | 94.6 ms                                                | 64.1 ms: 1.48x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 329 ms: 1.47x faster                                                   |
| hexiom                  | 6.31 ms                                                | 4.31 ms: 1.46x faster                                                  |
| pickle_pure_python      | 284 us                                                 | 195 us: 1.46x faster                                                   |
| scimark_sor             | 126 ms                                                 | 86.5 ms: 1.46x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.5 ms: 1.46x faster                                                  |
| mako                    | 10.6 ms                                                | 7.36 ms: 1.44x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 143 us: 1.43x faster                                                   |
| chaos                   | 66.5 ms                                                | 46.6 ms: 1.43x faster                                                  |
| pyflate                 | 454 ms                                                 | 328 ms: 1.38x faster                                                   |
| async_tree_none         | 396 ms                                                 | 286 ms: 1.38x faster                                                   |
| 2to3                    | 222 ms                                                 | 162 ms: 1.38x faster                                                   |
| float                   | 72.1 ms                                                | 52.4 ms: 1.38x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 52.7 ms: 1.37x faster                                                  |
| pycparser               | 915 ms                                                 | 669 ms: 1.37x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 745 ms: 1.36x faster                                                   |
| json_dumps              | 8.34 ms                                                | 6.15 ms: 1.36x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 25.5 us: 1.35x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 28.3 ms: 1.33x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.44 ms: 1.32x faster                                                  |
| regex_compile           | 96.2 ms                                                | 73.0 ms: 1.32x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 954 ms: 1.30x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 468 ms: 1.30x faster                                                   |
| tornado_http            | 90.1 ms                                                | 70.3 ms: 1.28x faster                                                  |
| django_template         | 27.2 ms                                                | 21.3 ms: 1.28x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 75.2 ms: 1.27x faster                                                  |
| generators              | 32.5 ms                                                | 25.5 ms: 1.27x faster                                                  |
| genshi_text             | 18.2 ms                                                | 14.3 ms: 1.27x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.64 us: 1.27x faster                                                  |
| logging_format          | 4.95 us                                                | 3.91 us: 1.26x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.05 ms: 1.26x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.22 ms: 1.26x faster                                                  |
| deepcopy                | 278 us                                                 | 221 us: 1.26x faster                                                   |
| thrift                  | 577 us                                                 | 461 us: 1.25x faster                                                   |
| xml_etree_process       | 45.1 ms                                                | 36.0 ms: 1.25x faster                                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.23 ms: 1.25x faster                                                  |
| fannkuch                | 318 ms                                                 | 257 ms: 1.24x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.91 us: 1.24x faster                                                  |
| dulwich_log             | 36.4 ms                                                | 29.5 ms: 1.23x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.82 ms: 1.23x faster                                                  |
| html5lib                | 44.0 ms                                                | 35.8 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 542 ms: 1.23x faster                                                   |
| sqlglot_optimize        | 38.1 ms                                                | 31.9 ms: 1.19x faster                                                  |
| scimark_fft             | 231 ms                                                 | 194 ms: 1.19x faster                                                   |
| docutils                | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                 |
| sympy_integrate         | 13.3 ms                                                | 11.3 ms: 1.17x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 63.9 ms: 1.16x faster                                                  |
| sympy_str               | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                                   |
| bench_thread_pool       | 531 us                                                 | 466 us: 1.14x faster                                                   |
| sympy_expand            | 275 ms                                                 | 243 ms: 1.13x faster                                                   |
| coroutines              | 20.1 ms                                                | 17.8 ms: 1.13x faster                                                  |
| json                    | 3.13 ms                                                | 2.77 ms: 1.13x faster                                                  |
| regex_v8                | 17.7 ms                                                | 15.8 ms: 1.12x faster                                                  |
| nqueens                 | 68.6 ms                                                | 61.1 ms: 1.12x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 83.8 ms: 1.12x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.35 us: 1.11x faster                                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| xml_etree_generate      | 54.5 ms                                                | 50.3 ms: 1.08x faster                                                  |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                                 |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| telco                   | 3.63 ms                                                | 3.48 ms: 1.04x faster                                                  |
| unpickle                | 10.0 us                                                | 9.65 us: 1.04x faster                                                  |
| unpickle_list           | 2.66 us                                                | 2.57 us: 1.04x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 97.6 ms: 1.03x faster                                                  |
| meteor_contest          | 77.7 ms                                                | 76.3 ms: 1.02x faster                                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| pickle_dict             | 18.0 us                                                | 18.1 us: 1.01x slower                                                  |
| pickle                  | 7.50 us                                                | 7.56 us: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.9 ms: 1.03x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                  |
| bench_mp_pool           | 40.8 ms                                                | 46.2 ms: 1.13x slower                                                  |
| async_generators        | 231 ms                                                 | 264 ms: 1.14x slower                                                   |
| pathlib                 | 22.2 ms                                                | 27.0 ms: 1.22x slower                                                  |
| python_startup          | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.4 ms: 1.49x slower                                                  |
| coverage                | 40.8 ms                                                | 60.9 ms: 1.49x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                           |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230219-3.12.0a5+-b1b375e/bm-20230219-darwin-arm64-python-b1b375e2670a58fc37cb-3.12.0a5+-b1b375e.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
