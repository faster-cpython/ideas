
# Results vs. 3.11.0

- fork: python
- ref: cdde29dde90947df9bac
- machine: windows-amd64
- commit hash: cdde29d
- commit date: 2022-11-21
- overall geometric mean: 1.08x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 194 ms: 1.05x faster                                                        |
| chameleon      | 5.15 ms                                                                  | 4.62 ms: 1.12x faster                                                       |
| docutils       | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| html5lib       | 38.5 ms                                                                  | 34.8 ms: 1.10x faster                                                       |
| tornado_http   | 91.8 ms                                                                  | 88.1 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 59.0 ms: 1.20x faster                                                       |
| float          | 53.3 ms                                                                  | 51.0 ms: 1.04x faster                                                       |
| pidigits       | 147 ms                                                                   | 148 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 89.7 ms                                                                  | 81.1 ms: 1.11x faster                                                       |
| regex_effbot   | 1.63 ms                                                                  | 1.53 ms: 1.06x faster                                                       |
| regex_dna      | 115 ms                                                                   | 118 ms: 1.02x slower                                                        |
| regex_v8       | 13.5 ms                                                                  | 13.9 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 7.71 ms                                                                  | 5.35 ms: 1.44x faster                                                       |
| pickle_pure_python   | 203 us                                                                   | 177 us: 1.15x faster                                                        |
| unpickle_pure_python | 150 us                                                                   | 131 us: 1.14x faster                                                        |
| xml_etree_process    | 36.6 ms                                                                  | 33.6 ms: 1.09x faster                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 48.4 ms: 1.08x faster                                                       |
| unpickle_list        | 2.80 us                                                                  | 2.64 us: 1.06x faster                                                       |
| json_loads           | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| xml_etree_parse      | 92.1 ms                                                                  | 91.0 ms: 1.01x faster                                                       |
| xml_etree_iterparse  | 61.8 ms                                                                  | 64.0 ms: 1.04x slower                                                       |
| pickle_dict          | 18.6 us                                                                  | 19.4 us: 1.04x slower                                                       |
| unpickle             | 8.01 us                                                                  | 8.52 us: 1.06x slower                                                       |
| pickle               | 6.47 us                                                                  | 7.13 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| python_startup_no_site | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 17.3 ms                                                                  | 13.9 ms: 1.24x faster                                                       |
| genshi_xml      | 38.0 ms                                                                  | 32.4 ms: 1.17x faster                                                       |
| django_template | 23.9 ms                                                                  | 21.0 ms: 1.14x faster                                                       |
| mako            | 7.20 ms                                                                  | 6.38 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                                    | 1.17x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpack_sequence         | 43.1 ns                                                                  | 26.3 ns: 1.64x faster                                                       |
| json_dumps              | 7.71 ms                                                                  | 5.35 ms: 1.44x faster                                                       |
| richards                | 32.1 ms                                                                  | 24.8 ms: 1.30x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.08 ms: 1.29x faster                                                       |
| mypy2                   | 276 ms                                                                   | 216 ms: 1.28x faster                                                        |
| genshi_text             | 17.3 ms                                                                  | 13.9 ms: 1.24x faster                                                       |
| logging_silent          | 71.0 ns                                                                  | 57.8 ns: 1.23x faster                                                       |
| spectral_norm           | 71.8 ms                                                                  | 59.7 ms: 1.20x faster                                                       |
| nbody                   | 70.9 ms                                                                  | 59.0 ms: 1.20x faster                                                       |
| deepcopy_memo           | 25.3 us                                                                  | 21.4 us: 1.19x faster                                                       |
| go                      | 97.5 ms                                                                  | 82.9 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.24 ms: 1.17x faster                                                       |
| genshi_xml              | 38.0 ms                                                                  | 32.4 ms: 1.17x faster                                                       |
| json                    | 3.20 ms                                                                  | 2.78 ms: 1.15x faster                                                       |
| hexiom                  | 4.46 ms                                                                  | 3.87 ms: 1.15x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 177 us: 1.15x faster                                                        |
| unpickle_pure_python    | 150 us                                                                   | 131 us: 1.14x faster                                                        |
| nqueens                 | 65.1 ms                                                                  | 57.1 ms: 1.14x faster                                                       |
| django_template         | 23.9 ms                                                                  | 21.0 ms: 1.14x faster                                                       |
| fannkuch                | 255 ms                                                                   | 225 ms: 1.13x faster                                                        |
| raytrace                | 206 ms                                                                   | 182 ms: 1.13x faster                                                        |
| pyflate                 | 302 ms                                                                   | 267 ms: 1.13x faster                                                        |
| deepcopy                | 240 us                                                                   | 212 us: 1.13x faster                                                        |
| mako                    | 7.20 ms                                                                  | 6.38 ms: 1.13x faster                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 1.82 us: 1.13x faster                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 934 ms: 1.12x faster                                                        |
| chaos                   | 47.3 ms                                                                  | 42.2 ms: 1.12x faster                                                       |
| pprint_safe_repr        | 512 ms                                                                   | 458 ms: 1.12x faster                                                        |
| scimark_sor             | 77.7 ms                                                                  | 69.5 ms: 1.12x faster                                                       |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.01 ms: 1.12x faster                                                       |
| chameleon               | 5.15 ms                                                                  | 4.62 ms: 1.12x faster                                                       |
| sqlglot_parse           | 929 us                                                                   | 833 us: 1.11x faster                                                        |
| logging_format          | 7.13 us                                                                  | 6.39 us: 1.11x faster                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 31.0 ms: 1.11x faster                                                       |
| regex_compile           | 89.7 ms                                                                  | 81.1 ms: 1.11x faster                                                       |
| html5lib                | 38.5 ms                                                                  | 34.8 ms: 1.10x faster                                                       |
| xml_etree_process       | 36.6 ms                                                                  | 33.6 ms: 1.09x faster                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 174 ms: 1.09x faster                                                        |
| mdp                     | 1.67 sec                                                                 | 1.54 sec: 1.09x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 275 ms: 1.08x faster                                                        |
| scimark_monte_carlo     | 45.8 ms                                                                  | 42.3 ms: 1.08x faster                                                       |
| xml_etree_generate      | 52.3 ms                                                                  | 48.4 ms: 1.08x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 69.2 ms: 1.08x faster                                                       |
| scimark_lu              | 62.8 ms                                                                  | 58.9 ms: 1.07x faster                                                       |
| regex_effbot            | 1.63 ms                                                                  | 1.53 ms: 1.06x faster                                                       |
| sympy_str               | 184 ms                                                                   | 173 ms: 1.06x faster                                                        |
| unpickle_list           | 2.80 us                                                                  | 2.64 us: 1.06x faster                                                       |
| logging_simple          | 6.60 us                                                                  | 6.24 us: 1.06x faster                                                       |
| crypto_pyaes            | 48.3 ms                                                                  | 45.7 ms: 1.06x faster                                                       |
| dulwich_log             | 43.4 ms                                                                  | 41.1 ms: 1.06x faster                                                       |
| 2to3                    | 204 ms                                                                   | 194 ms: 1.05x faster                                                        |
| json_loads              | 13.5 us                                                                  | 12.9 us: 1.05x faster                                                       |
| sympy_integrate         | 13.7 ms                                                                  | 13.0 ms: 1.05x faster                                                       |
| telco                   | 3.93 ms                                                                  | 3.75 ms: 1.05x faster                                                       |
| float                   | 53.3 ms                                                                  | 51.0 ms: 1.04x faster                                                       |
| tornado_http            | 91.8 ms                                                                  | 88.1 ms: 1.04x faster                                                       |
| scimark_fft             | 183 ms                                                                   | 175 ms: 1.04x faster                                                        |
| coverage                | 55.3 ms                                                                  | 53.2 ms: 1.04x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 95.2 ms: 1.04x faster                                                       |
| dask                    | 267 ms                                                                   | 257 ms: 1.04x faster                                                        |
| async_tree_memoization  | 374 ms                                                                   | 363 ms: 1.03x faster                                                        |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 496 ms: 1.03x faster                                                        |
| docutils                | 1.59 sec                                                                 | 1.55 sec: 1.03x faster                                                      |
| async_generators        | 180 ms                                                                   | 176 ms: 1.03x faster                                                        |
| coroutines              | 14.8 ms                                                                  | 14.5 ms: 1.02x faster                                                       |
| comprehensions          | 15.4 us                                                                  | 15.1 us: 1.02x faster                                                       |
| thrift                  | 487 us                                                                   | 478 us: 1.02x faster                                                        |
| bench_thread_pool       | 856 us                                                                   | 842 us: 1.02x faster                                                        |
| xml_etree_parse         | 92.1 ms                                                                  | 91.0 ms: 1.01x faster                                                       |
| pidigits                | 147 ms                                                                   | 148 ms: 1.01x slower                                                        |
| python_startup          | 18.4 ms                                                                  | 18.7 ms: 1.02x slower                                                       |
| generators              | 33.5 ms                                                                  | 34.4 ms: 1.02x slower                                                       |
| regex_dna               | 115 ms                                                                   | 118 ms: 1.02x slower                                                        |
| python_startup_no_site  | 15.4 ms                                                                  | 15.8 ms: 1.03x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.9 ms: 1.03x slower                                                       |
| create_gc_cycles        | 666 us                                                                   | 685 us: 1.03x slower                                                        |
| bench_mp_pool           | 61.2 ms                                                                  | 63.3 ms: 1.03x slower                                                       |
| xml_etree_iterparse     | 61.8 ms                                                                  | 64.0 ms: 1.04x slower                                                       |
| pickle_dict             | 18.6 us                                                                  | 19.4 us: 1.04x slower                                                       |
| pathlib                 | 72.9 ms                                                                  | 76.4 ms: 1.05x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 783 ms: 1.05x slower                                                        |
| gc_traversal            | 1.40 ms                                                                  | 1.48 ms: 1.06x slower                                                       |
| unpickle                | 8.01 us                                                                  | 8.52 us: 1.06x slower                                                       |
| sqlite_synth            | 1.67 us                                                                  | 1.80 us: 1.07x slower                                                       |
| pickle                  | 6.47 us                                                                  | 7.13 us: 1.10x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 747 ms: 1.11x slower                                                        |
| Geometric mean          | (ref)                                                                    | 1.08x faster                                                                |

Benchmark hidden because not significant (3): async_tree_none, pycparser, pickle_list
Ignored benchmarks (5) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
