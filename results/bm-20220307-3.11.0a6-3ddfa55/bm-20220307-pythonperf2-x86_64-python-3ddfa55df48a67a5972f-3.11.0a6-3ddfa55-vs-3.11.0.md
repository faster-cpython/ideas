
# Results vs. 3.11.0

- fork: python
- ref: 3ddfa55df48a67a5972f
- machine: linux-x86_64
- commit hash: 3ddfa55
- commit date: 2022-03-07
- overall geometric mean: 1.07x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 289 ms                                                                    | 300 ms: 1.04x slower                                                        |
| chameleon      | 7.50 ms                                                                   | 8.43 ms: 1.12x slower                                                       |
| docutils       | 2.86 sec                                                                  | 2.98 sec: 1.04x slower                                                      |
| html5lib       | 70.2 ms                                                                   | 75.6 ms: 1.08x slower                                                       |
| tornado_http   | 125 ms                                                                    | 130 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.06x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 252 ms                                                                    | 253 ms: 1.01x slower                                                        |
| float          | 75.7 ms                                                                   | 79.1 ms: 1.04x slower                                                       |
| nbody          | 92.1 ms                                                                   | 98.0 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                                     | 1.04x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                    | 161 ms: 1.04x slower                                                        |
| regex_effbot   | 3.31 ms                                                                   | 3.49 ms: 1.06x slower                                                       |
| regex_v8       | 24.4 ms                                                                   | 26.4 ms: 1.08x slower                                                       |
| regex_dna      | 225 ms                                                                    | 257 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.08x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                   | 23.9 us: 1.19x faster                                                       |
| xml_etree_parse      | 161 ms                                                                    | 154 ms: 1.04x faster                                                        |
| xml_etree_iterparse  | 106 ms                                                                    | 104 ms: 1.01x faster                                                        |
| pickle               | 9.92 us                                                                   | 9.96 us: 1.00x slower                                                       |
| json_dumps           | 13.4 ms                                                                   | 13.6 ms: 1.02x slower                                                       |
| unpickle_list        | 4.52 us                                                                   | 4.68 us: 1.03x slower                                                       |
| unpickle             | 13.0 us                                                                   | 13.5 us: 1.04x slower                                                       |
| pickle_dict          | 31.1 us                                                                   | 32.2 us: 1.04x slower                                                       |
| xml_etree_generate   | 79.1 ms                                                                   | 83.5 ms: 1.06x slower                                                       |
| xml_etree_process    | 55.8 ms                                                                   | 59.4 ms: 1.06x slower                                                       |
| pickle_pure_python   | 319 us                                                                    | 352 us: 1.10x slower                                                        |
| pickle_list          | 3.78 us                                                                   | 4.28 us: 1.13x slower                                                       |
| unpickle_pure_python | 238 us                                                                    | 273 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                                     | 1.03x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                   | 10.4 ms: 1.03x faster                                                       |
| python_startup_no_site | 7.73 ms                                                                   | 7.55 ms: 1.02x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.03x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 26.3 ms                                                                   | 26.5 ms: 1.01x slower                                                       |
| genshi_xml      | 57.8 ms                                                                   | 60.7 ms: 1.05x slower                                                       |
| mako            | 10.9 ms                                                                   | 11.4 ms: 1.05x slower                                                       |
| django_template | 39.6 ms                                                                   | 43.8 ms: 1.11x slower                                                       |
| Geometric mean  | (ref)                                                                     | 1.05x slower                                                                |

All benchmarks:
===============

