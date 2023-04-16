
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 4fe1c4b
- commit date: 2023-04-15
- overall geometric mean: 1.25x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 161 ms: 1.38x faster                                   |
| chameleon      | 5.86 ms                                                | 4.23 ms: 1.38x faster                                  |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.21x faster                                 |
| html5lib       | 44.0 ms                                                | 34.9 ms: 1.26x faster                                  |
| tornado_http   | 90.1 ms                                                | 68.5 ms: 1.31x faster                                  |
| Geometric mean | (ref)                                                  | 1.31x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 56.7 ms: 1.67x faster                                  |
| float          | 72.1 ms                                                | 50.9 ms: 1.42x faster                                  |
| pidigits       | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.34x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 72.3 ms: 1.33x faster                                  |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.61 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 182 us: 1.56x faster                                   |
| unpickle_pure_python | 204 us                                                 | 137 us: 1.49x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.04 ms: 1.38x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 34.5 ms: 1.31x faster                                  |
| unpickle             | 10.0 us                                                | 8.99 us: 1.12x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 49.0 ms: 1.11x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 97.5 ms: 1.03x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.62 us: 1.02x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 68.4 ms: 1.01x faster                                  |
| pickle_list          | 2.83 us                                                | 2.91 us: 1.03x slower                                  |
| pickle_dict          | 18.0 us                                                | 18.5 us: 1.03x slower                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 11.5 ms: 1.20x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 9.51 ms: 1.36x slower                                  |
| Geometric mean         | (ref)                                                  | 1.28x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.04 ms: 1.51x faster                                  |
| genshi_xml      | 37.7 ms                                                | 26.4 ms: 1.43x faster                                  |
| genshi_text     | 18.2 ms                                                | 13.4 ms: 1.36x faster                                  |
| django_template | 27.2 ms                                                | 20.2 ms: 1.35x faster                                  |
| Geometric mean  | (ref)                                                  | 1.41x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.50 ms: 2.15x faster                                  |
| logging_silent          | 119 ns                                                 | 62.1 ns: 1.92x faster                                  |
| richards                | 51.4 ms                                                | 30.7 ms: 1.68x faster                                  |
| nbody                   | 94.6 ms                                                | 56.7 ms: 1.67x faster                                  |
| scimark_lu              | 110 ms                                                 | 67.3 ms: 1.63x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 831 us: 1.60x faster                                   |
| pickle_pure_python      | 284 us                                                 | 182 us: 1.56x faster                                   |
| raytrace                | 329 ms                                                 | 212 ms: 1.56x faster                                   |
| sqlglot_transpile       | 1.54 ms                                                | 992 us: 1.55x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.10 ms: 1.54x faster                                  |
| scimark_sor             | 126 ms                                                 | 81.8 ms: 1.54x faster                                  |
| async_tree_memoization  | 485 ms                                                 | 320 ms: 1.52x faster                                   |
| mako                    | 10.6 ms                                                | 7.04 ms: 1.51x faster                                  |
| go                      | 165 ms                                                 | 110 ms: 1.50x faster                                   |
| unpickle_pure_python    | 204 us                                                 | 137 us: 1.49x faster                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 48.9 ms: 1.48x faster                                  |
| chaos                   | 66.5 ms                                                | 45.2 ms: 1.47x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.4 ms: 1.46x faster                                  |
| generators              | 32.5 ms                                                | 22.5 ms: 1.44x faster                                  |
| genshi_xml              | 37.7 ms                                                | 26.4 ms: 1.43x faster                                  |
| async_tree_none         | 396 ms                                                 | 277 ms: 1.43x faster                                   |
| float                   | 72.1 ms                                                | 50.9 ms: 1.42x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 24.3 us: 1.41x faster                                  |
| spectral_norm           | 95.8 ms                                                | 67.8 ms: 1.41x faster                                  |
| async_tree_io           | 1.01 sec                                               | 716 ms: 1.41x faster                                   |
| pycparser               | 915 ms                                                 | 658 ms: 1.39x faster                                   |
| pyflate                 | 454 ms                                                 | 327 ms: 1.39x faster                                   |
| 2to3                    | 222 ms                                                 | 161 ms: 1.38x faster                                   |
| chameleon               | 5.86 ms                                                | 4.23 ms: 1.38x faster                                  |
| pprint_safe_repr        | 608 ms                                                 | 440 ms: 1.38x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.04 ms: 1.38x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 902 ms: 1.37x faster                                   |
| genshi_text             | 18.2 ms                                                | 13.4 ms: 1.36x faster                                  |
| django_template         | 27.2 ms                                                | 20.2 ms: 1.35x faster                                  |
| regex_compile           | 96.2 ms                                                | 72.3 ms: 1.33x faster                                  |
| logging_simple          | 4.61 us                                                | 3.46 us: 1.33x faster                                  |
| deepcopy                | 278 us                                                 | 211 us: 1.32x faster                                   |
| tornado_http            | 90.1 ms                                                | 68.5 ms: 1.31x faster                                  |
| thrift                  | 577 us                                                 | 440 us: 1.31x faster                                   |
| xml_etree_process       | 45.1 ms                                                | 34.5 ms: 1.31x faster                                  |
| logging_format          | 4.95 us                                                | 3.79 us: 1.31x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 29.5 ns: 1.29x faster                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.83 us: 1.29x faster                                  |
| scimark_fft             | 231 ms                                                 | 179 ms: 1.29x faster                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.71 ms: 1.28x faster                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.07 ms: 1.27x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 29.9 ms: 1.27x faster                                  |
| html5lib                | 44.0 ms                                                | 34.9 ms: 1.26x faster                                  |
| dulwich_log             | 36.4 ms                                                | 29.2 ms: 1.25x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 533 ms: 1.25x faster                                   |
| fannkuch                | 318 ms                                                 | 257 ms: 1.24x faster                                   |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.21x faster                                 |
| sqlglot_normalize       | 198 ms                                                 | 164 ms: 1.21x faster                                   |
| sqlalchemy_declarative  | 74.4 ms                                                | 61.6 ms: 1.21x faster                                  |
| sympy_integrate         | 13.3 ms                                                | 11.2 ms: 1.18x faster                                  |
| pylint                  | 302 ms                                                 | 256 ms: 1.18x faster                                   |
| coroutines              | 20.1 ms                                                | 17.2 ms: 1.17x faster                                  |
| bench_thread_pool       | 531 us                                                 | 455 us: 1.17x faster                                   |
| sympy_expand            | 275 ms                                                 | 237 ms: 1.16x faster                                   |
| nqueens                 | 68.6 ms                                                | 59.9 ms: 1.14x faster                                  |
| sympy_str               | 169 ms                                                 | 148 ms: 1.14x faster                                   |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                  |
| json                    | 3.13 ms                                                | 2.78 ms: 1.12x faster                                  |
| unpickle                | 10.0 us                                                | 8.99 us: 1.12x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 49.0 ms: 1.11x faster                                  |
| sqlite_synth            | 1.50 us                                                | 1.35 us: 1.11x faster                                  |
| mdp                     | 1.66 sec                                               | 1.50 sec: 1.11x faster                                 |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| sympy_sum               | 93.5 ms                                                | 84.9 ms: 1.10x faster                                  |
| meteor_contest          | 77.7 ms                                                | 71.3 ms: 1.09x faster                                  |
| telco                   | 3.63 ms                                                | 3.36 ms: 1.08x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 97.5 ms: 1.03x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.62 us: 1.02x faster                                  |
| pidigits                | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| xml_etree_iterparse     | 69.0 ms                                                | 68.4 ms: 1.01x faster                                  |
| pickle_list             | 2.83 us                                                | 2.91 us: 1.03x slower                                  |
| pickle_dict             | 18.0 us                                                | 18.5 us: 1.03x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.61 ms: 1.06x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 45.1 ms: 1.11x slower                                  |
| async_generators        | 231 ms                                                 | 257 ms: 1.12x slower                                   |
| python_startup          | 9.59 ms                                                | 11.5 ms: 1.20x slower                                  |
| pathlib                 | 22.2 ms                                                | 27.2 ms: 1.22x slower                                  |
| coverage                | 40.8 ms                                                | 52.1 ms: 1.28x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 9.51 ms: 1.36x slower                                  |
| Geometric mean          | (ref)                                                  | 1.25x faster                                           |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy
Ignored benchmarks (6) of public/results/bm-20230415-3.12.0a7+-4fe1c4b/bm-20230415-darwin-arm64-python-main-3.12.0a7+-4fe1c4b.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
