
# Results vs. 3.10.4

- fork: python
- ref: 7b14c2ef194b6eed7967
- machine: darwin-arm64
- commit hash: 7b14c2e
- commit date: 2023-01-16
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 163 ms: 1.37x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.57 ms: 1.28x faster                                                  |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| html5lib       | 44.0 ms                                                | 34.9 ms: 1.26x faster                                                  |
| tornado_http   | 90.1 ms                                                | 70.5 ms: 1.28x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 64.1 ms: 1.47x faster                                                  |
| float          | 72.1 ms                                                | 51.7 ms: 1.39x faster                                                  |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 74.6 ms: 1.29x faster                                                  |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.62 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 193 us: 1.47x faster                                                   |
| unpickle_pure_python | 204 us                                                 | 144 us: 1.42x faster                                                   |
| json_dumps           | 8.34 ms                                                | 6.15 ms: 1.36x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 35.0 ms: 1.29x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.2 ms: 1.13x faster                                                  |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.9 ms: 1.03x faster                                                  |
| unpickle             | 10.0 us                                                | 9.74 us: 1.03x faster                                                  |
| pickle_list          | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 70.1 ms: 1.01x slower                                                  |
| unpickle_list        | 2.66 us                                                | 2.73 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                  |
| python_startup_no_site | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.39x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 37.7 ms                                                | 28.2 ms: 1.34x faster                                                  |
| mako            | 10.6 ms                                                | 8.14 ms: 1.30x faster                                                  |
| django_template | 27.2 ms                                                | 21.7 ms: 1.25x faster                                                  |
| genshi_text     | 18.2 ms                                                | 15.2 ms: 1.19x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.27x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.63 ms: 2.04x faster                                                  |
| logging_silent          | 119 ns                                                 | 66.1 ns: 1.80x faster                                                  |
| richards                | 51.4 ms                                                | 30.8 ms: 1.67x faster                                                  |
| scimark_sor             | 126 ms                                                 | 78.5 ms: 1.61x faster                                                  |
| go                      | 165 ms                                                 | 108 ms: 1.52x faster                                                   |
| scimark_lu              | 110 ms                                                 | 72.6 ms: 1.51x faster                                                  |
| raytrace                | 329 ms                                                 | 219 ms: 1.51x faster                                                   |
| nbody                   | 94.6 ms                                                | 64.1 ms: 1.47x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 52.9 ms: 1.47x faster                                                  |
| pickle_pure_python      | 284 us                                                 | 193 us: 1.47x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 332 ms: 1.46x faster                                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 49.8 ms: 1.45x faster                                                  |
| pyflate                 | 454 ms                                                 | 316 ms: 1.44x faster                                                   |
| unpickle_pure_python    | 204 us                                                 | 144 us: 1.42x faster                                                   |
| float                   | 72.1 ms                                                | 51.7 ms: 1.39x faster                                                  |
| async_tree_none         | 396 ms                                                 | 289 ms: 1.37x faster                                                   |
| 2to3                    | 222 ms                                                 | 163 ms: 1.37x faster                                                   |
| pycparser               | 915 ms                                                 | 673 ms: 1.36x faster                                                   |
| json_dumps              | 8.34 ms                                                | 6.15 ms: 1.36x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 750 ms: 1.35x faster                                                   |
| genshi_xml              | 37.7 ms                                                | 28.2 ms: 1.34x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 26.0 us: 1.32x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.79 ms: 1.32x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.49 us: 1.32x faster                                                  |
| thrift                  | 577 us                                                 | 440 us: 1.31x faster                                                   |
| chaos                   | 66.5 ms                                                | 50.7 ms: 1.31x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 945 ms: 1.31x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 465 ms: 1.31x faster                                                   |
| mako                    | 10.6 ms                                                | 8.14 ms: 1.30x faster                                                  |
| logging_format          | 4.95 us                                                | 3.80 us: 1.30x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 73.7 ms: 1.30x faster                                                  |
| regex_compile           | 96.2 ms                                                | 74.6 ms: 1.29x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 35.0 ms: 1.29x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.20 ms: 1.28x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.57 ms: 1.28x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.04 ms: 1.28x faster                                                  |
| tornado_http            | 90.1 ms                                                | 70.5 ms: 1.28x faster                                                  |
| html5lib                | 44.0 ms                                                | 34.9 ms: 1.26x faster                                                  |
| django_template         | 27.2 ms                                                | 21.7 ms: 1.25x faster                                                  |
| fannkuch                | 318 ms                                                 | 254 ms: 1.25x faster                                                   |
| deepcopy                | 278 us                                                 | 223 us: 1.25x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.91 us: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.80 ms: 1.24x faster                                                  |
| dulwich_log             | 36.4 ms                                                | 29.7 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 543 ms: 1.23x faster                                                   |
| sqlglot_optimize        | 38.1 ms                                                | 31.4 ms: 1.21x faster                                                  |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.21x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.2 ms: 1.19x faster                                                  |
| scimark_fft             | 231 ms                                                 | 195 ms: 1.18x faster                                                   |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.5 ms: 1.16x faster                                                  |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.15x faster                                                   |
| bench_thread_pool       | 531 us                                                 | 464 us: 1.14x faster                                                   |
| sympy_expand            | 275 ms                                                 | 241 ms: 1.14x faster                                                   |
| async_generators        | 231 ms                                                 | 202 ms: 1.14x faster                                                   |
| xml_etree_generate      | 54.5 ms                                                | 48.2 ms: 1.13x faster                                                  |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                  |
| json                    | 3.13 ms                                                | 2.78 ms: 1.13x faster                                                  |
| sympy_str               | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| sqlite_synth            | 1.50 us                                                | 1.34 us: 1.11x faster                                                  |
| nqueens                 | 68.6 ms                                                | 61.7 ms: 1.11x faster                                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| mdp                     | 1.66 sec                                               | 1.51 sec: 1.10x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 86.6 ms: 1.08x faster                                                  |
| coroutines              | 20.1 ms                                                | 18.7 ms: 1.07x faster                                                  |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                  |
| telco                   | 3.63 ms                                                | 3.51 ms: 1.04x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.9 ms: 1.03x faster                                                  |
| unpickle                | 10.0 us                                                | 9.74 us: 1.03x faster                                                  |
| meteor_contest          | 77.7 ms                                                | 75.6 ms: 1.03x faster                                                  |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                   |
| pickle_list             | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 70.1 ms: 1.01x slower                                                  |
| unpickle_list           | 2.66 us                                                | 2.73 us: 1.02x slower                                                  |
| generators              | 32.5 ms                                                | 33.9 ms: 1.04x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.62 ms: 1.07x slower                                                  |
| bench_mp_pool           | 40.8 ms                                                | 44.3 ms: 1.09x slower                                                  |
| pathlib                 | 22.2 ms                                                | 27.5 ms: 1.24x slower                                                  |
| python_startup          | 9.59 ms                                                | 12.4 ms: 1.29x slower                                                  |
| coverage                | 40.8 ms                                                | 55.4 ms: 1.36x slower                                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.4 ms: 1.48x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                           |

Benchmark hidden because not significant (2): pickle, pickle_dict
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of public/results/bm-20230116-3.12.0a4+-7b14c2e/bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4+-7b14c2e.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
