
# Results vs. 3.11.0

- fork: python
- ref: 5a7e1e0a92622c605ab2
- machine: windows-amd64
- commit hash: 5a7e1e0
- commit date: 2022-07-11
- overall geometric mean: 1.01x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 204 ms                                                                   | 206 ms: 1.01x slower                                                       |
| docutils       | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                     |
| html5lib       | 38.5 ms                                                                  | 38.9 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                               |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.9 ms                                                                  | 68.7 ms: 1.03x faster                                                      |
| pidigits       | 147 ms                                                                   | 146 ms: 1.00x faster                                                       |
| float          | 53.3 ms                                                                  | 53.9 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 115 ms                                                                   | 114 ms: 1.01x faster                                                       |
| regex_v8       | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                      |
| regex_compile  | 89.7 ms                                                                  | 90.8 ms: 1.01x slower                                                      |
| regex_effbot   | 1.63 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_list          | 2.70 us                                                                  | 2.65 us: 1.02x faster                                                      |
| pickle_dict          | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                      |
| json_dumps           | 7.71 ms                                                                  | 7.78 ms: 1.01x slower                                                      |
| xml_etree_iterparse  | 61.8 ms                                                                  | 62.7 ms: 1.01x slower                                                      |
| unpickle_pure_python | 150 us                                                                   | 152 us: 1.02x slower                                                       |
| xml_etree_generate   | 52.3 ms                                                                  | 53.4 ms: 1.02x slower                                                      |
| xml_etree_process    | 36.6 ms                                                                  | 37.8 ms: 1.03x slower                                                      |
| xml_etree_parse      | 92.1 ms                                                                  | 95.1 ms: 1.03x slower                                                      |
| unpickle             | 8.01 us                                                                  | 8.32 us: 1.04x slower                                                      |
| json_loads           | 13.5 us                                                                  | 14.1 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                               |

