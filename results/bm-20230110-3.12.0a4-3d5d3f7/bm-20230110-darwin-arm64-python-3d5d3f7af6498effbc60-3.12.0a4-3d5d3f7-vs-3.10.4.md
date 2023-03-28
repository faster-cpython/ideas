
# Results vs. 3.10.4

- fork: python
- ref: 3d5d3f7af6498effbc60
- machine: darwin-arm64
- commit hash: 3d5d3f7
- commit date: 2023-01-10
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 163 ms: 1.37x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.53 ms: 1.29x faster                                                 |
| docutils       | 1.76 sec                                               | 1.45 sec: 1.21x faster                                                |
| html5lib       | 44.0 ms                                                | 35.0 ms: 1.26x faster                                                 |
| Geometric mean | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 63.9 ms: 1.48x faster                                                 |
| float          | 72.1 ms                                                | 52.0 ms: 1.39x faster                                                 |
| pidigits       | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 74.5 ms: 1.29x faster                                                 |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                 |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.61 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 192 us: 1.47x faster                                                  |
| unpickle_pure_python | 204 us                                                 | 143 us: 1.43x faster                                                  |
| json_dumps           | 8.34 ms                                                | 6.05 ms: 1.38x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 48.6 ms: 1.12x faster                                                 |
| json_loads           | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| xml_etree_parse      | 100 ms                                                 | 96.5 ms: 1.04x faster                                                 |
| unpickle             | 10.0 us                                                | 9.76 us: 1.03x faster                                                 |
| pickle               | 7.50 us                                                | 7.44 us: 1.01x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 69.4 ms: 1.01x slower                                                 |
| unpickle_list        | 2.66 us                                                | 2.70 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (2): pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.3 ms: 1.28x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 10.2 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 37.7 ms                                                | 28.4 ms: 1.33x faster                                                 |
| mako            | 10.6 ms                                                | 8.12 ms: 1.31x faster                                                 |
| django_template | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.2 ms: 1.19x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.27x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.64 ms: 2.03x faster                                                 |
| logging_silent          | 119 ns                                                 | 66.4 ns: 1.80x faster                                                 |
| richards                | 51.4 ms                                                | 30.6 ms: 1.68x faster                                                 |
| scimark_sor             | 126 ms                                                 | 82.8 ms: 1.52x faster                                                 |
| raytrace                | 329 ms                                                 | 217 ms: 1.52x faster                                                  |
| go                      | 165 ms                                                 | 109 ms: 1.52x faster                                                  |
| scimark_lu              | 110 ms                                                 | 72.7 ms: 1.51x faster                                                 |
| crypto_pyaes            | 77.9 ms                                                | 52.6 ms: 1.48x faster                                                 |
| nbody                   | 94.6 ms                                                | 63.9 ms: 1.48x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.47x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 332 ms: 1.46x faster                                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 49.6 ms: 1.46x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 143 us: 1.43x faster                                                  |
| pyflate                 | 454 ms                                                 | 318 ms: 1.43x faster                                                  |
| float                   | 72.1 ms                                                | 52.0 ms: 1.39x faster                                                 |
| json_dumps              | 8.34 ms                                                | 6.05 ms: 1.38x faster                                                 |
| async_tree_none         | 396 ms                                                 | 288 ms: 1.37x faster                                                  |
| 2to3                    | 222 ms                                                 | 163 ms: 1.37x faster                                                  |
| pycparser               | 915 ms                                                 | 676 ms: 1.35x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 748 ms: 1.35x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.44 us: 1.34x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 28.4 ms: 1.33x faster                                                 |
| logging_format          | 4.95 us                                                | 3.74 us: 1.32x faster                                                 |
| pprint_pformat          | 1.24 sec                                               | 939 ms: 1.32x faster                                                  |
| thrift                  | 577 us                                                 | 438 us: 1.32x faster                                                  |
| chaos                   | 66.5 ms                                                | 50.5 ms: 1.32x faster                                                 |
| pprint_safe_repr        | 608 ms                                                 | 462 ms: 1.32x faster                                                  |
| deepcopy_memo           | 34.4 us                                                | 26.2 us: 1.31x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 73.4 ms: 1.31x faster                                                 |
| mako                    | 10.6 ms                                                | 8.12 ms: 1.31x faster                                                 |
| chameleon               | 5.86 ms                                                | 4.53 ms: 1.29x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| regex_compile           | 96.2 ms                                                | 74.5 ms: 1.29x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.20 ms: 1.29x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.04 ms: 1.28x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.94 ms: 1.28x faster                                                 |
| deepcopy                | 278 us                                                 | 221 us: 1.26x faster                                                  |
| django_template         | 27.2 ms                                                | 21.6 ms: 1.26x faster                                                 |
| html5lib                | 44.0 ms                                                | 35.0 ms: 1.26x faster                                                 |
| fannkuch                | 318 ms                                                 | 254 ms: 1.25x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.81 ms: 1.23x faster                                                 |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                                 |
| deepcopy_reduce         | 2.36 us                                                | 1.92 us: 1.23x faster                                                 |
| async_tree_cpu_io_mixed | 665 ms                                                 | 546 ms: 1.22x faster                                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.3 ms: 1.22x faster                                                 |
| docutils                | 1.76 sec                                               | 1.45 sec: 1.21x faster                                                |
| genshi_text             | 18.2 ms                                                | 15.2 ms: 1.19x faster                                                 |
| scimark_fft             | 231 ms                                                 | 195 ms: 1.19x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                                 |
| sympy_integrate         | 13.3 ms                                                | 11.4 ms: 1.16x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 172 ms: 1.15x faster                                                  |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                                  |
| bench_thread_pool       | 531 us                                                 | 462 us: 1.15x faster                                                  |
| sympy_expand            | 275 ms                                                 | 242 ms: 1.14x faster                                                  |
| nqueens                 | 68.6 ms                                                | 60.5 ms: 1.13x faster                                                 |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                 |
| json                    | 3.13 ms                                                | 2.78 ms: 1.12x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 48.6 ms: 1.12x faster                                                 |
| sympy_str               | 169 ms                                                 | 151 ms: 1.12x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.35 us: 1.11x faster                                                 |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                  |
| sympy_sum               | 93.5 ms                                                | 85.9 ms: 1.09x faster                                                 |
| coroutines              | 20.1 ms                                                | 18.7 ms: 1.08x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.54 sec: 1.08x faster                                                |
| telco                   | 3.63 ms                                                | 3.39 ms: 1.07x faster                                                 |
| json_loads              | 17.0 us                                                | 16.2 us: 1.05x faster                                                 |
| xml_etree_parse         | 100 ms                                                 | 96.5 ms: 1.04x faster                                                 |
| meteor_contest          | 77.7 ms                                                | 75.1 ms: 1.04x faster                                                 |
| unpickle                | 10.0 us                                                | 9.76 us: 1.03x faster                                                 |
| pidigits                | 284 ms                                                 | 281 ms: 1.01x faster                                                  |
| pickle                  | 7.50 us                                                | 7.44 us: 1.01x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 69.4 ms: 1.01x slower                                                 |
| unpickle_list           | 2.66 us                                                | 2.70 us: 1.02x slower                                                 |
| generators              | 32.5 ms                                                | 33.7 ms: 1.04x slower                                                 |
| regex_effbot            | 2.45 ms                                                | 2.61 ms: 1.06x slower                                                 |
| bench_mp_pool           | 40.8 ms                                                | 44.0 ms: 1.08x slower                                                 |
| pathlib                 | 22.2 ms                                                | 27.8 ms: 1.25x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.3 ms: 1.28x slower                                                 |
| coverage                | 40.8 ms                                                | 57.2 ms: 1.40x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 10.2 ms: 1.46x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (2): pickle_dict, pickle_list
Ignored benchmarks (8) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (6) of public/results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
