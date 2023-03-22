
# Results vs. 3.11.0

- fork: python
- ref: e2b4e4bab90b69fbd361
- machine: windows-amd64
- commit hash: e2b4e4b
- commit date: 2021-11-05
- overall geometric mean: 1.08x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 210 ms: 1.03x slower                                                       |
| chameleon      | 5.15 ms                                                                  | 5.53 ms: 1.07x slower                                                      |
| docutils       | 1.59 sec                                                                 | 1.67 sec: 1.05x slower                                                     |
| html5lib       | 38.5 ms                                                                  | 41.4 ms: 1.08x slower                                                      |
| tornado_http   | 91.8 ms                                                                  | 98.3 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.06x slower                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 147 ms                                                                   | 148 ms: 1.01x slower                                                       |
| float          | 53.3 ms                                                                  | 56.1 ms: 1.05x slower                                                      |
| nbody          | 70.9 ms                                                                  | 90.3 ms: 1.27x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.11x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 90.4 ms: 1.01x slower                                                      |
| regex_effbot   | 1.63 ms                                                                  | 1.82 ms: 1.11x slower                                                      |
| regex_dna      | 115 ms                                                                   | 131 ms: 1.14x slower                                                       |
| regex_v8       | 13.5 ms                                                                  | 16.6 ms: 1.23x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.12x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 18.6 us                                                                  | 16.2 us: 1.15x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.54 us: 1.10x faster                                                      |
| pickle_list          | 2.70 us                                                                  | 2.49 us: 1.09x faster                                                      |
| unpickle             | 8.01 us                                                                  | 7.81 us: 1.03x faster                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 93.8 ms: 1.02x slower                                                      |
| pickle               | 6.47 us                                                                  | 6.61 us: 1.02x slower                                                      |
| json_dumps           | 7.71 ms                                                                  | 7.94 ms: 1.03x slower                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 54.7 ms: 1.05x slower                                                      |
| xml_etree_iterparse  | 61.8 ms                                                                  | 65.2 ms: 1.05x slower                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 39.7 ms: 1.09x slower                                                      |
| json_loads           | 13.5 us                                                                  | 14.9 us: 1.10x slower                                                      |
| pickle_pure_python   | 203 us                                                                   | 228 us: 1.12x slower                                                       |
| unpickle_pure_python | 150 us                                                                   | 168 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.02x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 15.4 ms                                                                  | 15.1 ms: 1.02x faster                                                      |
| python_startup         | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                      |
| Geometric mean         | (ref)                                                                    | 1.00x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 17.5 ms: 1.01x slower                                                      |
| django_template | 23.9 ms                                                                  | 26.0 ms: 1.09x slower                                                      |
| mako            | 7.20 ms                                                                  | 8.07 ms: 1.12x slower                                                      |
| Geometric mean  | (ref)                                                                    | 1.06x slower                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| logging_simple          | 6.60 us                                                                  | 5.45 us: 1.21x faster                                                      |
| logging_format          | 7.13 us                                                                  | 5.92 us: 1.20x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 16.2 us: 1.15x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.54 us: 1.10x faster                                                      |
| pickle_list             | 2.70 us                                                                  | 2.49 us: 1.09x faster                                                      |
| generators              | 33.5 ms                                                                  | 31.0 ms: 1.08x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.61 sec: 1.04x faster                                                     |
| unpickle                | 8.01 us                                                                  | 7.81 us: 1.03x faster                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.37 ms: 1.02x faster                                                      |
| python_startup_no_site  | 15.4 ms                                                                  | 15.1 ms: 1.02x faster                                                      |
| async_tree_none         | 313 ms                                                                   | 307 ms: 1.02x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.91 ms: 1.01x faster                                                      |
| flaskblogging           | 2.04 sec                                                                 | 2.05 sec: 1.00x slower                                                     |
| pidigits                | 147 ms                                                                   | 148 ms: 1.01x slower                                                       |
| regex_compile           | 89.7 ms                                                                  | 90.4 ms: 1.01x slower                                                      |
| genshi_text             | 17.3 ms                                                                  | 17.5 ms: 1.01x slower                                                      |
| dulwich_log             | 43.4 ms                                                                  | 44.1 ms: 1.01x slower                                                      |
| logging_silent          | 71.0 ns                                                                  | 72.1 ns: 1.01x slower                                                      |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.6 ms: 1.02x slower                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 93.8 ms: 1.02x slower                                                      |
| pickle                  | 6.47 us                                                                  | 6.61 us: 1.02x slower                                                      |
| meteor_contest          | 74.4 ms                                                                  | 76.2 ms: 1.02x slower                                                      |
| python_startup          | 18.4 ms                                                                  | 18.8 ms: 1.02x slower                                                      |
| sympy_sum               | 98.9 ms                                                                  | 102 ms: 1.03x slower                                                       |
| json_dumps              | 7.71 ms                                                                  | 7.94 ms: 1.03x slower                                                      |
| create_gc_cycles        | 666 us                                                                   | 686 us: 1.03x slower                                                       |
| 2to3                    | 204 ms                                                                   | 210 ms: 1.03x slower                                                       |
| nqueens                 | 65.1 ms                                                                  | 67.3 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 530 ms: 1.03x slower                                                       |
| sympy_str               | 184 ms                                                                   | 191 ms: 1.04x slower                                                       |
| raytrace                | 206 ms                                                                   | 214 ms: 1.04x slower                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 196 ms: 1.04x slower                                                       |
| sympy_expand            | 298 ms                                                                   | 311 ms: 1.04x slower                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 54.7 ms: 1.05x slower                                                      |
| docutils                | 1.59 sec                                                                 | 1.67 sec: 1.05x slower                                                     |
| float                   | 53.3 ms                                                                  | 56.1 ms: 1.05x slower                                                      |
| sympy_integrate         | 13.7 ms                                                                  | 14.4 ms: 1.05x slower                                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 65.2 ms: 1.05x slower                                                      |
| async_tree_memoization  | 374 ms                                                                   | 395 ms: 1.06x slower                                                       |
| richards                | 32.1 ms                                                                  | 34.0 ms: 1.06x slower                                                      |
| bench_thread_pool       | 856 us                                                                   | 906 us: 1.06x slower                                                       |
| async_generators        | 180 ms                                                                   | 192 ms: 1.06x slower                                                       |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 88.5 ms: 1.07x slower                                                      |
| async_tree_io           | 744 ms                                                                   | 793 ms: 1.07x slower                                                       |
| deltablue               | 2.68 ms                                                                  | 2.86 ms: 1.07x slower                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 547 ms: 1.07x slower                                                       |
| tornado_http            | 91.8 ms                                                                  | 98.3 ms: 1.07x slower                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 1.13 sec: 1.07x slower                                                     |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.07x slower                                                      |
| chameleon               | 5.15 ms                                                                  | 5.53 ms: 1.07x slower                                                      |
| html5lib                | 38.5 ms                                                                  | 41.4 ms: 1.08x slower                                                      |
| fannkuch                | 255 ms                                                                   | 275 ms: 1.08x slower                                                       |
| thrift                  | 487 us                                                                   | 528 us: 1.08x slower                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 2.23 us: 1.09x slower                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 39.7 ms: 1.09x slower                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 37.5 ms: 1.09x slower                                                      |
| go                      | 97.5 ms                                                                  | 106 ms: 1.09x slower                                                       |
| django_template         | 23.9 ms                                                                  | 26.0 ms: 1.09x slower                                                      |
| json_loads              | 13.5 us                                                                  | 14.9 us: 1.10x slower                                                      |
| dask                    | 267 ms                                                                   | 295 ms: 1.10x slower                                                       |
| deepcopy                | 240 us                                                                   | 266 us: 1.11x slower                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 28.1 us: 1.11x slower                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.82 ms: 1.11x slower                                                      |
| pickle_pure_python      | 203 us                                                                   | 228 us: 1.12x slower                                                       |
| mako                    | 7.20 ms                                                                  | 8.07 ms: 1.12x slower                                                      |
| pycparser               | 686 ms                                                                   | 769 ms: 1.12x slower                                                       |
| unpickle_pure_python    | 150 us                                                                   | 168 us: 1.12x slower                                                       |
| scimark_monte_carlo     | 45.8 ms                                                                  | 51.7 ms: 1.13x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 5.06 ms: 1.13x slower                                                      |
| regex_dna               | 115 ms                                                                   | 131 ms: 1.14x slower                                                       |
| chaos                   | 47.3 ms                                                                  | 53.9 ms: 1.14x slower                                                      |
| spectral_norm           | 71.8 ms                                                                  | 82.7 ms: 1.15x slower                                                      |
| scimark_fft             | 183 ms                                                                   | 212 ms: 1.16x slower                                                       |
| pyflate                 | 302 ms                                                                   | 358 ms: 1.18x slower                                                       |
| unpack_sequence         | 43.1 ns                                                                  | 51.9 ns: 1.20x slower                                                      |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 3.18 ms: 1.21x slower                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 58.9 ms: 1.22x slower                                                      |
| coroutines              | 14.8 ms                                                                  | 18.1 ms: 1.22x slower                                                      |
| regex_v8                | 13.5 ms                                                                  | 16.6 ms: 1.23x slower                                                      |
| comprehensions          | 15.4 us                                                                  | 19.1 us: 1.24x slower                                                      |
| nbody                   | 70.9 ms                                                                  | 90.3 ms: 1.27x slower                                                      |
| scimark_lu              | 62.8 ms                                                                  | 81.5 ms: 1.30x slower                                                      |
| scimark_sor             | 77.7 ms                                                                  | 101 ms: 1.31x slower                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.50 ms: 1.32x slower                                                      |
| sqlglot_parse           | 929 us                                                                   | 1.29 ms: 1.39x slower                                                      |
| coverage                | 55.3 ms                                                                  | 262 ms: 4.74x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.08x slower                                                               |

Benchmark hidden because not significant (6): json, bench_mp_pool, pathlib, pylint, genshi_xml, asyncio_tcp
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, mypy2
