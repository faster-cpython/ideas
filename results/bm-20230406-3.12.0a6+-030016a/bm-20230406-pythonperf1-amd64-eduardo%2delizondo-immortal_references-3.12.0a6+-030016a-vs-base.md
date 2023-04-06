
# Results vs. base

- fork: eduardo-elizondo
- ref: immortal_references
- machine: windows-amd64
- commit hash: 030016a
- commit date: 2023-04-06
- overall geometric mean: 1.20x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 202 ms                                                                      | 234 ms: 1.16x slower                                                                   |
| chameleon      | 4.50 ms                                                                     | 6.13 ms: 1.36x slower                                                                  |
| docutils       | 1.58 sec                                                                    | 1.70 sec: 1.08x slower                                                                 |
| html5lib       | 35.7 ms                                                                     | 42.8 ms: 1.20x slower                                                                  |
| tornado_http   | 87.7 ms                                                                     | 95.8 ms: 1.09x slower                                                                  |
| Geometric mean | (ref)                                                                       | 1.17x slower                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 145 ms                                                                      | 152 ms: 1.05x slower                                                                   |
| float          | 47.4 ms                                                                     | 62.4 ms: 1.32x slower                                                                  |
| nbody          | 53.3 ms                                                                     | 92.3 ms: 1.73x slower                                                                  |
| Geometric mean | (ref)                                                                       | 1.34x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_dna      | 123 ms                                                                      | 116 ms: 1.06x faster                                                                   |
| regex_effbot   | 1.55 ms                                                                     | 1.50 ms: 1.03x faster                                                                  |
| regex_compile  | 79.5 ms                                                                     | 103 ms: 1.30x slower                                                                   |
| Geometric mean | (ref)                                                                       | 1.04x slower                                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| unpickle_list        | 2.76 us                                                                     | 2.59 us: 1.06x faster                                                                  |
| unpickle             | 7.73 us                                                                     | 7.80 us: 1.01x slower                                                                  |
| pickle               | 7.09 us                                                                     | 7.23 us: 1.02x slower                                                                  |
| json_loads           | 13.5 us                                                                     | 13.9 us: 1.03x slower                                                                  |
| pickle_dict          | 18.9 us                                                                     | 19.6 us: 1.04x slower                                                                  |
| xml_etree_parse      | 89.7 ms                                                                     | 94.4 ms: 1.05x slower                                                                  |
| json_dumps           | 5.30 ms                                                                     | 5.78 ms: 1.09x slower                                                                  |
| xml_etree_iterparse  | 60.4 ms                                                                     | 67.4 ms: 1.12x slower                                                                  |
| pickle_list          | 2.75 us                                                                     | 3.10 us: 1.13x slower                                                                  |
| xml_etree_generate   | 50.7 ms                                                                     | 60.6 ms: 1.20x slower                                                                  |
| xml_etree_process    | 34.7 ms                                                                     | 44.2 ms: 1.27x slower                                                                  |
| pickle_pure_python   | 171 us                                                                      | 239 us: 1.40x slower                                                                   |
| unpickle_pure_python | 121 us                                                                      | 173 us: 1.43x slower                                                                   |
| Geometric mean       | (ref)                                                                       | 1.12x slower                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|------------------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                                     | 15.8 ms: 1.02x faster                                                                  |
| Geometric mean         | (ref)                                                                       | 1.01x faster                                                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-----------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| django_template | 20.7 ms                                                                     | 25.3 ms: 1.22x slower                                                                  |
| mako            | 6.17 ms                                                                     | 7.79 ms: 1.26x slower                                                                  |
| genshi_xml      | 29.6 ms                                                                     | 38.2 ms: 1.29x slower                                                                  |
| genshi_text     | 13.2 ms                                                                     | 17.5 ms: 1.32x slower                                                                  |
| Geometric mean  | (ref)                                                                       | 1.27x slower                                                                           |

All benchmarks:
===============