Benchmark hidden because not significant (3): unpickle_list, pickle_pure_python, pickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 38.0 ms                                                                  | 38.6 ms: 1.01x slower                                                      |
| genshi_text     | 17.3 ms                                                                  | 17.6 ms: 1.02x slower                                                      |
| django_template | 23.9 ms                                                                  | 25.0 ms: 1.05x slower                                                      |
| Geometric mean  | (ref)                                                                    | 1.02x slower                                                               |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220711-pythonperf1-amd64-python-5a7e1e0a92622c605ab2-3.11.0b4-5a7e1e0 |
|-------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| scimark_monte_carlo     | 45.8 ms                                                                  | 44.3 ms: 1.03x faster                                                      |
| nbody                   | 70.9 ms                                                                  | 68.7 ms: 1.03x faster                                                      |
| sympy_sum               | 98.9 ms                                                                  | 95.8 ms: 1.03x faster                                                      |
| sympy_expand            | 298 ms                                                                   | 291 ms: 1.02x faster                                                       |
| coverage                | 55.3 ms                                                                  | 54.1 ms: 1.02x faster                                                      |
| pickle_list             | 2.70 us                                                                  | 2.65 us: 1.02x faster                                                      |
| fannkuch                | 255 ms                                                                   | 251 ms: 1.02x faster                                                       |
| async_generators        | 180 ms                                                                   | 178 ms: 1.02x faster                                                       |
| pickle_dict             | 18.6 us                                                                  | 18.4 us: 1.01x faster                                                      |
| richards                | 32.1 ms                                                                  | 31.7 ms: 1.01x faster                                                      |
| sympy_str               | 184 ms                                                                   | 182 ms: 1.01x faster                                                       |
| docutils                | 1.59 sec                                                                 | 1.58 sec: 1.01x faster                                                     |
| raytrace                | 206 ms                                                                   | 204 ms: 1.01x faster                                                       |
| deltablue               | 2.68 ms                                                                  | 2.66 ms: 1.01x faster                                                      |
| regex_dna               | 115 ms                                                                   | 114 ms: 1.01x faster                                                       |
| regex_v8                | 13.5 ms                                                                  | 13.4 ms: 1.01x faster                                                      |
| sqlalchemy_imperative   | 10.4 ms                                                                  | 10.4 ms: 1.00x faster                                                      |
| mdp                     | 1.67 sec                                                                 | 1.67 sec: 1.00x faster                                                     |
| pidigits                | 147 ms                                                                   | 146 ms: 1.00x faster                                                       |
| meteor_contest          | 74.4 ms                                                                  | 74.8 ms: 1.01x slower                                                      |
| pprint_safe_repr        | 512 ms                                                                   | 515 ms: 1.01x slower                                                       |
| gc_traversal            | 1.40 ms                                                                  | 1.41 ms: 1.01x slower                                                      |
| sqlglot_parse           | 929 us                                                                   | 936 us: 1.01x slower                                                       |
| sqlglot_optimize        | 34.5 ms                                                                  | 34.8 ms: 1.01x slower                                                      |
| json_dumps              | 7.71 ms                                                                  | 7.78 ms: 1.01x slower                                                      |
| 2to3                    | 204 ms                                                                   | 206 ms: 1.01x slower                                                       |
| logging_format          | 7.13 us                                                                  | 7.19 us: 1.01x slower                                                      |
| html5lib                | 38.5 ms                                                                  | 38.9 ms: 1.01x slower                                                      |
| scimark_sor             | 77.7 ms                                                                  | 78.5 ms: 1.01x slower                                                      |
| generators              | 33.5 ms                                                                  | 33.9 ms: 1.01x slower                                                      |
| logging_simple          | 6.60 us                                                                  | 6.68 us: 1.01x slower                                                      |
| float                   | 53.3 ms                                                                  | 53.9 ms: 1.01x slower                                                      |
| async_tree_none         | 313 ms                                                                   | 317 ms: 1.01x slower                                                       |
| pyflate                 | 302 ms                                                                   | 306 ms: 1.01x slower                                                       |
| async_tree_io           | 744 ms                                                                   | 753 ms: 1.01x slower                                                       |
| regex_compile           | 89.7 ms                                                                  | 90.8 ms: 1.01x slower                                                      |
| sqlite_synth            | 1.67 us                                                                  | 1.70 us: 1.01x slower                                                      |
| genshi_xml              | 38.0 ms                                                                  | 38.6 ms: 1.01x slower                                                      |
| xml_etree_iterparse     | 61.8 ms                                                                  | 62.7 ms: 1.01x slower                                                      |
| unpickle_pure_python    | 150 us                                                                   | 152 us: 1.02x slower                                                       |
| sqlglot_normalize       | 189 ms                                                                   | 192 ms: 1.02x slower                                                       |
| pprint_pformat          | 1.05 sec                                                                 | 1.07 sec: 1.02x slower                                                     |
| dulwich_log             | 43.4 ms                                                                  | 44.2 ms: 1.02x slower                                                      |
| genshi_text             | 17.3 ms                                                                  | 17.6 ms: 1.02x slower                                                      |
| logging_silent          | 71.0 ns                                                                  | 72.4 ns: 1.02x slower                                                      |
| scimark_fft             | 183 ms                                                                   | 186 ms: 1.02x slower                                                       |
| scimark_sparse_mat_mult | 2.63 ms                                                                  | 2.68 ms: 1.02x slower                                                      |
| sqlalchemy_declarative  | 83.1 ms                                                                  | 84.7 ms: 1.02x slower                                                      |
| go                      | 97.5 ms                                                                  | 99.5 ms: 1.02x slower                                                      |
| xml_etree_generate      | 52.3 ms                                                                  | 53.4 ms: 1.02x slower                                                      |
| telco                   | 3.93 ms                                                                  | 4.02 ms: 1.02x slower                                                      |
| comprehensions          | 15.4 us                                                                  | 15.7 us: 1.02x slower                                                      |
| deepcopy                | 240 us                                                                   | 246 us: 1.02x slower                                                       |
| spectral_norm           | 71.8 ms                                                                  | 73.7 ms: 1.03x slower                                                      |
| pycparser               | 686 ms                                                                   | 706 ms: 1.03x slower                                                       |
| chaos                   | 47.3 ms                                                                  | 48.7 ms: 1.03x slower                                                      |
| xml_etree_process       | 36.6 ms                                                                  | 37.8 ms: 1.03x slower                                                      |
| xml_etree_parse         | 92.1 ms                                                                  | 95.1 ms: 1.03x slower                                                      |
| hexiom                  | 4.46 ms                                                                  | 4.61 ms: 1.03x slower                                                      |
| unpickle                | 8.01 us                                                                  | 8.32 us: 1.04x slower                                                      |
| nqueens                 | 65.1 ms                                                                  | 67.6 ms: 1.04x slower                                                      |
| json_loads              | 13.5 us                                                                  | 14.1 us: 1.04x slower                                                      |
| regex_effbot            | 1.63 ms                                                                  | 1.70 ms: 1.04x slower                                                      |
| deepcopy_reduce         | 2.06 us                                                                  | 2.14 us: 1.04x slower                                                      |
| django_template         | 23.9 ms                                                                  | 25.0 ms: 1.05x slower                                                      |
| crypto_pyaes            | 48.3 ms                                                                  | 50.6 ms: 1.05x slower                                                      |
| unpack_sequence         | 43.1 ns                                                                  | 45.4 ns: 1.05x slower                                                      |
| thrift                  | 487 us                                                                   | 518 us: 1.06x slower                                                       |
| Geometric mean          | (ref)                                                                    | 1.01x slower                                                               |

Benchmark hidden because not significant (26): async_tree_cpu_io_mixed, pathlib, aiohttp, chameleon, create_gc_cycles, scimark_lu, unpickle_list, sqlglot_transpile, pylint, coroutines, python_startup, python_startup_no_site, deepcopy_memo, tornado_http, asyncio_tcp, pickle_pure_python, async_tree_memoization, pickle, flaskblogging, sympy_integrate, bench_thread_pool, bench_mp_pool, mako, mypy2, dask, json
