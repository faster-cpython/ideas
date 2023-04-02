
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 06249ec
- commit date: 2023-04-01
- overall geometric mean: 1.19x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 168 ms: 1.32x faster                                   |
| chameleon      | 5.86 ms                                                | 4.50 ms: 1.30x faster                                  |
| docutils       | 1.76 sec                                               | 1.49 sec: 1.18x faster                                 |
| html5lib       | 44.0 ms                                                | 36.8 ms: 1.20x faster                                  |
| tornado_http   | 90.1 ms                                                | 69.7 ms: 1.29x faster                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 60.4 ms: 1.57x faster                                  |
| float          | 72.1 ms                                                | 53.1 ms: 1.36x faster                                  |
| pidigits       | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.8 ms: 1.25x faster                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.70 ms: 1.10x slower                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 193 us: 1.47x faster                                   |
| unpickle_pure_python | 204 us                                                 | 148 us: 1.37x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.23 ms: 1.34x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 36.8 ms: 1.22x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 51.3 ms: 1.06x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| unpickle             | 10.0 us                                                | 9.67 us: 1.04x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 99.1 ms: 1.01x faster                                  |
| pickle               | 7.50 us                                                | 7.47 us: 1.00x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.69 us: 1.01x slower                                  |
| pickle_list          | 2.83 us                                                | 2.91 us: 1.03x slower                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 71.3 ms: 1.03x slower                                  |
| Geometric mean       | (ref)                                                  | 1.10x faster                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.4 ms: 1.29x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 10.2 ms: 1.46x slower                                  |
| Geometric mean         | (ref)                                                  | 1.37x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.40 ms: 1.43x faster                                  |
| genshi_xml      | 37.7 ms                                                | 29.4 ms: 1.28x faster                                  |
| django_template | 27.2 ms                                                | 21.8 ms: 1.25x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.8 ms: 1.23x faster                                  |
| Geometric mean  | (ref)                                                  | 1.30x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.61 ms: 2.06x faster                                  |
| logging_silent          | 119 ns                                                 | 66.8 ns: 1.79x faster                                  |
| richards                | 51.4 ms                                                | 31.4 ms: 1.64x faster                                  |
| nbody                   | 94.6 ms                                                | 60.4 ms: 1.57x faster                                  |
| scimark_lu              | 110 ms                                                 | 71.4 ms: 1.54x faster                                  |
| raytrace                | 329 ms                                                 | 222 ms: 1.48x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 330 ms: 1.47x faster                                   |
| pickle_pure_python      | 284 us                                                 | 193 us: 1.47x faster                                   |
| mako                    | 10.6 ms                                                | 7.40 ms: 1.43x faster                                  |
| scimark_sor             | 126 ms                                                 | 88.3 ms: 1.43x faster                                  |
| hexiom                  | 6.31 ms                                                | 4.43 ms: 1.42x faster                                  |
| go                      | 165 ms                                                 | 116 ms: 1.42x faster                                   |
| crypto_pyaes            | 77.9 ms                                                | 54.9 ms: 1.42x faster                                  |
| chaos                   | 66.5 ms                                                | 47.5 ms: 1.40x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 148 us: 1.37x faster                                   |
| async_tree_none         | 396 ms                                                 | 289 ms: 1.37x faster                                   |
| async_tree_io           | 1.01 sec                                               | 739 ms: 1.37x faster                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 53.0 ms: 1.36x faster                                  |
| float                   | 72.1 ms                                                | 53.1 ms: 1.36x faster                                  |
| pycparser               | 915 ms                                                 | 680 ms: 1.34x faster                                   |
| json_dumps              | 8.34 ms                                                | 6.23 ms: 1.34x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 26.0 us: 1.32x faster                                  |
| pyflate                 | 454 ms                                                 | 343 ms: 1.32x faster                                   |
| 2to3                    | 222 ms                                                 | 168 ms: 1.32x faster                                   |
| spectral_norm           | 95.8 ms                                                | 73.1 ms: 1.31x faster                                  |
| chameleon               | 5.86 ms                                                | 4.50 ms: 1.30x faster                                  |
| tornado_http            | 90.1 ms                                                | 69.7 ms: 1.29x faster                                  |
| genshi_xml              | 37.7 ms                                                | 29.4 ms: 1.28x faster                                  |
| pprint_safe_repr        | 608 ms                                                 | 477 ms: 1.27x faster                                   |
| pprint_pformat          | 1.24 sec                                               | 973 ms: 1.27x faster                                   |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                   |
| regex_compile           | 96.2 ms                                                | 76.8 ms: 1.25x faster                                  |
| logging_simple          | 4.61 us                                                | 3.68 us: 1.25x faster                                  |
| django_template         | 27.2 ms                                                | 21.8 ms: 1.25x faster                                  |
| logging_format          | 4.95 us                                                | 3.97 us: 1.24x faster                                  |
| thrift                  | 577 us                                                 | 464 us: 1.24x faster                                   |
| sqlglot_parse           | 1.33 ms                                                | 1.07 ms: 1.24x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.25 ms: 1.24x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.8 ms: 1.23x faster                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.34 ms: 1.23x faster                                  |
| scimark_fft             | 231 ms                                                 | 188 ms: 1.23x faster                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.83 ms: 1.23x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 36.8 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 545 ms: 1.22x faster                                   |
| dulwich_log             | 36.4 ms                                                | 30.0 ms: 1.22x faster                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.95 us: 1.21x faster                                  |
| html5lib                | 44.0 ms                                                | 36.8 ms: 1.20x faster                                  |
| docutils                | 1.76 sec                                               | 1.49 sec: 1.18x faster                                 |
| sqlglot_optimize        | 38.1 ms                                                | 32.3 ms: 1.18x faster                                  |
| generators              | 32.5 ms                                                | 27.6 ms: 1.18x faster                                  |
| fannkuch                | 318 ms                                                 | 271 ms: 1.18x faster                                   |
| unpack_sequence         | 38.2 ns                                                | 32.9 ns: 1.16x faster                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.4 ms: 1.15x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 176 ms: 1.13x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.8 ms: 1.13x faster                                  |
| bench_thread_pool       | 531 us                                                 | 472 us: 1.12x faster                                   |
| json                    | 3.13 ms                                                | 2.80 ms: 1.12x faster                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| sympy_expand            | 275 ms                                                 | 250 ms: 1.10x faster                                   |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                  |
| sympy_str               | 169 ms                                                 | 156 ms: 1.09x faster                                   |
| nqueens                 | 68.6 ms                                                | 63.3 ms: 1.08x faster                                  |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                 |
| regex_dna               | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| meteor_contest          | 77.7 ms                                                | 72.7 ms: 1.07x faster                                  |
| coroutines              | 20.1 ms                                                | 18.9 ms: 1.07x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 51.3 ms: 1.06x faster                                  |
| sympy_sum               | 93.5 ms                                                | 88.8 ms: 1.05x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| unpickle                | 10.0 us                                                | 9.67 us: 1.04x faster                                  |
| telco                   | 3.63 ms                                                | 3.54 ms: 1.02x faster                                  |
| pidigits                | 284 ms                                                 | 280 ms: 1.01x faster                                   |
| xml_etree_parse         | 100 ms                                                 | 99.1 ms: 1.01x faster                                  |
| pickle                  | 7.50 us                                                | 7.47 us: 1.00x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.69 us: 1.01x slower                                  |
| pickle_list             | 2.83 us                                                | 2.91 us: 1.03x slower                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 71.3 ms: 1.03x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.70 ms: 1.10x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 46.4 ms: 1.14x slower                                  |
| async_generators        | 231 ms                                                 | 265 ms: 1.15x slower                                   |
| pathlib                 | 22.2 ms                                                | 27.6 ms: 1.24x slower                                  |
| python_startup          | 9.59 ms                                                | 12.4 ms: 1.29x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.2 ms: 1.46x slower                                  |
| coverage                | 40.8 ms                                                | 60.5 ms: 1.48x slower                                  |
| Geometric mean          | (ref)                                                  | 1.19x faster                                           |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230401-3.12.0a6+-06249ec/bm-20230401-darwin-arm64-python-main-3.12.0a6+-06249ec.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
