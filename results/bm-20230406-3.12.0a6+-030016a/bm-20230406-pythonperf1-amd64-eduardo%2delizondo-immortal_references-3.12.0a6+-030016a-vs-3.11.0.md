
# Results vs. 3.11.0

- fork: eduardo-elizondo
- ref: immortal_references
- machine: windows-amd64
- commit hash: 030016a
- commit date: 2023-04-06
- overall geometric mean: 1.09x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 234 ms: 1.15x slower                                                                   |
| chameleon      | 5.15 ms                                                                  | 6.13 ms: 1.19x slower                                                                  |
| docutils       | 1.59 sec                                                                 | 1.70 sec: 1.07x slower                                                                 |
| html5lib       | 38.5 ms                                                                  | 42.8 ms: 1.11x slower                                                                  |
| tornado_http   | 91.8 ms                                                                  | 95.8 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                                    | 1.11x slower                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                   | 152 ms: 1.04x slower                                                                   |
| float          | 53.3 ms                                                                  | 62.4 ms: 1.17x slower                                                                  |
| nbody          | 70.9 ms                                                                  | 92.3 ms: 1.30x slower                                                                  |
| Geometric mean | (ref)                                                                    | 1.17x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.50 ms: 1.09x faster                                                                  |
| regex_dna      | 115 ms                                                                   | 116 ms: 1.01x slower                                                                   |
| regex_v8       | 13.5 ms                                                                  | 13.8 ms: 1.03x slower                                                                  |
| regex_compile  | 89.7 ms                                                                  | 103 ms: 1.15x slower                                                                   |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.78 ms: 1.33x faster                                                                  |
| unpickle_list        | 2.80 us                                                                  | 2.59 us: 1.08x faster                                                                  |
| unpickle             | 8.01 us                                                                  | 7.80 us: 1.03x faster                                                                  |
| xml_etree_parse      | 92.1 ms                                                                  | 94.4 ms: 1.03x slower                                                                  |
| json_loads           | 13.5 us                                                                  | 13.9 us: 1.03x slower                                                                  |
| pickle_dict          | 18.6 us                                                                  | 19.6 us: 1.05x slower                                                                  |
| xml_etree_iterparse  | 61.8 ms                                                                  | 67.4 ms: 1.09x slower                                                                  |
| pickle               | 6.47 us                                                                  | 7.23 us: 1.12x slower                                                                  |
| pickle_list          | 2.70 us                                                                  | 3.10 us: 1.15x slower                                                                  |
| unpickle_pure_python | 150 us                                                                   | 173 us: 1.15x slower                                                                   |
| xml_etree_generate   | 52.3 ms                                                                  | 60.6 ms: 1.16x slower                                                                  |
| pickle_pure_python   | 203 us                                                                   | 239 us: 1.18x slower                                                                   |
| xml_etree_process    | 36.6 ms                                                                  | 44.2 ms: 1.21x slower                                                                  |
| Geometric mean       | (ref)                                                                    | 1.05x slower                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                                  |
| python_startup         | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                                  |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 17.5 ms: 1.01x slower                                                                  |
| django_template | 23.9 ms                                                                  | 25.3 ms: 1.06x slower                                                                  |
| mako            | 7.20 ms                                                                  | 7.79 ms: 1.08x slower                                                                  |
| Geometric mean  | (ref)                                                                    | 1.04x slower                                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| generators              | 33.5 ms                                                                  | 22.5 ms: 1.49x faster                                                                  |
| asyncio_tcp             | 674 ms                                                                   | 492 ms: 1.37x faster                                                                   |
| json_dumps              | 7.71 ms                                                                  | 5.78 ms: 1.33x faster                                                                  |
| json                    | 3.20 ms                                                                  | 2.78 ms: 1.15x faster                                                                  |
| mypy2                   | 276 ms                                                                   | 246 ms: 1.12x faster                                                                   |
| mdp                     | 1.67 sec                                                                 | 1.50 sec: 1.12x faster                                                                 |
| regex_effbot            | 1.63 ms                                                                  | 1.50 ms: 1.09x faster                                                                  |
| unpickle_list           | 2.80 us                                                                  | 2.59 us: 1.08x faster                                                                  |
| unpickle                | 8.01 us                                                                  | 7.80 us: 1.03x faster                                                                  |
| coverage                | 55.3 ms                                                                  | 53.8 ms: 1.03x faster                                                                  |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 502 ms: 1.02x faster                                                                   |
| regex_dna               | 115 ms                                                                   | 116 ms: 1.01x slower                                                                   |
| deltablue               | 2.68 ms                                                                  | 2.70 ms: 1.01x slower                                                                  |
| sympy_expand            | 298 ms                                                                   | 302 ms: 1.01x slower                                                                   |
| genshi_text             | 17.3 ms                                                                  | 17.5 ms: 1.01x slower                                                                  |
| thrift                  | 487 us                                                                   | 494 us: 1.02x slower                                                                   |
| xml_etree_parse         | 92.1 ms                                                                  | 94.4 ms: 1.03x slower                                                                  |
| regex_v8                | 13.5 ms                                                                  | 13.8 ms: 1.03x slower                                                                  |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                                  |
| json_loads              | 13.5 us                                                                  | 13.9 us: 1.03x slower                                                                  |
| python_startup          | 18.4 ms                                                                  | 18.9 ms: 1.03x slower                                                                  |
| dulwich_log             | 43.4 ms                                                                  | 45.0 ms: 1.04x slower                                                                  |
| nqueens                 | 65.1 ms                                                                  | 67.5 ms: 1.04x slower                                                                  |
| sqlglot_normalize       | 189 ms                                                                   | 196 ms: 1.04x slower                                                                   |
| pidigits                | 147 ms                                                                   | 152 ms: 1.04x slower                                                                   |
| sympy_str               | 184 ms                                                                   | 192 ms: 1.04x slower                                                                   |
| logging_silent          | 71.0 ns                                                                  | 73.9 ns: 1.04x slower                                                                  |
| tornado_http            | 91.8 ms                                                                  | 95.8 ms: 1.04x slower                                                                  |
| bench_thread_pool       | 856 us                                                                   | 897 us: 1.05x slower                                                                   |
| pickle_dict             | 18.6 us                                                                  | 19.6 us: 1.05x slower                                                                  |
| logging_format          | 7.13 us                                                                  | 7.54 us: 1.06x slower                                                                  |
| richards                | 32.1 ms                                                                  | 33.9 ms: 1.06x slower                                                                  |
| django_template         | 23.9 ms                                                                  | 25.3 ms: 1.06x slower                                                                  |
| sqlglot_optimize        | 34.5 ms                                                                  | 36.6 ms: 1.06x slower                                                                  |
| create_gc_cycles        | 666 us                                                                   | 711 us: 1.07x slower                                                                   |
| docutils                | 1.59 sec                                                                 | 1.70 sec: 1.07x slower                                                                 |
| sympy_sum               | 98.9 ms                                                                  | 106 ms: 1.07x slower                                                                   |
| async_tree_io           | 744 ms                                                                   | 802 ms: 1.08x slower                                                                   |
| mako                    | 7.20 ms                                                                  | 7.79 ms: 1.08x slower                                                                  |
| gc_traversal            | 1.40 ms                                                                  | 1.52 ms: 1.08x slower                                                                  |
| raytrace                | 206 ms                                                                   | 223 ms: 1.08x slower                                                                   |
| async_tree_memoization  | 374 ms                                                                   | 407 ms: 1.09x slower                                                                   |
| sympy_integrate         | 13.7 ms                                                                  | 14.9 ms: 1.09x slower                                                                  |
| xml_etree_iterparse     | 61.8 ms                                                                  | 67.4 ms: 1.09x slower                                                                  |
| async_tree_none         | 313 ms                                                                   | 342 ms: 1.09x slower                                                                   |
| telco                   | 3.93 ms                                                                  | 4.31 ms: 1.10x slower                                                                  |
| coroutines              | 14.8 ms                                                                  | 16.4 ms: 1.11x slower                                                                  |
| html5lib                | 38.5 ms                                                                  | 42.8 ms: 1.11x slower                                                                  |
| logging_simple          | 6.60 us                                                                  | 7.36 us: 1.12x slower                                                                  |
| pickle                  | 6.47 us                                                                  | 7.23 us: 1.12x slower                                                                  |
| sqlite_synth            | 1.67 us                                                                  | 1.87 us: 1.12x slower                                                                  |
| bench_mp_pool           | 61.2 ms                                                                  | 68.7 ms: 1.12x slower                                                                  |
| spectral_norm           | 71.8 ms                                                                  | 81.1 ms: 1.13x slower                                                                  |
| go                      | 97.5 ms                                                                  | 110 ms: 1.13x slower                                                                   |
| pycparser               | 686 ms                                                                   | 776 ms: 1.13x slower                                                                   |
| deepcopy_reduce         | 2.06 us                                                                  | 2.35 us: 1.14x slower                                                                  |
| 2to3                    | 204 ms                                                                   | 234 ms: 1.15x slower                                                                   |
| meteor_contest          | 74.4 ms                                                                  | 85.3 ms: 1.15x slower                                                                  |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 3.02 ms: 1.15x slower                                                                  |
| pickle_list             | 2.70 us                                                                  | 3.10 us: 1.15x slower                                                                  |
| pprint_safe_repr        | 512 ms                                                                   | 588 ms: 1.15x slower                                                                   |
| regex_compile           | 89.7 ms                                                                  | 103 ms: 1.15x slower                                                                   |
| pprint_pformat          | 1.05 sec                                                                 | 1.21 sec: 1.15x slower                                                                 |
| unpickle_pure_python    | 150 us                                                                   | 173 us: 1.15x slower                                                                   |
| deepcopy                | 240 us                                                                   | 278 us: 1.16x slower                                                                   |
| chaos                   | 47.3 ms                                                                  | 54.8 ms: 1.16x slower                                                                  |
| xml_etree_generate      | 52.3 ms                                                                  | 60.6 ms: 1.16x slower                                                                  |
| scimark_lu              | 62.8 ms                                                                  | 73.2 ms: 1.16x slower                                                                  |
| crypto_pyaes            | 48.3 ms                                                                  | 56.3 ms: 1.17x slower                                                                  |
| pathlib                 | 72.9 ms                                                                  | 85.3 ms: 1.17x slower                                                                  |
| float                   | 53.3 ms                                                                  | 62.4 ms: 1.17x slower                                                                  |
| pickle_pure_python      | 203 us                                                                   | 239 us: 1.18x slower                                                                   |
| deepcopy_memo           | 25.3 us                                                                  | 29.8 us: 1.18x slower                                                                  |
| pyflate                 | 302 ms                                                                   | 357 ms: 1.18x slower                                                                   |
| chameleon               | 5.15 ms                                                                  | 6.13 ms: 1.19x slower                                                                  |
| hexiom                  | 4.46 ms                                                                  | 5.32 ms: 1.19x slower                                                                  |
| comprehensions          | 15.4 us                                                                  | 18.5 us: 1.20x slower                                                                  |
| scimark_fft             | 183 ms                                                                   | 220 ms: 1.20x slower                                                                   |
| xml_etree_process       | 36.6 ms                                                                  | 44.2 ms: 1.21x slower                                                                  |
| sqlglot_parse           | 929 us                                                                   | 1.13 ms: 1.22x slower                                                                  |
| scimark_monte_carlo     | 45.8 ms                                                                  | 56.0 ms: 1.22x slower                                                                  |
| fannkuch                | 255 ms                                                                   | 313 ms: 1.23x slower                                                                   |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.39 ms: 1.23x slower                                                                  |
| nbody                   | 70.9 ms                                                                  | 92.3 ms: 1.30x slower                                                                  |
| async_generators        | 180 ms                                                                   | 239 ms: 1.33x slower                                                                   |
| scimark_sor             | 77.7 ms                                                                  | 104 ms: 1.35x slower                                                                   |
| unpack_sequence         | 43.1 ns                                                                  | 61.7 ns: 1.43x slower                                                                  |
| dask                    | 267 ms                                                                   | 417 ms: 1.56x slower                                                                   |
| Geometric mean          | (ref)                                                                    | 1.09x slower                                                                           |

Benchmark hidden because not significant (1): genshi_xml
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
