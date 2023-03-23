
# Results vs. 3.10.4

- fork: python
- ref: ef7c2bfcf1fd618438f9
- machine: darwin-arm64
- commit hash: ef7c2bf
- commit date: 2023-02-05
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 163 ms: 1.37x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.56 ms: 1.28x faster                                                  |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| html5lib       | 44.0 ms                                                | 34.7 ms: 1.27x faster                                                  |
| tornado_http   | 90.1 ms                                                | 69.3 ms: 1.30x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.0 ms: 1.48x faster                                                  |
| float          | 72.1 ms                                                | 52.0 ms: 1.38x faster                                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 72.4 ms: 1.33x faster                                                  |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 191 us: 1.48x faster                                                   |
| json_dumps           | 8.34 ms                                                | 6.11 ms: 1.36x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 156 us: 1.30x faster                                                   |
| xml_etree_process    | 45.1 ms                                                | 34.7 ms: 1.30x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.0 ms: 1.14x faster                                                  |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.4 ms: 1.04x faster                                                  |
| pickle_list          | 2.83 us                                                | 2.74 us: 1.03x faster                                                  |
| unpickle             | 10.0 us                                                | 9.87 us: 1.02x faster                                                  |
| pickle               | 7.50 us                                                | 7.46 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.1 ms: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (2): pickle_dict, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.5 ms: 1.30x slower                                                  |
| python_startup_no_site | 7.00 ms                                                | 10.4 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.39x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 10.6 ms                                                | 7.18 ms: 1.48x faster                                                  |
| genshi_xml      | 37.7 ms                                                | 28.3 ms: 1.33x faster                                                  |
| django_template | 27.2 ms                                                | 21.2 ms: 1.29x faster                                                  |
| genshi_text     | 18.2 ms                                                | 14.2 ms: 1.28x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.34x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.58 ms: 2.08x faster                                                  |
| logging_silent          | 119 ns                                                 | 65.8 ns: 1.81x faster                                                  |
| richards                | 51.4 ms                                                | 29.8 ms: 1.73x faster                                                  |
| scimark_lu              | 110 ms                                                 | 70.8 ms: 1.55x faster                                                  |
| go                      | 165 ms                                                 | 110 ms: 1.50x faster                                                   |
| raytrace                | 329 ms                                                 | 222 ms: 1.49x faster                                                   |
| pickle_pure_python      | 284 us                                                 | 191 us: 1.48x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 327 ms: 1.48x faster                                                   |
| nbody                   | 94.6 ms                                                | 64.0 ms: 1.48x faster                                                  |
| mako                    | 10.6 ms                                                | 7.18 ms: 1.48x faster                                                  |
| scimark_sor             | 126 ms                                                 | 85.5 ms: 1.47x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.1 ms: 1.47x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.32 ms: 1.46x faster                                                  |
| chaos                   | 66.5 ms                                                | 45.7 ms: 1.46x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 49.8 ms: 1.45x faster                                                  |
| async_tree_none         | 396 ms                                                 | 285 ms: 1.39x faster                                                   |
| float                   | 72.1 ms                                                | 52.0 ms: 1.38x faster                                                  |
| pycparser               | 915 ms                                                 | 666 ms: 1.37x faster                                                   |
| pyflate                 | 454 ms                                                 | 331 ms: 1.37x faster                                                   |
| 2to3                    | 222 ms                                                 | 163 ms: 1.37x faster                                                   |
| json_dumps              | 8.34 ms                                                | 6.11 ms: 1.36x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 743 ms: 1.36x faster                                                   |
| genshi_xml              | 37.7 ms                                                | 28.3 ms: 1.33x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 25.9 us: 1.33x faster                                                  |
| regex_compile           | 96.2 ms                                                | 72.4 ms: 1.33x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 72.7 ms: 1.32x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 156 us: 1.30x faster                                                   |
| thrift                  | 577 us                                                 | 443 us: 1.30x faster                                                   |
| sqlglot_parse           | 1.33 ms                                                | 1.02 ms: 1.30x faster                                                  |
| tornado_http            | 90.1 ms                                                | 69.3 ms: 1.30x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 34.7 ms: 1.30x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.19 ms: 1.30x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 961 ms: 1.29x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 472 ms: 1.29x faster                                                   |
| django_template         | 27.2 ms                                                | 21.2 ms: 1.29x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.56 ms: 1.28x faster                                                  |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.03 ms: 1.28x faster                                                  |
| genshi_text             | 18.2 ms                                                | 14.2 ms: 1.28x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.62 us: 1.27x faster                                                  |
| html5lib                | 44.0 ms                                                | 34.7 ms: 1.27x faster                                                  |
| logging_format          | 4.95 us                                                | 3.90 us: 1.27x faster                                                  |
| deepcopy                | 278 us                                                 | 219 us: 1.27x faster                                                   |
| fannkuch                | 318 ms                                                 | 256 ms: 1.24x faster                                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.80 ms: 1.24x faster                                                  |
| dulwich_log             | 36.4 ms                                                | 29.5 ms: 1.24x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 1.91 us: 1.24x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 543 ms: 1.23x faster                                                   |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                                  |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| scimark_fft             | 231 ms                                                 | 192 ms: 1.20x faster                                                   |
| sympy_integrate         | 13.3 ms                                                | 11.2 ms: 1.19x faster                                                  |
| sqlalchemy_declarative  | 74.4 ms                                                | 63.0 ms: 1.18x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                                  |
| sympy_str               | 169 ms                                                 | 146 ms: 1.16x faster                                                   |
| sqlglot_normalize       | 198 ms                                                 | 171 ms: 1.16x faster                                                   |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                                   |
| bench_thread_pool       | 531 us                                                 | 463 us: 1.15x faster                                                   |
| sympy_sum               | 93.5 ms                                                | 82.0 ms: 1.14x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.0 ms: 1.14x faster                                                  |
| sympy_expand            | 275 ms                                                 | 243 ms: 1.13x faster                                                   |
| nqueens                 | 68.6 ms                                                | 60.6 ms: 1.13x faster                                                  |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                  |
| json                    | 3.13 ms                                                | 2.78 ms: 1.12x faster                                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| sqlite_synth            | 1.50 us                                                | 1.36 us: 1.10x faster                                                  |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.09x faster                                                 |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                                  |
| telco                   | 3.63 ms                                                | 3.43 ms: 1.06x faster                                                  |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.4 ms: 1.04x faster                                                  |
| pickle_list             | 2.83 us                                                | 2.74 us: 1.03x faster                                                  |
| meteor_contest          | 77.7 ms                                                | 76.2 ms: 1.02x faster                                                  |
| unpickle                | 10.0 us                                                | 9.87 us: 1.02x faster                                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| pickle                  | 7.50 us                                                | 7.46 us: 1.01x faster                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.1 ms: 1.02x slower                                                  |
| generators              | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.63 ms: 1.07x slower                                                  |
| bench_mp_pool           | 40.8 ms                                                | 45.0 ms: 1.10x slower                                                  |
| pathlib                 | 22.2 ms                                                | 27.9 ms: 1.26x slower                                                  |
| python_startup          | 9.59 ms                                                | 12.5 ms: 1.30x slower                                                  |
| coverage                | 40.8 ms                                                | 57.3 ms: 1.40x slower                                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.4 ms: 1.49x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                           |

Benchmark hidden because not significant (2): pickle_dict, unpickle_list
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230205-3.12.0a4+-ef7c2bf/bm-20230205-darwin-arm64-python-ef7c2bfcf1fd618438f9-3.12.0a4+-ef7c2bf.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
