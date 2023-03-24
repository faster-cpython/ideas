
# Results vs. 3.10.4

- fork: python
- ref: f3cb15c88afa2e87067d
- machine: darwin-arm64
- commit hash: f3cb15c
- commit date: 2023-02-26
- overall geometric mean: 1.20x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 164 ms: 1.36x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.41 ms: 1.33x faster                                                  |
| docutils       | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                 |
| html5lib       | 44.0 ms                                                | 35.7 ms: 1.23x faster                                                  |
| tornado_http   | 90.1 ms                                                | 71.3 ms: 1.26x faster                                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 63.9 ms: 1.48x faster                                                  |
| float          | 72.1 ms                                                | 53.0 ms: 1.36x faster                                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.2 ms: 1.28x faster                                                  |
| regex_v8       | 17.7 ms                                                | 16.0 ms: 1.11x faster                                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.69 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 195 us: 1.46x faster                                                   |
| unpickle_pure_python | 204 us                                                 | 142 us: 1.43x faster                                                   |
| json_dumps           | 8.34 ms                                                | 6.22 ms: 1.34x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 36.2 ms: 1.24x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 50.7 ms: 1.07x faster                                                  |
| json_loads           | 17.0 us                                                | 15.9 us: 1.07x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.7 ms: 1.03x faster                                                  |
| unpickle             | 10.0 us                                                | 9.73 us: 1.03x faster                                                  |
| pickle               | 7.50 us                                                | 7.54 us: 1.01x slower                                                  |
| pickle_dict          | 18.0 us                                                | 18.1 us: 1.01x slower                                                  |
| unpickle_list        | 2.66 us                                                | 2.69 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.2 ms: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.5 ms: 1.30x slower                                                  |
| python_startup_no_site | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.39x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.43 ms: 1.43x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 28.4 ms: 1.33x faster                                                  |
| django_template | 27.2 ms                                                | 21.4 ms: 1.27x faster                                                  |
| genshi_text     | 18.2 ms                                                | 14.4 ms: 1.26x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.32x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.56 ms: 2.10x faster                                                  |
| logging_silent          | 119 ns                                                 | 66.9 ns: 1.78x faster                                                  |
| richards                | 51.4 ms                                                | 30.4 ms: 1.69x faster                                                  |
| go                      | 165 ms                                                 | 109 ms: 1.51x faster                                                   |
| scimark_lu              | 110 ms                                                 | 73.5 ms: 1.49x faster                                                  |
| nbody                   | 94.6 ms                                                | 63.9 ms: 1.48x faster                                                  |
| raytrace                | 329 ms                                                 | 223 ms: 1.48x faster                                                   |
| pickle_pure_python      | 284 us                                                 | 195 us: 1.46x faster                                                   |
| crypto_pyaes            | 77.9 ms                                                | 53.6 ms: 1.46x faster                                                  |
| scimark_sor             | 126 ms                                                 | 86.7 ms: 1.45x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.35 ms: 1.45x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 335 ms: 1.45x faster                                                   |
| unpickle_pure_python    | 204 us                                                 | 142 us: 1.43x faster                                                   |
| mako                    | 10.6 ms                                                | 7.43 ms: 1.43x faster                                                  |
| chaos                   | 66.5 ms                                                | 47.6 ms: 1.40x faster                                                  |
| pyflate                 | 454 ms                                                 | 328 ms: 1.38x faster                                                   |
| async_tree_none         | 396 ms                                                 | 288 ms: 1.37x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 738 ms: 1.37x faster                                                   |
| pycparser               | 915 ms                                                 | 668 ms: 1.37x faster                                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 53.2 ms: 1.36x faster                                                  |
| float                   | 72.1 ms                                                | 53.0 ms: 1.36x faster                                                  |
| 2to3                    | 222 ms                                                 | 164 ms: 1.36x faster                                                   |
| json_dumps              | 8.34 ms                                                | 6.22 ms: 1.34x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 25.7 us: 1.34x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 28.4 ms: 1.33x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.41 ms: 1.33x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 964 ms: 1.29x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 473 ms: 1.28x faster                                                   |
| regex_compile           | 96.2 ms                                                | 75.2 ms: 1.28x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.61 us: 1.28x faster                                                  |
| django_template         | 27.2 ms                                                | 21.4 ms: 1.27x faster                                                  |
| generators              | 32.5 ms                                                | 25.5 ms: 1.27x faster                                                  |
| thrift                  | 577 us                                                 | 454 us: 1.27x faster                                                   |
| spectral_norm           | 95.8 ms                                                | 75.5 ms: 1.27x faster                                                  |
| logging_format          | 4.95 us                                                | 3.91 us: 1.27x faster                                                  |
| tornado_http            | 90.1 ms                                                | 71.3 ms: 1.26x faster                                                  |
| genshi_text             | 18.2 ms                                                | 14.4 ms: 1.26x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.23 ms: 1.25x faster                                                  |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                                   |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.22 ms: 1.25x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.06 ms: 1.25x faster                                                  |
| fannkuch                | 318 ms                                                 | 255 ms: 1.25x faster                                                   |
| xml_etree_process       | 45.1 ms                                                | 36.2 ms: 1.24x faster                                                  |
| html5lib                | 44.0 ms                                                | 35.7 ms: 1.23x faster                                                  |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 542 ms: 1.23x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.95 us: 1.21x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.7 ms: 1.20x faster                                                  |
| docutils                | 1.76 sec                                               | 1.49 sec: 1.18x faster                                                 |
| scimark_fft             | 231 ms                                                 | 197 ms: 1.17x faster                                                   |
| sqlalchemy_declarative  | 74.4 ms                                                | 63.8 ms: 1.16x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 33.2 ns: 1.15x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 173 ms: 1.15x faster                                                   |
| sympy_integrate         | 13.3 ms                                                | 11.6 ms: 1.14x faster                                                  |
| bench_thread_pool       | 531 us                                                 | 466 us: 1.14x faster                                                   |
| coroutines              | 20.1 ms                                                | 17.7 ms: 1.14x faster                                                  |
| json                    | 3.13 ms                                                | 2.78 ms: 1.12x faster                                                  |
| sympy_expand            | 275 ms                                                 | 245 ms: 1.12x faster                                                   |
| nqueens                 | 68.6 ms                                                | 61.9 ms: 1.11x faster                                                  |
| regex_v8                | 17.7 ms                                                | 16.0 ms: 1.11x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                                  |
| sympy_str               | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.19 ms: 1.09x faster                                                  |
| regex_dna               | 164 ms                                                 | 152 ms: 1.08x faster                                                   |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 50.7 ms: 1.07x faster                                                  |
| json_loads              | 17.0 us                                                | 15.9 us: 1.07x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 88.2 ms: 1.06x faster                                                  |
| telco                   | 3.63 ms                                                | 3.49 ms: 1.04x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.7 ms: 1.03x faster                                                  |
| unpickle                | 10.0 us                                                | 9.73 us: 1.03x faster                                                  |
| meteor_contest          | 77.7 ms                                                | 76.1 ms: 1.02x faster                                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| pickle                  | 7.50 us                                                | 7.54 us: 1.01x slower                                                  |
| pickle_dict             | 18.0 us                                                | 18.1 us: 1.01x slower                                                  |
| unpickle_list           | 2.66 us                                                | 2.69 us: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.2 ms: 1.02x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.69 ms: 1.10x slower                                                  |
| bench_mp_pool           | 40.8 ms                                                | 46.3 ms: 1.14x slower                                                  |
| async_generators        | 231 ms                                                 | 266 ms: 1.16x slower                                                   |
| pathlib                 | 22.2 ms                                                | 27.2 ms: 1.23x slower                                                  |
| python_startup          | 9.59 ms                                                | 12.5 ms: 1.30x slower                                                  |
| coverage                | 40.8 ms                                                | 60.3 ms: 1.48x slower                                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.20x faster                                                           |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230226-3.12.0a5+-f3cb15c/bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5+-f3cb15c.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
