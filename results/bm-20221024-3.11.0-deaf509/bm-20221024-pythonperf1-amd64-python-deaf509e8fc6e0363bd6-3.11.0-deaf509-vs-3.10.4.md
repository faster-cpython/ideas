
# Results vs. 3.10.4

- fork: python
- ref: deaf509e8fc6e0363bd6
- machine: windows-amd64
- commit hash: deaf509
- commit date: 2022-10-24
- overall geometric mean: 1.11x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                   | 204 ms: 1.12x faster                                                     |
| chameleon      | 5.77 ms                                                                  | 5.15 ms: 1.12x faster                                                    |
| docutils       | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                   |
| html5lib       | 47.3 ms                                                                  | 38.5 ms: 1.23x faster                                                    |
| tornado_http   | 106 ms                                                                   | 91.8 ms: 1.16x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.16x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 59.5 ms                                                                  | 53.3 ms: 1.12x faster                                                    |
| nbody          | 71.5 ms                                                                  | 70.9 ms: 1.01x faster                                                    |
| pidigits       | 145 ms                                                                   | 147 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 103 ms                                                                   | 89.7 ms: 1.15x faster                                                    |
| regex_dna      | 131 ms                                                                   | 115 ms: 1.14x faster                                                     |
| regex_v8       | 15.1 ms                                                                  | 13.5 ms: 1.12x faster                                                    |
| regex_effbot   | 1.64 ms                                                                  | 1.63 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 264 us                                                                   | 203 us: 1.30x faster                                                     |
| unpickle_pure_python | 179 us                                                                   | 150 us: 1.20x faster                                                     |
| xml_etree_process    | 43.0 ms                                                                  | 36.6 ms: 1.18x faster                                                    |
| json_dumps           | 9.00 ms                                                                  | 7.71 ms: 1.17x faster                                                    |
| unpickle             | 8.88 us                                                                  | 8.01 us: 1.11x faster                                                    |
| json_loads           | 14.2 us                                                                  | 13.5 us: 1.05x faster                                                    |
| xml_etree_parse      | 95.6 ms                                                                  | 92.1 ms: 1.04x faster                                                    |
| pickle               | 6.67 us                                                                  | 6.47 us: 1.03x faster                                                    |
| xml_etree_generate   | 53.8 ms                                                                  | 52.3 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 62.5 ms                                                                  | 61.8 ms: 1.01x faster                                                    |
| unpickle_list        | 2.71 us                                                                  | 2.80 us: 1.03x slower                                                    |
| pickle_list          | 2.57 us                                                                  | 2.70 us: 1.05x slower                                                    |
| pickle_dict          | 16.7 us                                                                  | 18.6 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                    |
| python_startup_no_site | 14.8 ms                                                                  | 15.4 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 29.2 ms                                                                  | 23.9 ms: 1.22x faster                                                    |
| mako            | 8.69 ms                                                                  | 7.20 ms: 1.21x faster                                                    |
| genshi_text     | 18.5 ms                                                                  | 17.3 ms: 1.07x faster                                                    |
| genshi_xml      | 38.8 ms                                                                  | 38.0 ms: 1.02x faster                                                    |
| Geometric mean  | (ref)                                                                    | 1.13x faster                                                             |

All benchmarks:
===============

