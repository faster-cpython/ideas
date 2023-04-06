
# Results vs. base

- fork: eduardo-elizondo
- ref: immortal_references
- machine: linux-x86_64
- commit hash: 030016a
- commit date: 2023-04-06
- overall geometric mean: 1.06x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 271 ms: 1.07x slower                                                              |
| chameleon      | 6.53 ms                                                                | 6.94 ms: 1.06x slower                                                             |
| docutils       | 2.53 sec                                                               | 2.80 sec: 1.10x slower                                                            |
| html5lib       | 62.0 ms                                                                | 66.6 ms: 1.07x slower                                                             |
| tornado_http   | 91.8 ms                                                                | 104 ms: 1.13x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 88.1 ms                                                                | 91.1 ms: 1.03x slower                                                             |
| pidigits       | 189 ms                                                                 | 197 ms: 1.05x slower                                                              |
| float          | 74.6 ms                                                                | 81.0 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                                             |
| regex_dna      | 202 ms                                                                 | 203 ms: 1.00x slower                                                              |
| regex_effbot   | 3.59 ms                                                                | 3.61 ms: 1.01x slower                                                             |
| regex_compile  | 135 ms                                                                 | 148 ms: 1.10x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_dict          | 31.2 us                                                                | 31.0 us: 1.01x faster                                                             |
| unpickle_list        | 5.09 us                                                                | 5.14 us: 1.01x slower                                                             |
| xml_etree_parse      | 148 ms                                                                 | 151 ms: 1.02x slower                                                              |
| pickle               | 10.4 us                                                                | 10.7 us: 1.03x slower                                                             |
| json_dumps           | 9.53 ms                                                                | 9.96 ms: 1.04x slower                                                             |
| xml_etree_generate   | 80.1 ms                                                                | 84.1 ms: 1.05x slower                                                             |
| pickle_list          | 4.21 us                                                                | 4.45 us: 1.06x slower                                                             |
| xml_etree_process    | 55.5 ms                                                                | 59.0 ms: 1.06x slower                                                             |
| json_loads           | 24.1 us                                                                | 25.8 us: 1.07x slower                                                             |
| unpickle_pure_python | 202 us                                                                 | 219 us: 1.08x slower                                                              |
| pickle_pure_python   | 286 us                                                                 | 316 us: 1.10x slower                                                              |
| Geometric mean       | (ref)                                                                  | 1.04x slower                                                                      |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 6.54 ms                                                                | 6.59 ms: 1.01x slower                                                             |
| python_startup         | 8.85 ms                                                                | 9.02 ms: 1.02x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 47.6 ms                                                                | 50.5 ms: 1.06x slower                                                             |
| django_template | 33.2 ms                                                                | 35.6 ms: 1.07x slower                                                             |
| genshi_text     | 21.1 ms                                                                | 22.9 ms: 1.08x slower                                                             |
| mako            | 10.1 ms                                                                | 11.0 ms: 1.09x slower                                                             |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_dict             | 31.2 us                                                                | 31.0 us: 1.01x faster                                                             |
| mdp                     | 2.70 sec                                                               | 2.68 sec: 1.01x faster                                                            |
| regex_v8                | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                                             |
| create_gc_cycles        | 1.47 ms                                                                | 1.48 ms: 1.00x slower                                                             |
| regex_dna               | 202 ms                                                                 | 203 ms: 1.00x slower                                                              |
| nqueens                 | 81.4 ms                                                                | 81.9 ms: 1.01x slower                                                             |
| regex_effbot            | 3.59 ms                                                                | 3.61 ms: 1.01x slower                                                             |
| python_startup_no_site  | 6.54 ms                                                                | 6.59 ms: 1.01x slower                                                             |
| gc_traversal            | 3.62 ms                                                                | 3.66 ms: 1.01x slower                                                             |
| unpickle_list           | 5.09 us                                                                | 5.14 us: 1.01x slower                                                             |
| go                      | 138 ms                                                                 | 140 ms: 1.01x slower                                                              |
| coverage                | 97.1 ms                                                                | 98.5 ms: 1.01x slower                                                             |
| async_tree_io           | 1.29 sec                                                               | 1.31 sec: 1.02x slower                                                            |
| python_startup          | 8.85 ms                                                                | 9.02 ms: 1.02x slower                                                             |
| xml_etree_parse         | 148 ms                                                                 | 151 ms: 1.02x slower                                                              |
| async_tree_none         | 527 ms                                                                 | 539 ms: 1.02x slower                                                              |
| async_tree_cpu_io_mixed | 742 ms                                                                 | 761 ms: 1.03x slower                                                              |
| pickle                  | 10.4 us                                                                | 10.7 us: 1.03x slower                                                             |
| asyncio_tcp             | 503 ms                                                                 | 517 ms: 1.03x slower                                                              |
| pathlib                 | 17.9 ms                                                                | 18.5 ms: 1.03x slower                                                             |
| thrift                  | 777 us                                                                 | 802 us: 1.03x slower                                                              |
| async_tree_memoization  | 658 ms                                                                 | 680 ms: 1.03x slower                                                              |
| fannkuch                | 378 ms                                                                 | 391 ms: 1.03x slower                                                              |
| nbody                   | 88.1 ms                                                                | 91.1 ms: 1.03x slower                                                             |
| async_generators        | 415 ms                                                                 | 429 ms: 1.03x slower                                                              |
| sqlite_synth            | 2.59 us                                                                | 2.70 us: 1.04x slower                                                             |
| pycparser               | 1.12 sec                                                               | 1.16 sec: 1.04x slower                                                            |
| djangocms               | 32.7 us                                                                | 34.1 us: 1.04x slower                                                             |
| telco                   | 6.45 ms                                                                | 6.73 ms: 1.04x slower                                                             |
| json_dumps              | 9.53 ms                                                                | 9.96 ms: 1.04x slower                                                             |
| hexiom                  | 6.05 ms                                                                | 6.33 ms: 1.05x slower                                                             |
| pidigits                | 189 ms                                                                 | 197 ms: 1.05x slower                                                              |
| xml_etree_generate      | 80.1 ms                                                                | 84.1 ms: 1.05x slower                                                             |
| pickle_list             | 4.21 us                                                                | 4.45 us: 1.06x slower                                                             |
| pprint_pformat          | 1.42 sec                                                               | 1.50 sec: 1.06x slower                                                            |
| scimark_lu              | 107 ms                                                                 | 114 ms: 1.06x slower                                                              |
| comprehensions          | 23.7 us                                                                | 25.1 us: 1.06x slower                                                             |
| genshi_xml              | 47.6 ms                                                                | 50.5 ms: 1.06x slower                                                             |
| richards                | 43.2 ms                                                                | 45.9 ms: 1.06x slower                                                             |
| xml_etree_process       | 55.5 ms                                                                | 59.0 ms: 1.06x slower                                                             |
| chameleon               | 6.53 ms                                                                | 6.94 ms: 1.06x slower                                                             |
| bench_thread_pool       | 787 us                                                                 | 838 us: 1.06x slower                                                              |
| raytrace                | 280 ms                                                                 | 298 ms: 1.06x slower                                                              |
| chaos                   | 66.2 ms                                                                | 70.5 ms: 1.06x slower                                                             |
| scimark_monte_carlo     | 67.5 ms                                                                | 71.9 ms: 1.07x slower                                                             |
| json_loads              | 24.1 us                                                                | 25.8 us: 1.07x slower                                                             |
| django_template         | 33.2 ms                                                                | 35.6 ms: 1.07x slower                                                             |
| pprint_safe_repr        | 687 ms                                                                 | 737 ms: 1.07x slower                                                              |
| 2to3                    | 252 ms                                                                 | 271 ms: 1.07x slower                                                              |
| html5lib                | 62.0 ms                                                                | 66.6 ms: 1.07x slower                                                             |
| logging_silent          | 95.2 ns                                                                | 103 ns: 1.08x slower                                                              |
| unpickle_pure_python    | 202 us                                                                 | 219 us: 1.08x slower                                                              |
| crypto_pyaes            | 73.8 ms                                                                | 80.0 ms: 1.08x slower                                                             |
| sqlglot_optimize        | 51.2 ms                                                                | 55.6 ms: 1.08x slower                                                             |
| genshi_text             | 21.1 ms                                                                | 22.9 ms: 1.08x slower                                                             |
| float                   | 74.6 ms                                                                | 81.0 ms: 1.09x slower                                                             |
| sqlglot_normalize       | 105 ms                                                                 | 115 ms: 1.09x slower                                                              |
| mako                    | 10.1 ms                                                                | 11.0 ms: 1.09x slower                                                             |
| sympy_integrate         | 20.4 ms                                                                | 22.2 ms: 1.09x slower                                                             |
| dask                    | 510 ms                                                                 | 555 ms: 1.09x slower                                                              |
| generators              | 29.2 ms                                                                | 31.8 ms: 1.09x slower                                                             |
| sqlglot_parse           | 1.44 ms                                                                | 1.57 ms: 1.09x slower                                                             |
| sqlalchemy_declarative  | 136 ms                                                                 | 149 ms: 1.10x slower                                                              |
| regex_compile           | 135 ms                                                                 | 148 ms: 1.10x slower                                                              |
| deltablue               | 3.27 ms                                                                | 3.59 ms: 1.10x slower                                                             |
| mypy2                   | 333 ms                                                                 | 366 ms: 1.10x slower                                                              |
| sympy_expand            | 461 ms                                                                 | 506 ms: 1.10x slower                                                              |
| deepcopy_reduce         | 2.97 us                                                                | 3.26 us: 1.10x slower                                                             |
| dulwich_log             | 63.4 ms                                                                | 69.8 ms: 1.10x slower                                                             |
| meteor_contest          | 103 ms                                                                 | 113 ms: 1.10x slower                                                              |
| sqlglot_transpile       | 1.73 ms                                                                | 1.90 ms: 1.10x slower                                                             |
| pickle_pure_python      | 286 us                                                                 | 316 us: 1.10x slower                                                              |
| docutils                | 2.53 sec                                                               | 2.80 sec: 1.10x slower                                                            |
| logging_format          | 6.34 us                                                                | 7.00 us: 1.10x slower                                                             |
| deepcopy_memo           | 34.7 us                                                                | 38.5 us: 1.11x slower                                                             |
| sympy_sum               | 165 ms                                                                 | 183 ms: 1.11x slower                                                              |
| pyflate                 | 417 ms                                                                 | 464 ms: 1.11x slower                                                              |
| json                    | 4.62 ms                                                                | 5.15 ms: 1.12x slower                                                             |
| logging_simple          | 5.69 us                                                                | 6.35 us: 1.12x slower                                                             |
| sqlalchemy_imperative   | 17.7 ms                                                                | 19.8 ms: 1.12x slower                                                             |
| deepcopy                | 328 us                                                                 | 367 us: 1.12x slower                                                              |
| sympy_str               | 285 ms                                                                 | 319 ms: 1.12x slower                                                              |
| spectral_norm           | 94.7 ms                                                                | 107 ms: 1.13x slower                                                              |
| tornado_http            | 91.8 ms                                                                | 104 ms: 1.13x slower                                                              |
| scimark_fft             | 308 ms                                                                 | 352 ms: 1.14x slower                                                              |
| scimark_sparse_mat_mult | 4.05 ms                                                                | 4.64 ms: 1.15x slower                                                             |
| unpack_sequence         | 43.1 ns                                                                | 53.0 ns: 1.23x slower                                                             |
| scimark_sor             | 111 ms                                                                 | 137 ms: 1.24x slower                                                              |
| Geometric mean          | (ref)                                                                  | 1.06x slower                                                                      |

Benchmark hidden because not significant (4): coroutines, bench_mp_pool, xml_etree_iterparse, unpickle
Ignored benchmarks (2) of public/results/bm-20230402-3.12.0a6+-385b5d6/bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6+-385b5d6.json: aiohttp, gunicorn