| Benchmark               | bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-------------------------|:---------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| unpickle_list           | 2.76 us                                                                     | 2.59 us: 1.06x faster                                                                  |
| regex_dna               | 123 ms                                                                      | 116 ms: 1.06x faster                                                                   |
| regex_effbot            | 1.55 ms                                                                     | 1.50 ms: 1.03x faster                                                                  |
| python_startup_no_site  | 16.2 ms                                                                     | 15.8 ms: 1.02x faster                                                                  |
| unpickle                | 7.73 us                                                                     | 7.80 us: 1.01x slower                                                                  |
| pathlib                 | 83.9 ms                                                                     | 85.3 ms: 1.02x slower                                                                  |
| pickle                  | 7.09 us                                                                     | 7.23 us: 1.02x slower                                                                  |
| create_gc_cycles        | 696 us                                                                      | 711 us: 1.02x slower                                                                   |
| json_loads              | 13.5 us                                                                     | 13.9 us: 1.03x slower                                                                  |
| coverage                | 52.2 ms                                                                     | 53.8 ms: 1.03x slower                                                                  |
| gc_traversal            | 1.47 ms                                                                     | 1.52 ms: 1.03x slower                                                                  |
| bench_mp_pool           | 66.4 ms                                                                     | 68.7 ms: 1.03x slower                                                                  |
| pickle_dict             | 18.9 us                                                                     | 19.6 us: 1.04x slower                                                                  |
| json                    | 2.65 ms                                                                     | 2.78 ms: 1.05x slower                                                                  |
| pidigits                | 145 ms                                                                      | 152 ms: 1.05x slower                                                                   |
| sqlite_synth            | 1.78 us                                                                     | 1.87 us: 1.05x slower                                                                  |
| xml_etree_parse         | 89.7 ms                                                                     | 94.4 ms: 1.05x slower                                                                  |
| async_tree_cpu_io_mixed | 476 ms                                                                      | 502 ms: 1.05x slower                                                                   |
| async_tree_io           | 757 ms                                                                      | 802 ms: 1.06x slower                                                                   |
| mdp                     | 1.40 sec                                                                    | 1.50 sec: 1.07x slower                                                                 |
| bench_thread_pool       | 836 us                                                                      | 897 us: 1.07x slower                                                                   |
| thrift                  | 460 us                                                                      | 494 us: 1.07x slower                                                                   |
| docutils                | 1.58 sec                                                                    | 1.70 sec: 1.08x slower                                                                 |
| sympy_sum               | 97.7 ms                                                                     | 106 ms: 1.08x slower                                                                   |
| dulwich_log             | 41.6 ms                                                                     | 45.0 ms: 1.08x slower                                                                  |
| sympy_expand            | 278 ms                                                                      | 302 ms: 1.09x slower                                                                   |
| json_dumps              | 5.30 ms                                                                     | 5.78 ms: 1.09x slower                                                                  |
| tornado_http            | 87.7 ms                                                                     | 95.8 ms: 1.09x slower                                                                  |
| sympy_str               | 175 ms                                                                      | 192 ms: 1.09x slower                                                                   |
| telco                   | 3.92 ms                                                                     | 4.31 ms: 1.10x slower                                                                  |
| generators              | 20.2 ms                                                                     | 22.5 ms: 1.11x slower                                                                  |
| xml_etree_iterparse     | 60.4 ms                                                                     | 67.4 ms: 1.12x slower                                                                  |
| async_tree_none         | 306 ms                                                                      | 342 ms: 1.12x slower                                                                   |
| async_tree_memoization  | 362 ms                                                                      | 407 ms: 1.13x slower                                                                   |
| pickle_list             | 2.75 us                                                                     | 3.10 us: 1.13x slower                                                                  |
| mypy2                   | 217 ms                                                                      | 246 ms: 1.14x slower                                                                   |
| 2to3                    | 202 ms                                                                      | 234 ms: 1.16x slower                                                                   |
| async_generators        | 206 ms                                                                      | 239 ms: 1.16x slower                                                                   |
| sympy_integrate         | 12.8 ms                                                                     | 14.9 ms: 1.17x slower                                                                  |
| pycparser               | 665 ms                                                                      | 776 ms: 1.17x slower                                                                   |
| dask                    | 355 ms                                                                      | 417 ms: 1.18x slower                                                                   |
| nqueens                 | 57.4 ms                                                                     | 67.5 ms: 1.18x slower                                                                  |
| coroutines              | 13.8 ms                                                                     | 16.4 ms: 1.18x slower                                                                  |
| sqlglot_normalize       | 165 ms                                                                      | 196 ms: 1.18x slower                                                                   |
| sqlglot_optimize        | 30.7 ms                                                                     | 36.6 ms: 1.19x slower                                                                  |
| xml_etree_generate      | 50.7 ms                                                                     | 60.6 ms: 1.20x slower                                                                  |
| html5lib                | 35.7 ms                                                                     | 42.8 ms: 1.20x slower                                                                  |
| logging_format          | 6.29 us                                                                     | 7.54 us: 1.20x slower                                                                  |
| django_template         | 20.7 ms                                                                     | 25.3 ms: 1.22x slower                                                                  |
| logging_simple          | 6.02 us                                                                     | 7.36 us: 1.22x slower                                                                  |
| meteor_contest          | 69.1 ms                                                                     | 85.3 ms: 1.24x slower                                                                  |
| mako                    | 6.17 ms                                                                     | 7.79 ms: 1.26x slower                                                                  |
| comprehensions          | 14.6 us                                                                     | 18.5 us: 1.27x slower                                                                  |
| xml_etree_process       | 34.7 ms                                                                     | 44.2 ms: 1.27x slower                                                                  |
| pyflate                 | 278 ms                                                                      | 357 ms: 1.29x slower                                                                   |
| genshi_xml              | 29.6 ms                                                                     | 38.2 ms: 1.29x slower                                                                  |
| regex_compile           | 79.5 ms                                                                     | 103 ms: 1.30x slower                                                                   |
| pprint_safe_repr        | 453 ms                                                                      | 588 ms: 1.30x slower                                                                   |
| crypto_pyaes            | 43.4 ms                                                                     | 56.3 ms: 1.30x slower                                                                  |
| deepcopy_reduce         | 1.80 us                                                                     | 2.35 us: 1.31x slower                                                                  |
| float                   | 47.4 ms                                                                     | 62.4 ms: 1.32x slower                                                                  |
| raytrace                | 169 ms                                                                      | 223 ms: 1.32x slower                                                                   |
| genshi_text             | 13.2 ms                                                                     | 17.5 ms: 1.32x slower                                                                  |
| pprint_pformat          | 906 ms                                                                      | 1.21 sec: 1.34x slower                                                                 |
| go                      | 82.4 ms                                                                     | 110 ms: 1.34x slower                                                                   |
| chaos                   | 40.9 ms                                                                     | 54.8 ms: 1.34x slower                                                                  |
| deepcopy                | 205 us                                                                      | 278 us: 1.35x slower                                                                   |
| sqlglot_parse           | 832 us                                                                      | 1.13 ms: 1.36x slower                                                                  |
| chameleon               | 4.50 ms                                                                     | 6.13 ms: 1.36x slower                                                                  |
| sqlglot_transpile       | 1.02 ms                                                                     | 1.39 ms: 1.36x slower                                                                  |
| logging_silent          | 53.8 ns                                                                     | 73.9 ns: 1.38x slower                                                                  |
| deltablue               | 1.95 ms                                                                     | 2.70 ms: 1.38x slower                                                                  |
| fannkuch                | 225 ms                                                                      | 313 ms: 1.39x slower                                                                   |
| pickle_pure_python      | 171 us                                                                      | 239 us: 1.40x slower                                                                   |
| hexiom                  | 3.78 ms                                                                     | 5.32 ms: 1.41x slower                                                                  |
| richards                | 24.0 ms                                                                     | 33.9 ms: 1.42x slower                                                                  |
| unpickle_pure_python    | 121 us                                                                      | 173 us: 1.43x slower                                                                   |
| scimark_fft             | 154 ms                                                                      | 220 ms: 1.43x slower                                                                   |
| scimark_sparse_mat_mult | 2.09 ms                                                                     | 3.02 ms: 1.45x slower                                                                  |
| scimark_lu              | 50.6 ms                                                                     | 73.2 ms: 1.45x slower                                                                  |
| spectral_norm           | 55.4 ms                                                                     | 81.1 ms: 1.46x slower                                                                  |
| scimark_monte_carlo     | 38.0 ms                                                                     | 56.0 ms: 1.48x slower                                                                  |
| deepcopy_memo           | 20.1 us                                                                     | 29.8 us: 1.49x slower                                                                  |
| scimark_sor             | 65.1 ms                                                                     | 104 ms: 1.60x slower                                                                   |
| nbody                   | 53.3 ms                                                                     | 92.3 ms: 1.73x slower                                                                  |
| unpack_sequence         | 27.4 ns                                                                     | 61.7 ns: 2.25x slower                                                                  |
| Geometric mean          | (ref)                                                                       | 1.20x slower                                                                           |

Benchmark hidden because not significant (3): python_startup, regex_v8, asyncio_tcp