| Benchmark               | bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20220307-pythonperf2-x86_64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads              | 28.4 us                                                                   | 23.9 us: 1.19x faster                                                       |
| json                    | 5.59 ms                                                                   | 5.04 ms: 1.11x faster                                                       |
| gc_traversal            | 4.22 ms                                                                   | 4.03 ms: 1.05x faster                                                       |
| xml_etree_parse         | 161 ms                                                                    | 154 ms: 1.04x faster                                                        |
| python_startup          | 10.7 ms                                                                   | 10.4 ms: 1.03x faster                                                       |
| python_startup_no_site  | 7.73 ms                                                                   | 7.55 ms: 1.02x faster                                                       |
| coverage                | 86.0 ms                                                                   | 84.1 ms: 1.02x faster                                                       |
| generators              | 56.0 ms                                                                   | 54.8 ms: 1.02x faster                                                       |
| xml_etree_iterparse     | 106 ms                                                                    | 104 ms: 1.01x faster                                                        |
| logging_format          | 7.84 us                                                                   | 7.75 us: 1.01x faster                                                       |
| pickle                  | 9.92 us                                                                   | 9.96 us: 1.00x slower                                                       |
| pidigits                | 252 ms                                                                    | 253 ms: 1.01x slower                                                        |
| async_generators        | 318 ms                                                                    | 320 ms: 1.01x slower                                                        |
| pathlib                 | 19.2 ms                                                                   | 19.3 ms: 1.01x slower                                                       |
| asyncio_tcp             | 752 ms                                                                    | 757 ms: 1.01x slower                                                        |
| genshi_text             | 26.3 ms                                                                   | 26.5 ms: 1.01x slower                                                       |
| sympy_sum               | 182 ms                                                                    | 184 ms: 1.01x slower                                                        |
| async_tree_cpu_io_mixed | 754 ms                                                                    | 763 ms: 1.01x slower                                                        |
| chaos                   | 76.2 ms                                                                   | 77.5 ms: 1.02x slower                                                       |
| async_tree_memoization  | 639 ms                                                                    | 651 ms: 1.02x slower                                                        |
| logging_simple          | 6.95 us                                                                   | 7.08 us: 1.02x slower                                                       |
| json_dumps              | 13.4 ms                                                                   | 13.6 ms: 1.02x slower                                                       |
| sqlite_synth            | 2.49 us                                                                   | 2.54 us: 1.02x slower                                                       |
| coroutines              | 29.5 ms                                                                   | 30.1 ms: 1.02x slower                                                       |
| meteor_contest          | 129 ms                                                                    | 133 ms: 1.03x slower                                                        |
| sympy_integrate         | 25.3 ms                                                                   | 25.9 ms: 1.03x slower                                                       |
| telco                   | 6.70 ms                                                                   | 6.90 ms: 1.03x slower                                                       |
| sympy_str               | 333 ms                                                                    | 343 ms: 1.03x slower                                                        |
| unpickle_list           | 4.52 us                                                                   | 4.68 us: 1.03x slower                                                       |
| unpickle                | 13.0 us                                                                   | 13.5 us: 1.04x slower                                                       |
| 2to3                    | 289 ms                                                                    | 300 ms: 1.04x slower                                                        |
| pickle_dict             | 31.1 us                                                                   | 32.2 us: 1.04x slower                                                       |
| tornado_http            | 125 ms                                                                    | 130 ms: 1.04x slower                                                        |
| docutils                | 2.86 sec                                                                  | 2.98 sec: 1.04x slower                                                      |
| regex_compile           | 154 ms                                                                    | 161 ms: 1.04x slower                                                        |
| float                   | 75.7 ms                                                                   | 79.1 ms: 1.04x slower                                                       |
| aiohttp                 | 959 us                                                                    | 1.00 ms: 1.05x slower                                                       |
| flaskblogging           | 3.81 ms                                                                   | 3.99 ms: 1.05x slower                                                       |
| sympy_expand            | 547 ms                                                                    | 573 ms: 1.05x slower                                                        |
| genshi_xml              | 57.8 ms                                                                   | 60.7 ms: 1.05x slower                                                       |
| mako                    | 10.9 ms                                                                   | 11.4 ms: 1.05x slower                                                       |
| thrift                  | 942 us                                                                    | 991 us: 1.05x slower                                                        |
| bench_thread_pool       | 990 us                                                                    | 1.04 ms: 1.05x slower                                                       |
| sqlalchemy_declarative  | 156 ms                                                                    | 164 ms: 1.05x slower                                                        |
| regex_effbot            | 3.31 ms                                                                   | 3.49 ms: 1.06x slower                                                       |
| xml_etree_generate      | 79.1 ms                                                                   | 83.5 ms: 1.06x slower                                                       |
| bench_mp_pool           | 4.54 ms                                                                   | 4.80 ms: 1.06x slower                                                       |
| dask                    | 418 ms                                                                    | 442 ms: 1.06x slower                                                        |
| sqlalchemy_imperative   | 19.8 ms                                                                   | 21.0 ms: 1.06x slower                                                       |
| gunicorn                | 936 us                                                                    | 994 us: 1.06x slower                                                        |
| xml_etree_process       | 55.8 ms                                                                   | 59.4 ms: 1.06x slower                                                       |
| nbody                   | 92.1 ms                                                                   | 98.0 ms: 1.06x slower                                                       |
| scimark_lu              | 114 ms                                                                    | 122 ms: 1.07x slower                                                        |
| dulwich_log             | 69.1 ms                                                                   | 73.8 ms: 1.07x slower                                                       |
| mdp                     | 2.73 sec                                                                  | 2.91 sec: 1.07x slower                                                      |
| sqlglot_normalize       | 122 ms                                                                    | 131 ms: 1.07x slower                                                        |
| deepcopy                | 384 us                                                                    | 413 us: 1.08x slower                                                        |
| html5lib                | 70.2 ms                                                                   | 75.6 ms: 1.08x slower                                                       |
| regex_v8                | 24.4 ms                                                                   | 26.4 ms: 1.08x slower                                                       |
| sqlglot_optimize        | 58.6 ms                                                                   | 63.7 ms: 1.09x slower                                                       |
| pycparser               | 1.30 sec                                                                  | 1.43 sec: 1.10x slower                                                      |
| scimark_monte_carlo     | 67.8 ms                                                                   | 74.4 ms: 1.10x slower                                                       |
| deepcopy_reduce         | 3.39 us                                                                   | 3.73 us: 1.10x slower                                                       |
| crypto_pyaes            | 85.0 ms                                                                   | 93.5 ms: 1.10x slower                                                       |
| pickle_pure_python      | 319 us                                                                    | 352 us: 1.10x slower                                                        |
| scimark_fft             | 276 ms                                                                    | 305 ms: 1.10x slower                                                        |
| hexiom                  | 7.00 ms                                                                   | 7.74 ms: 1.10x slower                                                       |
| django_template         | 39.6 ms                                                                   | 43.8 ms: 1.11x slower                                                       |
| scimark_sor             | 109 ms                                                                    | 121 ms: 1.11x slower                                                        |
| pprint_pformat          | 1.60 sec                                                                  | 1.77 sec: 1.11x slower                                                      |
| pprint_safe_repr        | 768 ms                                                                    | 853 ms: 1.11x slower                                                        |
| scimark_sparse_mat_mult | 4.06 ms                                                                   | 4.53 ms: 1.12x slower                                                       |
| logging_silent          | 103 ns                                                                    | 115 ns: 1.12x slower                                                        |
| chameleon               | 7.50 ms                                                                   | 8.43 ms: 1.12x slower                                                       |
| go                      | 158 ms                                                                    | 178 ms: 1.12x slower                                                        |
| deltablue               | 3.99 ms                                                                   | 4.49 ms: 1.12x slower                                                       |
| deepcopy_memo           | 37.0 us                                                                   | 41.7 us: 1.13x slower                                                       |
| pyflate                 | 438 ms                                                                    | 494 ms: 1.13x slower                                                        |
| raytrace                | 303 ms                                                                    | 343 ms: 1.13x slower                                                        |
| pickle_list             | 3.78 us                                                                   | 4.28 us: 1.13x slower                                                       |
| richards                | 49.1 ms                                                                   | 55.9 ms: 1.14x slower                                                       |
| regex_dna               | 225 ms                                                                    | 257 ms: 1.14x slower                                                        |
| unpickle_pure_python    | 238 us                                                                    | 273 us: 1.15x slower                                                        |
| spectral_norm           | 95.1 ms                                                                   | 111 ms: 1.16x slower                                                        |
| comprehensions          | 24.7 us                                                                   | 29.6 us: 1.20x slower                                                       |
| sqlglot_transpile       | 1.88 ms                                                                   | 2.50 ms: 1.33x slower                                                       |
| sqlglot_parse           | 1.53 ms                                                                   | 2.13 ms: 1.39x slower                                                       |
| unpack_sequence         | 45.9 ns                                                                   | 152 ns: 3.31x slower                                                        |
| Geometric mean          | (ref)                                                                     | 1.07x slower                                                                |

Benchmark hidden because not significant (5): create_gc_cycles, nqueens, async_tree_none, async_tree_io, fannkuch
Ignored benchmarks (2) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: mypy2, pylint
