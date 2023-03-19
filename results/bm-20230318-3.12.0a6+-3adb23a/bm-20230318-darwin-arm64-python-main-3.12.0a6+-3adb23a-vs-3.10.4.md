
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 3adb23a
- commit date: 2023-03-18
- overall geometric mean: 1.20x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 165 ms: 1.35x faster                                   |
| chameleon      | 5.86 ms                                                | 4.48 ms: 1.31x faster                                  |
| docutils       | 1.76 sec                                               | 1.51 sec: 1.17x faster                                 |
| html5lib       | 44.0 ms                                                | 35.7 ms: 1.23x faster                                  |
| tornado_http   | 90.1 ms                                                | 69.5 ms: 1.30x faster                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 60.7 ms: 1.56x faster                                  |
| float          | 72.1 ms                                                | 52.7 ms: 1.37x faster                                  |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.9 ms: 1.27x faster                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| regex_dna      | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.68 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 192 us: 1.48x faster                                   |
| unpickle_pure_python | 204 us                                                 | 145 us: 1.40x faster                                   |
| json_dumps           | 8.34 ms                                                | 6.28 ms: 1.33x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 36.7 ms: 1.23x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 51.8 ms: 1.05x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| xml_etree_parse      | 100 ms                                                 | 97.4 ms: 1.03x faster                                  |
| unpickle             | 10.0 us                                                | 9.77 us: 1.03x faster                                  |
| pickle               | 7.50 us                                                | 7.41 us: 1.01x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.64 us: 1.01x faster                                  |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.3 ms: 1.02x slower                                  |
| Geometric mean       | (ref)                                                  | 1.11x faster                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 11.0 ms: 1.14x slower                                  |
| python_startup_no_site | 7.00 ms                                                | 8.99 ms: 1.28x slower                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.44 ms: 1.43x faster                                  |
| genshi_xml      | 37.7 ms                                                | 29.3 ms: 1.29x faster                                  |
| django_template | 27.2 ms                                                | 21.9 ms: 1.25x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.8 ms: 1.23x faster                                  |
| Geometric mean  | (ref)                                                  | 1.29x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.56 ms: 2.10x faster                                  |
| logging_silent          | 119 ns                                                 | 66.9 ns: 1.78x faster                                  |
| richards                | 51.4 ms                                                | 30.7 ms: 1.68x faster                                  |
| nbody                   | 94.6 ms                                                | 60.7 ms: 1.56x faster                                  |
| scimark_lu              | 110 ms                                                 | 71.2 ms: 1.54x faster                                  |
| raytrace                | 329 ms                                                 | 222 ms: 1.49x faster                                   |
| go                      | 165 ms                                                 | 111 ms: 1.48x faster                                   |
| scimark_sor             | 126 ms                                                 | 85.2 ms: 1.48x faster                                  |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.48x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 333 ms: 1.46x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.40 ms: 1.43x faster                                  |
| crypto_pyaes            | 77.9 ms                                                | 54.6 ms: 1.43x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 50.7 ms: 1.43x faster                                  |
| mako                    | 10.6 ms                                                | 7.44 ms: 1.43x faster                                  |
| chaos                   | 66.5 ms                                                | 47.4 ms: 1.40x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 145 us: 1.40x faster                                   |
| async_tree_none         | 396 ms                                                 | 288 ms: 1.37x faster                                   |
| pyflate                 | 454 ms                                                 | 332 ms: 1.37x faster                                   |
| float                   | 72.1 ms                                                | 52.7 ms: 1.37x faster                                  |
| async_tree_io           | 1.01 sec                                               | 743 ms: 1.36x faster                                   |
| pycparser               | 915 ms                                                 | 676 ms: 1.35x faster                                   |
| 2to3                    | 222 ms                                                 | 165 ms: 1.35x faster                                   |
| deepcopy_memo           | 34.4 us                                                | 25.8 us: 1.33x faster                                  |
| spectral_norm           | 95.8 ms                                                | 72.1 ms: 1.33x faster                                  |
| json_dumps              | 8.34 ms                                                | 6.28 ms: 1.33x faster                                  |
| chameleon               | 5.86 ms                                                | 4.48 ms: 1.31x faster                                  |
| tornado_http            | 90.1 ms                                                | 69.5 ms: 1.30x faster                                  |
| genshi_xml              | 37.7 ms                                                | 29.3 ms: 1.29x faster                                  |
| pprint_pformat          | 1.24 sec                                               | 967 ms: 1.28x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 475 ms: 1.28x faster                                   |
| regex_compile           | 96.2 ms                                                | 75.9 ms: 1.27x faster                                  |
| thrift                  | 577 us                                                 | 456 us: 1.27x faster                                   |
| logging_simple          | 4.61 us                                                | 3.66 us: 1.26x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.06 ms: 1.25x faster                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.19 ms: 1.25x faster                                  |
| logging_format          | 4.95 us                                                | 3.95 us: 1.25x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.23 ms: 1.25x faster                                  |
| deepcopy                | 278 us                                                 | 222 us: 1.25x faster                                   |
| django_template         | 27.2 ms                                                | 21.9 ms: 1.25x faster                                  |
| scimark_fft             | 231 ms                                                 | 187 ms: 1.23x faster                                   |
| html5lib                | 44.0 ms                                                | 35.7 ms: 1.23x faster                                  |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 36.7 ms: 1.23x faster                                  |
| genshi_text             | 18.2 ms                                                | 14.8 ms: 1.23x faster                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 548 ms: 1.21x faster                                   |
| fannkuch                | 318 ms                                                 | 262 ms: 1.21x faster                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.86 ms: 1.21x faster                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.96 us: 1.21x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 32.0 ms: 1.19x faster                                  |
| generators              | 32.5 ms                                                | 27.8 ms: 1.17x faster                                  |
| docutils                | 1.76 sec                                               | 1.51 sec: 1.17x faster                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.5 ms: 1.15x faster                                  |
| unpack_sequence         | 38.2 ns                                                | 33.3 ns: 1.15x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.13x faster                                  |
| bench_thread_pool       | 531 us                                                 | 472 us: 1.12x faster                                   |
| json                    | 3.13 ms                                                | 2.80 ms: 1.12x faster                                  |
| mdp                     | 1.66 sec                                               | 1.49 sec: 1.11x faster                                 |
| coroutines              | 20.1 ms                                                | 18.1 ms: 1.11x faster                                  |
| sqlite_synth            | 1.50 us                                                | 1.35 us: 1.11x faster                                  |
| sympy_expand            | 275 ms                                                 | 248 ms: 1.11x faster                                   |
| nqueens                 | 68.6 ms                                                | 62.1 ms: 1.10x faster                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| sympy_str               | 169 ms                                                 | 154 ms: 1.10x faster                                   |
| regex_dna               | 164 ms                                                 | 152 ms: 1.08x faster                                   |
| sympy_sum               | 93.5 ms                                                | 88.3 ms: 1.06x faster                                  |
| meteor_contest          | 77.7 ms                                                | 73.8 ms: 1.05x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 51.8 ms: 1.05x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| telco                   | 3.63 ms                                                | 3.49 ms: 1.04x faster                                  |
| xml_etree_parse         | 100 ms                                                 | 97.4 ms: 1.03x faster                                  |
| unpickle                | 10.0 us                                                | 9.77 us: 1.03x faster                                  |
| pickle                  | 7.50 us                                                | 7.41 us: 1.01x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.64 us: 1.01x faster                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                   |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.3 ms: 1.02x slower                                  |
| regex_effbot            | 2.45 ms                                                | 2.68 ms: 1.09x slower                                  |
| bench_mp_pool           | 40.8 ms                                                | 44.8 ms: 1.10x slower                                  |
| python_startup          | 9.59 ms                                                | 11.0 ms: 1.14x slower                                  |
| async_generators        | 231 ms                                                 | 266 ms: 1.15x slower                                   |
| pathlib                 | 22.2 ms                                                | 27.9 ms: 1.26x slower                                  |
| python_startup_no_site  | 7.00 ms                                                | 8.99 ms: 1.28x slower                                  |
| coverage                | 40.8 ms                                                | 56.0 ms: 1.37x slower                                  |
| Geometric mean          | (ref)                                                  | 1.20x faster                                           |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230318-3.12.0a6+-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6+-3adb23a.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
