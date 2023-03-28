
# Results vs. 3.10.4

- fork: python
- ref: 3c67ec394faac79d2608
- machine: darwin-arm64
- commit hash: 3c67ec3
- commit date: 2023-02-07
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 162 ms: 1.37x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.61 ms: 1.27x faster                                                 |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                |
| html5lib       | 44.0 ms                                                | 34.8 ms: 1.26x faster                                                 |
| tornado_http   | 90.1 ms                                                | 70.0 ms: 1.29x faster                                                 |
| Geometric mean | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.1 ms: 1.48x faster                                                 |
| float          | 72.1 ms                                                | 52.1 ms: 1.38x faster                                                 |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 72.3 ms: 1.33x faster                                                 |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                 |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.62 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.12x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 192 us: 1.47x faster                                                  |
| json_dumps           | 8.34 ms                                                | 6.10 ms: 1.37x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.6 ms: 1.30x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 157 us: 1.30x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.3 ms: 1.13x faster                                                 |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 96.4 ms: 1.04x faster                                                 |
| pickle_list          | 2.83 us                                                | 2.76 us: 1.02x faster                                                 |
| unpickle             | 10.0 us                                                | 9.82 us: 1.02x faster                                                 |
| pickle               | 7.50 us                                                | 7.47 us: 1.00x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.68 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 70.1 ms: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 10.3 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.19 ms: 1.47x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 28.2 ms: 1.34x faster                                                 |
| django_template | 27.2 ms                                                | 21.1 ms: 1.29x faster                                                 |
| genshi_text     | 18.2 ms                                                | 14.2 ms: 1.28x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.34x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.57 ms: 2.09x faster                                                 |
| logging_silent          | 119 ns                                                 | 65.8 ns: 1.81x faster                                                 |
| richards                | 51.4 ms                                                | 29.8 ms: 1.73x faster                                                 |
| scimark_lu              | 110 ms                                                 | 70.9 ms: 1.55x faster                                                 |
| go                      | 165 ms                                                 | 110 ms: 1.51x faster                                                  |
| raytrace                | 329 ms                                                 | 221 ms: 1.49x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 327 ms: 1.48x faster                                                  |
| scimark_sor             | 126 ms                                                 | 85.3 ms: 1.48x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 52.8 ms: 1.48x faster                                                 |
| nbody                   | 94.6 ms                                                | 64.1 ms: 1.48x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.47x faster                                                  |
| mako                    | 10.6 ms                                                | 7.19 ms: 1.47x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.32 ms: 1.46x faster                                                 |
| chaos                   | 66.5 ms                                                | 45.7 ms: 1.45x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 50.0 ms: 1.45x faster                                                 |
| async_tree_none         | 396 ms                                                 | 284 ms: 1.39x faster                                                  |
| float                   | 72.1 ms                                                | 52.1 ms: 1.38x faster                                                 |
| pycparser               | 915 ms                                                 | 664 ms: 1.38x faster                                                  |
| pyflate                 | 454 ms                                                 | 331 ms: 1.37x faster                                                  |
| json_dumps              | 8.34 ms                                                | 6.10 ms: 1.37x faster                                                 |
| 2to3                    | 222 ms                                                 | 162 ms: 1.37x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 742 ms: 1.36x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 28.2 ms: 1.34x faster                                                 |
| regex_compile           | 96.2 ms                                                | 72.3 ms: 1.33x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 26.0 us: 1.32x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 72.5 ms: 1.32x faster                                                 |
| thrift                  | 577 us                                                 | 442 us: 1.31x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 34.6 ms: 1.30x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.02 ms: 1.30x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 157 us: 1.30x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 469 ms: 1.30x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.19 ms: 1.30x faster                                                 |
| django_template         | 27.2 ms                                                | 21.1 ms: 1.29x faster                                                 |
| tornado_http            | 90.1 ms                                                | 70.0 ms: 1.29x faster                                                 |
| pprint_pformat          | 1.24 sec                                               | 963 ms: 1.29x faster                                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.01 ms: 1.29x faster                                                 |
| genshi_text             | 18.2 ms                                                | 14.2 ms: 1.28x faster                                                 |
| chameleon               | 5.86 ms                                                | 4.61 ms: 1.27x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.64 us: 1.27x faster                                                 |
| logging_format          | 4.95 us                                                | 3.91 us: 1.27x faster                                                 |
| html5lib                | 44.0 ms                                                | 34.8 ms: 1.26x faster                                                 |
| deepcopy                | 278 us                                                 | 220 us: 1.26x faster                                                  |
| fannkuch                | 318 ms                                                 | 256 ms: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.80 ms: 1.24x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 29.4 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed | 665 ms                                                 | 538 ms: 1.24x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.93 us: 1.22x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                                 |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                |
| scimark_fft             | 231 ms                                                 | 192 ms: 1.20x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.2 ms: 1.18x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 62.9 ms: 1.18x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                                 |
| sympy_str               | 169 ms                                                 | 146 ms: 1.16x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.16x faster                                                  |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                                  |
| bench_thread_pool       | 531 us                                                 | 463 us: 1.15x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 82.1 ms: 1.14x faster                                                 |
| nqueens                 | 68.6 ms                                                | 60.6 ms: 1.13x faster                                                 |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                 |
| sympy_expand            | 275 ms                                                 | 244 ms: 1.13x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.3 ms: 1.13x faster                                                 |
| json                    | 3.13 ms                                                | 2.79 ms: 1.12x faster                                                 |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.37 us: 1.09x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.09x faster                                                |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                                 |
| telco                   | 3.63 ms                                                | 3.43 ms: 1.06x faster                                                 |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| xml_etree_parse         | 100 ms                                                 | 96.4 ms: 1.04x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 75.6 ms: 1.03x faster                                                 |
| pickle_list             | 2.83 us                                                | 2.76 us: 1.02x faster                                                 |
| unpickle                | 10.0 us                                                | 9.82 us: 1.02x faster                                                 |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| pickle                  | 7.50 us                                                | 7.47 us: 1.00x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.68 us: 1.01x slower                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 70.1 ms: 1.02x slower                                                 |
| generators              | 32.5 ms                                                | 34.3 ms: 1.06x slower                                                 |
| regex_effbot            | 2.45 ms                                                | 2.62 ms: 1.07x slower                                                 |
| bench_mp_pool           | 40.8 ms                                                | 44.6 ms: 1.09x slower                                                 |
| pathlib                 | 22.2 ms                                                | 27.5 ms: 1.24x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                 |
| coverage                | 40.8 ms                                                | 56.8 ms: 1.39x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 10.3 ms: 1.47x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230207-3.12.0a5-3c67ec3/bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