| Benchmark               | bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deltablue               | 4.15 ms                                                                  | 2.68 ms: 1.55x faster                                                    |
| go                      | 143 ms                                                                   | 97.5 ms: 1.47x faster                                                    |
| async_tree_io           | 1.02 sec                                                                 | 744 ms: 1.38x faster                                                     |
| scimark_lu              | 83.9 ms                                                                  | 62.8 ms: 1.33x faster                                                    |
| scimark_sor             | 104 ms                                                                   | 77.7 ms: 1.33x faster                                                    |
| logging_silent          | 94.6 ns                                                                  | 71.0 ns: 1.33x faster                                                    |
| async_tree_none         | 414 ms                                                                   | 313 ms: 1.32x faster                                                     |
| sqlglot_parse           | 1.22 ms                                                                  | 929 us: 1.31x faster                                                     |
| sqlglot_transpile       | 1.47 ms                                                                  | 1.13 ms: 1.30x faster                                                    |
| thrift                  | 632 us                                                                   | 487 us: 1.30x faster                                                     |
| pickle_pure_python      | 264 us                                                                   | 203 us: 1.30x faster                                                     |
| raytrace                | 267 ms                                                                   | 206 ms: 1.30x faster                                                     |
| async_tree_memoization  | 485 ms                                                                   | 374 ms: 1.30x faster                                                     |
| pyflate                 | 388 ms                                                                   | 302 ms: 1.29x faster                                                     |
| richards                | 41.0 ms                                                                  | 32.1 ms: 1.28x faster                                                    |
| pycparser               | 873 ms                                                                   | 686 ms: 1.27x faster                                                     |
| crypto_pyaes            | 61.4 ms                                                                  | 48.3 ms: 1.27x faster                                                    |
| chaos                   | 58.4 ms                                                                  | 47.3 ms: 1.24x faster                                                    |
| html5lib                | 47.3 ms                                                                  | 38.5 ms: 1.23x faster                                                    |
| django_template         | 29.2 ms                                                                  | 23.9 ms: 1.22x faster                                                    |
| scimark_monte_carlo     | 56.0 ms                                                                  | 45.8 ms: 1.22x faster                                                    |
| hexiom                  | 5.45 ms                                                                  | 4.46 ms: 1.22x faster                                                    |
| mypy2                   | 337 ms                                                                   | 276 ms: 1.22x faster                                                     |
| mako                    | 8.69 ms                                                                  | 7.20 ms: 1.21x faster                                                    |
| unpickle_pure_python    | 179 us                                                                   | 150 us: 1.20x faster                                                     |
| async_generators        | 214 ms                                                                   | 180 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed | 604 ms                                                                   | 512 ms: 1.18x faster                                                     |
| xml_etree_process       | 43.0 ms                                                                  | 36.6 ms: 1.18x faster                                                    |
| pprint_pformat          | 1.23 sec                                                                 | 1.05 sec: 1.17x faster                                                   |
| json_dumps              | 9.00 ms                                                                  | 7.71 ms: 1.17x faster                                                    |
| dask                    | 310 ms                                                                   | 267 ms: 1.16x faster                                                     |
| sqlalchemy_declarative  | 96.4 ms                                                                  | 83.1 ms: 1.16x faster                                                    |
| pprint_safe_repr        | 593 ms                                                                   | 512 ms: 1.16x faster                                                     |
| tornado_http            | 106 ms                                                                   | 91.8 ms: 1.16x faster                                                    |
| regex_compile           | 103 ms                                                                   | 89.7 ms: 1.15x faster                                                    |
| docutils                | 1.83 sec                                                                 | 1.59 sec: 1.15x faster                                                   |
| create_gc_cycles        | 764 us                                                                   | 666 us: 1.15x faster                                                     |
| regex_dna               | 131 ms                                                                   | 115 ms: 1.14x faster                                                     |
| 2to3                    | 229 ms                                                                   | 204 ms: 1.12x faster                                                     |
| sqlglot_optimize        | 38.7 ms                                                                  | 34.5 ms: 1.12x faster                                                    |
| deepcopy_memo           | 28.4 us                                                                  | 25.3 us: 1.12x faster                                                    |
| aiohttp                 | 968 us                                                                   | 864 us: 1.12x faster                                                     |
| chameleon               | 5.77 ms                                                                  | 5.15 ms: 1.12x faster                                                    |
| regex_v8                | 15.1 ms                                                                  | 13.5 ms: 1.12x faster                                                    |
| float                   | 59.5 ms                                                                  | 53.3 ms: 1.12x faster                                                    |
| bench_thread_pool       | 953 us                                                                   | 856 us: 1.11x faster                                                     |
| unpickle                | 8.88 us                                                                  | 8.01 us: 1.11x faster                                                    |
| sqlite_synth            | 1.85 us                                                                  | 1.67 us: 1.10x faster                                                    |
| sqlalchemy_imperative   | 11.3 ms                                                                  | 10.4 ms: 1.08x faster                                                    |
| dulwich_log             | 47.0 ms                                                                  | 43.4 ms: 1.08x faster                                                    |
| genshi_text             | 18.5 ms                                                                  | 17.3 ms: 1.07x faster                                                    |
| sympy_integrate         | 14.7 ms                                                                  | 13.7 ms: 1.07x faster                                                    |
| deepcopy                | 256 us                                                                   | 240 us: 1.07x faster                                                     |
| sqlglot_normalize       | 201 ms                                                                   | 189 ms: 1.06x faster                                                     |
| deepcopy_reduce         | 2.18 us                                                                  | 2.06 us: 1.06x faster                                                    |
| pylint                  | 337 ms                                                                   | 319 ms: 1.06x faster                                                     |
| coroutines              | 15.6 ms                                                                  | 14.8 ms: 1.06x faster                                                    |
| json_loads              | 14.2 us                                                                  | 13.5 us: 1.05x faster                                                    |
| sympy_expand            | 313 ms                                                                   | 298 ms: 1.05x faster                                                     |
| python_startup          | 19.3 ms                                                                  | 18.4 ms: 1.05x faster                                                    |
| comprehensions          | 16.0 us                                                                  | 15.4 us: 1.04x faster                                                    |
| xml_etree_parse         | 95.6 ms                                                                  | 92.1 ms: 1.04x faster                                                    |
| spectral_norm           | 74.3 ms                                                                  | 71.8 ms: 1.03x faster                                                    |
| sympy_sum               | 102 ms                                                                   | 98.9 ms: 1.03x faster                                                    |
| pickle                  | 6.67 us                                                                  | 6.47 us: 1.03x faster                                                    |
| pathlib                 | 75.2 ms                                                                  | 72.9 ms: 1.03x faster                                                    |
| xml_etree_generate      | 53.8 ms                                                                  | 52.3 ms: 1.03x faster                                                    |
| sympy_str               | 189 ms                                                                   | 184 ms: 1.02x faster                                                     |
| scimark_fft             | 187 ms                                                                   | 183 ms: 1.02x faster                                                     |
| genshi_xml              | 38.8 ms                                                                  | 38.0 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult | 2.67 ms                                                                  | 2.63 ms: 1.02x faster                                                    |
| xml_etree_iterparse     | 62.5 ms                                                                  | 61.8 ms: 1.01x faster                                                    |
| nbody                   | 71.5 ms                                                                  | 70.9 ms: 1.01x faster                                                    |
| regex_effbot            | 1.64 ms                                                                  | 1.63 ms: 1.01x faster                                                    |
| flaskblogging           | 2.05 sec                                                                 | 2.04 sec: 1.00x faster                                                   |
| pidigits                | 145 ms                                                                   | 147 ms: 1.01x slower                                                     |
| fannkuch                | 252 ms                                                                   | 255 ms: 1.01x slower                                                     |
| unpickle_list           | 2.71 us                                                                  | 2.80 us: 1.03x slower                                                    |
| bench_mp_pool           | 59.2 ms                                                                  | 61.2 ms: 1.03x slower                                                    |
| python_startup_no_site  | 14.8 ms                                                                  | 15.4 ms: 1.03x slower                                                    |
| telco                   | 3.77 ms                                                                  | 3.93 ms: 1.04x slower                                                    |
| mdp                     | 1.60 sec                                                                 | 1.67 sec: 1.04x slower                                                   |
| pickle_list             | 2.57 us                                                                  | 2.70 us: 1.05x slower                                                    |
| gc_traversal            | 1.33 ms                                                                  | 1.40 ms: 1.05x slower                                                    |
| generators              | 31.4 ms                                                                  | 33.5 ms: 1.07x slower                                                    |
| logging_simple          | 6.12 us                                                                  | 6.60 us: 1.08x slower                                                    |
| logging_format          | 6.53 us                                                                  | 7.13 us: 1.09x slower                                                    |
| unpack_sequence         | 39.4 ns                                                                  | 43.1 ns: 1.09x slower                                                    |
| pickle_dict             | 16.7 us                                                                  | 18.6 us: 1.12x slower                                                    |
| coverage                | 37.5 ms                                                                  | 55.3 ms: 1.48x slower                                                    |
| Geometric mean          | (ref)                                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (4): meteor_contest, nqueens, json, asyncio_tcp
