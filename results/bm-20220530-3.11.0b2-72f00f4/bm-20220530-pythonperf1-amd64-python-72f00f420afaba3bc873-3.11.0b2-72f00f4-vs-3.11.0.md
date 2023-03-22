
# Results vs. 3.11.0

- fork: python
- ref: 72f00f420afaba3bc873
- machine: windows-amd64
- commit hash: 72f00f4
- commit date: 2022-05-30
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 205 ms: 1.01x slower                                                       |
| chameleon      | 5.15 ms                                                                  | 5.35 ms: 1.04x slower                                                      |
| docutils       | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 39.6 ms: 1.03x slower                                                      |
| tornado_http   | 91.8 ms                                                                  | 91.0 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 68.5 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 1.63 ms                                                                  | 1.53 ms: 1.07x faster                                                      |
| regex_compile  | 89.7 ms                                                                  | 92.2 ms: 1.03x slower                                                      |
| regex_dna      | 115 ms                                                                   | 123 ms: 1.07x slower                                                       |
| regex_v8       | 13.5 ms                                                                  | 14.7 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 18.6 us                                                                  | 17.0 us: 1.09x faster                                                      |
| unpickle_list        | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                      |
| pickle_list          | 2.70 us                                                                  | 2.60 us: 1.04x faster                                                      |
| unpickle             | 8.01 us                                                                  | 7.81 us: 1.03x faster                                                      |
| pickle_pure_python   | 203 us                                                                   | 202 us: 1.01x faster                                                       |
| pickle               | 6.47 us                                                                  | 6.44 us: 1.00x faster                                                      |
| xml_etree_generate   | 52.3 ms                                                                  | 52.9 ms: 1.01x slower                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 93.2 ms: 1.01x slower                                                      |
| json_dumps           | 7.71 ms                                                                  | 7.87 ms: 1.02x slower                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 37.5 ms: 1.02x slower                                                      |
| unpickle_pure_python | 150 us                                                                   | 155 us: 1.04x slower                                                       |
| json_loads           | 13.5 us                                                                  | 14.3 us: 1.06x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 7.20 ms                                                                  | 7.10 ms: 1.01x faster                                                      |
| genshi_xml     | 38.0 ms                                                                  | 38.4 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| logging_format          | 7.13 us                                                                  | 6.10 us: 1.17x faster                                                      |
| logging_simple          | 6.60 us                                                                  | 5.65 us: 1.17x faster                                                      |
| pickle_dict             | 18.6 us                                                                  | 17.0 us: 1.09x faster                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.53 ms: 1.07x faster                                                      |
| unpickle_list           | 2.80 us                                                                  | 2.65 us: 1.06x faster                                                      |
| scimark_monte_carlo     | 45.8 ms                                                                  | 43.6 ms: 1.05x faster                                                      |
| richards                | 32.1 ms                                                                  | 30.5 ms: 1.05x faster                                                      |
| unpack_sequence         | 43.1 ns                                                                  | 41.1 ns: 1.05x faster                                                      |
| fannkuch                | 255 ms                                                                   | 245 ms: 1.04x faster                                                       |
| pickle_list             | 2.70 us                                                                  | 2.60 us: 1.04x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 68.5 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed | 512 ms                                                                   | 497 ms: 1.03x faster                                                       |
| unpickle                | 8.01 us                                                                  | 7.81 us: 1.03x faster                                                      |
| async_tree_memoization  | 374 ms                                                                   | 369 ms: 1.01x faster                                                       |
| mako                    | 7.20 ms                                                                  | 7.10 ms: 1.01x faster                                                      |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.3 ms: 1.01x faster                                                      |
| docutils                | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                     |
| tornado_http            | 91.8 ms                                                                  | 91.0 ms: 1.01x faster                                                      |
| async_tree_none         | 313 ms                                                                   | 310 ms: 1.01x faster                                                       |
| sympy_sum               | 98.9 ms                                                                  | 98.2 ms: 1.01x faster                                                      |
| spectral_norm           | 71.8 ms                                                                  | 71.3 ms: 1.01x faster                                                      |
| raytrace                | 206 ms                                                                   | 205 ms: 1.01x faster                                                       |
| pickle_pure_python      | 203 us                                                                   | 202 us: 1.01x faster                                                       |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 82.6 ms: 1.01x faster                                                      |
| pickle                  | 6.47 us                                                                  | 6.44 us: 1.00x faster                                                      |
| sympy_str               | 184 ms                                                                   | 185 ms: 1.01x slower                                                       |
| 2to3                    | 204 ms                                                                   | 205 ms: 1.01x slower                                                       |
| sympy_expand            | 298 ms                                                                   | 301 ms: 1.01x slower                                                       |
| scimark_sor             | 77.7 ms                                                                  | 78.3 ms: 1.01x slower                                                      |
| genshi_xml              | 38.0 ms                                                                  | 38.4 ms: 1.01x slower                                                      |
| async_generators        | 180 ms                                                                   | 182 ms: 1.01x slower                                                       |
| coroutines              | 14.8 ms                                                                  | 14.9 ms: 1.01x slower                                                      |
| sqlglot_normalize       | 189 ms                                                                   | 191 ms: 1.01x slower                                                       |
| go                      | 97.5 ms                                                                  | 98.5 ms: 1.01x slower                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 52.9 ms: 1.01x slower                                                      |
| gc_traversal            | 1.40 ms                                                                  | 1.42 ms: 1.01x slower                                                      |
| bench_thread_pool       | 856 us                                                                   | 865 us: 1.01x slower                                                       |
| logging_silent          | 71.0 ns                                                                  | 71.8 ns: 1.01x slower                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 93.2 ms: 1.01x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.70 us: 1.01x slower                                                      |
| scimark_lu              | 62.8 ms                                                                  | 63.8 ms: 1.02x slower                                                      |
| meteor_contest          | 74.4 ms                                                                  | 75.7 ms: 1.02x slower                                                      |
| chaos                   | 47.3 ms                                                                  | 48.2 ms: 1.02x slower                                                      |
| sqlglot_optimize        | 34.5 ms                                                                  | 35.2 ms: 1.02x slower                                                      |
| json_dumps              | 7.71 ms                                                                  | 7.87 ms: 1.02x slower                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 523 ms: 1.02x slower                                                       |
| generators              | 33.5 ms                                                                  | 34.3 ms: 1.02x slower                                                      |
| pycparser               | 686 ms                                                                   | 701 ms: 1.02x slower                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.69 ms: 1.02x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 4.56 ms: 1.02x slower                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 37.5 ms: 1.02x slower                                                      |
| pprint_pformat          | 1.05 sec                                                                 | 1.08 sec: 1.02x slower                                                     |
| mdp                     | 1.67 sec                                                                 | 1.72 sec: 1.03x slower                                                     |
| dask                    | 267 ms                                                                   | 274 ms: 1.03x slower                                                       |
| telco                   | 3.93 ms                                                                  | 4.03 ms: 1.03x slower                                                      |
| regex_compile           | 89.7 ms                                                                  | 92.2 ms: 1.03x slower                                                      |
| thrift                  | 487 us                                                                   | 500 us: 1.03x slower                                                       |
| deepcopy_reduce         | 2.06 us                                                                  | 2.12 us: 1.03x slower                                                      |
| html5lib                | 38.5 ms                                                                  | 39.6 ms: 1.03x slower                                                      |
| dulwich_log             | 43.4 ms                                                                  | 44.9 ms: 1.03x slower                                                      |
| unpickle_pure_python    | 150 us                                                                   | 155 us: 1.04x slower                                                       |
| asyncio_tcp             | 674 ms                                                                   | 699 ms: 1.04x slower                                                       |
| chameleon               | 5.15 ms                                                                  | 5.35 ms: 1.04x slower                                                      |
| nqueens                 | 65.1 ms                                                                  | 67.6 ms: 1.04x slower                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 51.1 ms: 1.06x slower                                                      |
| deepcopy                | 240 us                                                                   | 254 us: 1.06x slower                                                       |
| json_loads              | 13.5 us                                                                  | 14.3 us: 1.06x slower                                                      |
| regex_dna               | 115 ms                                                                   | 123 ms: 1.07x slower                                                       |
| regex_v8                | 13.5 ms                                                                  | 14.7 ms: 1.09x slower                                                      |
| comprehensions          | 15.4 us                                                                  | 17.4 us: 1.13x slower                                                      |
| sqlglot_transpile       | 1.13 ms                                                                  | 1.35 ms: 1.19x slower                                                      |
| sqlglot_parse           | 929 us                                                                   | 1.14 ms: 1.23x slower                                                      |
| coverage                | 55.3 ms                                                                  | 98.8 ms: 1.79x slower                                                      |
| Geometric mean          | (ref)                                                                    | 1.01x slower                                                               |

Benchmark hidden because not significant (20): pathlib, create_gc_cycles, json, genshi_text, python_startup, xml_etree_iterparse, python_startup_no_site, scimark_fft, pylint, pyflate, bench_mp_pool, deltablue, async_tree_io, pidigits, sympy_integrate, aiohttp, deepcopy_memo, django_template, float, mypy2
Ignored benchmarks (1) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging
