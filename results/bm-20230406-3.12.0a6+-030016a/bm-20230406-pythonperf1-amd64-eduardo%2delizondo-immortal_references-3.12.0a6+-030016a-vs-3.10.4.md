
# Results vs. 3.10.4

- fork: eduardo-elizondo
- ref: immortal_references
- machine: windows-amd64
- commit hash: 030016a
- commit date: 2023-04-06
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 234 ms: 1.02x slower                                                                   |
| chameleon      | 5.77 ms                                                                  | 6.13 ms: 1.06x slower                                                                  |
| docutils       | 1.83 sec                                                                 | 1.70 sec: 1.08x faster                                                                 |
| html5lib       | 47.3 ms                                                                  | 42.8 ms: 1.11x faster                                                                  |
| tornado_http   | 106 ms                                                                   | 95.8 ms: 1.11x faster                                                                  |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 145 ms                                                                   | 152 ms: 1.05x slower                                                                   |
| float          | 59.5 ms                                                                  | 62.4 ms: 1.05x slower                                                                  |
| nbody          | 71.5 ms                                                                  | 92.3 ms: 1.29x slower                                                                  |
| Geometric mean | (ref)                                                                    | 1.12x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                                   | 116 ms: 1.13x faster                                                                   |
| regex_effbot   | 1.64 ms                                                                  | 1.50 ms: 1.09x faster                                                                  |
| regex_v8       | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                                  |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps           | 9.00 ms                                                                  | 5.78 ms: 1.56x faster                                                                  |
| unpickle             | 8.88 us                                                                  | 7.80 us: 1.14x faster                                                                  |
| pickle_pure_python   | 264 us                                                                   | 239 us: 1.10x faster                                                                   |
| unpickle_list        | 2.71 us                                                                  | 2.59 us: 1.05x faster                                                                  |
| unpickle_pure_python | 179 us                                                                   | 173 us: 1.04x faster                                                                   |
| json_loads           | 14.2 us                                                                  | 13.9 us: 1.02x faster                                                                  |
| xml_etree_parse      | 95.6 ms                                                                  | 94.4 ms: 1.01x faster                                                                  |
| xml_etree_process    | 43.0 ms                                                                  | 44.2 ms: 1.03x slower                                                                  |
| xml_etree_iterparse  | 62.5 ms                                                                  | 67.4 ms: 1.08x slower                                                                  |
| pickle               | 6.67 us                                                                  | 7.23 us: 1.08x slower                                                                  |
| xml_etree_generate   | 53.8 ms                                                                  | 60.6 ms: 1.13x slower                                                                  |
| pickle_dict          | 16.7 us                                                                  | 19.6 us: 1.17x slower                                                                  |
| pickle_list          | 2.57 us                                                                  | 3.10 us: 1.21x slower                                                                  |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                                  |
| python_startup_no_site | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                                  |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 25.3 ms: 1.15x faster                                                                  |
| mako            | 8.69 ms                                                                  | 7.79 ms: 1.12x faster                                                                  |
| genshi_text     | 18.5 ms                                                                  | 17.5 ms: 1.06x faster                                                                  |
| genshi_xml      | 38.8 ms                                                                  | 38.2 ms: 1.02x faster                                                                  |
| Geometric mean  | (ref)                                                                    | 1.08x faster                                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-pythonperf1-amd64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps              | 9.00 ms                                                                  | 5.78 ms: 1.56x faster                                                                  |
| deltablue               | 4.15 ms                                                                  | 2.70 ms: 1.54x faster                                                                  |
| generators              | 31.4 ms                                                                  | 22.5 ms: 1.40x faster                                                                  |
| mypy2                   | 337 ms                                                                   | 246 ms: 1.37x faster                                                                   |
| asyncio_tcp             | 664 ms                                                                   | 492 ms: 1.35x faster                                                                   |
| go                      | 143 ms                                                                   | 110 ms: 1.30x faster                                                                   |
| logging_silent          | 94.6 ns                                                                  | 73.9 ns: 1.28x faster                                                                  |
| thrift                  | 632 us                                                                   | 494 us: 1.28x faster                                                                   |
| async_tree_io           | 1.02 sec                                                                 | 802 ms: 1.28x faster                                                                   |
| async_tree_none         | 414 ms                                                                   | 342 ms: 1.21x faster                                                                   |
| richards                | 41.0 ms                                                                  | 33.9 ms: 1.21x faster                                                                  |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 502 ms: 1.20x faster                                                                   |
| raytrace                | 267 ms                                                                   | 223 ms: 1.20x faster                                                                   |
| async_tree_memoization  | 485 ms                                                                   | 407 ms: 1.19x faster                                                                   |
| django_template         | 29.2 ms                                                                  | 25.3 ms: 1.15x faster                                                                  |
| scimark_lu              | 83.9 ms                                                                  | 73.2 ms: 1.15x faster                                                                  |
| json                    | 3.18 ms                                                                  | 2.78 ms: 1.14x faster                                                                  |
| unpickle                | 8.88 us                                                                  | 7.80 us: 1.14x faster                                                                  |
| regex_dna               | 131 ms                                                                   | 116 ms: 1.13x faster                                                                   |
| pycparser               | 873 ms                                                                   | 776 ms: 1.13x faster                                                                   |
| mako                    | 8.69 ms                                                                  | 7.79 ms: 1.12x faster                                                                  |
| tornado_http            | 106 ms                                                                   | 95.8 ms: 1.11x faster                                                                  |
| html5lib                | 47.3 ms                                                                  | 42.8 ms: 1.11x faster                                                                  |
| pickle_pure_python      | 264 us                                                                   | 239 us: 1.10x faster                                                                   |
| regex_effbot            | 1.64 ms                                                                  | 1.50 ms: 1.09x faster                                                                  |
| regex_v8                | 15.1 ms                                                                  | 13.8 ms: 1.09x faster                                                                  |
| crypto_pyaes            | 61.4 ms                                                                  | 56.3 ms: 1.09x faster                                                                  |
| pyflate                 | 388 ms                                                                   | 357 ms: 1.09x faster                                                                   |
| sqlglot_parse           | 1.22 ms                                                                  | 1.13 ms: 1.08x faster                                                                  |
| docutils                | 1.83 sec                                                                 | 1.70 sec: 1.08x faster                                                                 |
| create_gc_cycles        | 764 us                                                                   | 711 us: 1.08x faster                                                                   |
| mdp                     | 1.60 sec                                                                 | 1.50 sec: 1.07x faster                                                                 |
| chaos                   | 58.4 ms                                                                  | 54.8 ms: 1.07x faster                                                                  |
| bench_thread_pool       | 953 us                                                                   | 897 us: 1.06x faster                                                                   |
| genshi_text             | 18.5 ms                                                                  | 17.5 ms: 1.06x faster                                                                  |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.39 ms: 1.06x faster                                                                  |
| sqlglot_optimize        | 38.7 ms                                                                  | 36.6 ms: 1.06x faster                                                                  |
| unpickle_list           | 2.71 us                                                                  | 2.59 us: 1.05x faster                                                                  |
| dulwich_log             | 47.0 ms                                                                  | 45.0 ms: 1.04x faster                                                                  |
| unpickle_pure_python    | 179 us                                                                   | 173 us: 1.04x faster                                                                   |
| sympy_expand            | 313 ms                                                                   | 302 ms: 1.03x faster                                                                   |
| sqlglot_normalize       | 201 ms                                                                   | 196 ms: 1.03x faster                                                                   |
| hexiom                  | 5.45 ms                                                                  | 5.32 ms: 1.03x faster                                                                  |
| json_loads              | 14.2 us                                                                  | 13.9 us: 1.02x faster                                                                  |
| python_startup          | 19.3 ms                                                                  | 18.9 ms: 1.02x faster                                                                  |
| genshi_xml              | 38.8 ms                                                                  | 38.2 ms: 1.02x faster                                                                  |
| pprint_pformat          | 1.23 sec                                                                 | 1.21 sec: 1.01x faster                                                                 |
| xml_etree_parse         | 95.6 ms                                                                  | 94.4 ms: 1.01x faster                                                                  |
| pprint_safe_repr        | 593 ms                                                                   | 588 ms: 1.01x faster                                                                   |
| scimark_sor             | 104 ms                                                                   | 104 ms: 1.01x slower                                                                   |
| sympy_str               | 189 ms                                                                   | 192 ms: 1.02x slower                                                                   |
| sympy_integrate         | 14.7 ms                                                                  | 14.9 ms: 1.02x slower                                                                  |
| sqlite_synth            | 1.85 us                                                                  | 1.87 us: 1.02x slower                                                                  |
| 2to3                    | 229 ms                                                                   | 234 ms: 1.02x slower                                                                   |
| xml_etree_process       | 43.0 ms                                                                  | 44.2 ms: 1.03x slower                                                                  |
| sympy_sum               | 102 ms                                                                   | 106 ms: 1.03x slower                                                                   |
| nqueens                 | 64.8 ms                                                                  | 67.5 ms: 1.04x slower                                                                  |
| coroutines              | 15.6 ms                                                                  | 16.4 ms: 1.05x slower                                                                  |
| pidigits                | 145 ms                                                                   | 152 ms: 1.05x slower                                                                   |
| float                   | 59.5 ms                                                                  | 62.4 ms: 1.05x slower                                                                  |
| deepcopy_memo           | 28.4 us                                                                  | 29.8 us: 1.05x slower                                                                  |
| chameleon               | 5.77 ms                                                                  | 6.13 ms: 1.06x slower                                                                  |
| python_startup_no_site  | 14.8 ms                                                                  | 15.8 ms: 1.06x slower                                                                  |
| deepcopy_reduce         | 2.18 us                                                                  | 2.35 us: 1.08x slower                                                                  |
| xml_etree_iterparse     | 62.5 ms                                                                  | 67.4 ms: 1.08x slower                                                                  |
| deepcopy                | 256 us                                                                   | 278 us: 1.08x slower                                                                   |
| pickle                  | 6.67 us                                                                  | 7.23 us: 1.08x slower                                                                  |
| spectral_norm           | 74.3 ms                                                                  | 81.1 ms: 1.09x slower                                                                  |
| async_generators        | 214 ms                                                                   | 239 ms: 1.11x slower                                                                   |
| xml_etree_generate      | 53.8 ms                                                                  | 60.6 ms: 1.13x slower                                                                  |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 3.02 ms: 1.13x slower                                                                  |
| pathlib                 | 75.2 ms                                                                  | 85.3 ms: 1.13x slower                                                                  |
| gc_traversal            | 1.33 ms                                                                  | 1.52 ms: 1.14x slower                                                                  |
| telco                   | 3.77 ms                                                                  | 4.31 ms: 1.14x slower                                                                  |
| meteor_contest          | 74.3 ms                                                                  | 85.3 ms: 1.15x slower                                                                  |
| logging_format          | 6.53 us                                                                  | 7.54 us: 1.15x slower                                                                  |
| comprehensions          | 16.0 us                                                                  | 18.5 us: 1.16x slower                                                                  |
| bench_mp_pool           | 59.2 ms                                                                  | 68.7 ms: 1.16x slower                                                                  |
| pickle_dict             | 16.7 us                                                                  | 19.6 us: 1.17x slower                                                                  |
| scimark_fft             | 187 ms                                                                   | 220 ms: 1.18x slower                                                                   |
| logging_simple          | 6.12 us                                                                  | 7.36 us: 1.20x slower                                                                  |
| pickle_list             | 2.57 us                                                                  | 3.10 us: 1.21x slower                                                                  |
| fannkuch                | 252 ms                                                                   | 313 ms: 1.24x slower                                                                   |
| nbody                   | 71.5 ms                                                                  | 92.3 ms: 1.29x slower                                                                  |
| dask                    | 310 ms                                                                   | 417 ms: 1.34x slower                                                                   |
| coverage                | 37.5 ms                                                                  | 53.8 ms: 1.44x slower                                                                  |
| unpack_sequence         | 39.4 ns                                                                  | 61.7 ns: 1.57x slower                                                                  |
| Geometric mean          | (ref)                                                                    | 1.02x faster                                                                           |

Benchmark hidden because not significant (2): regex_compile, scimark_monte_carlo
Ignored benchmarks (5) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
