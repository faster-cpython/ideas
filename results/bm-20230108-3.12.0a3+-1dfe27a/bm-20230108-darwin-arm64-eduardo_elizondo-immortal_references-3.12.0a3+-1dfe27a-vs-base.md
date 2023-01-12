
# Results vs. base

- fork: eduardo_elizondo
- ref: immortal_references
- machine: darwin-arm64
- commit hash: 1dfe27a
- commit date: 2023-01-08
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 183 ms                                                                 | 178 ms: 1.02x faster                                                            |
| chameleon      | 4.62 ms                                                                | 4.51 ms: 1.02x faster                                                           |
| docutils       | 1.44 sec                                                               | 1.45 sec: 1.00x slower                                                          |
| html5lib       | 34.9 ms                                                                | 33.6 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 51.6 ms                                                                | 52.0 ms: 1.01x slower                                                           |
| nbody          | 63.7 ms                                                                | 66.3 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 74.4 ms                                                                | 69.8 ms: 1.07x faster                                                           |
| regex_effbot   | 2.61 ms                                                                | 2.63 ms: 1.01x slower                                                           |
| regex_v8       | 16.1 ms                                                                | 16.1 ms: 1.00x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 6.08 ms                                                                | 5.95 ms: 1.02x faster                                                           |
| json_loads           | 16.2 us                                                                | 16.3 us: 1.01x slower                                                           |
| pickle               | 7.52 us                                                                | 7.69 us: 1.02x slower                                                           |
| pickle_dict          | 17.9 us                                                                | 18.1 us: 1.01x slower                                                           |
| pickle_pure_python   | 194 us                                                                 | 187 us: 1.04x faster                                                            |
| unpickle             | 9.66 us                                                                | 10.2 us: 1.05x slower                                                           |
| unpickle_list        | 2.71 us                                                                | 2.66 us: 1.02x faster                                                           |
| unpickle_pure_python | 142 us                                                                 | 143 us: 1.01x slower                                                            |
| xml_etree_parse      | 93.1 ms                                                                | 94.7 ms: 1.02x slower                                                           |
| xml_etree_iterparse  | 66.5 ms                                                                | 66.3 ms: 1.00x faster                                                           |
| xml_etree_generate   | 48.1 ms                                                                | 49.3 ms: 1.03x slower                                                           |
| xml_etree_process    | 34.9 ms                                                                | 35.0 ms: 1.00x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 9.30 ms                                                                | 9.33 ms: 1.00x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                                | 20.9 ms: 1.04x faster                                                           |
| genshi_text     | 15.2 ms                                                                | 14.4 ms: 1.05x faster                                                           |
| genshi_xml      | 28.3 ms                                                                | 28.5 ms: 1.01x slower                                                           |
| mako            | 8.08 ms                                                                | 8.51 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3+-e47b139 | bm-20230108-darwin-arm64-eduardo_elizondo-immortal_references-3.12.0a3+-1dfe27a |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3                    | 183 ms                                                                 | 178 ms: 1.02x faster                                                            |
| async_generators        | 202 ms                                                                 | 197 ms: 1.02x faster                                                            |
| async_tree_none         | 286 ms                                                                 | 276 ms: 1.04x faster                                                            |
| async_tree_cpu_io_mixed | 538 ms                                                                 | 530 ms: 1.02x faster                                                            |
| async_tree_io           | 742 ms                                                                 | 720 ms: 1.03x faster                                                            |
| async_tree_memoization  | 328 ms                                                                 | 317 ms: 1.03x faster                                                            |
| chameleon               | 4.62 ms                                                                | 4.51 ms: 1.02x faster                                                           |
| chaos                   | 50.2 ms                                                                | 46.1 ms: 1.09x faster                                                           |
| bench_thread_pool       | 448 us                                                                 | 443 us: 1.01x faster                                                            |
| coroutines              | 18.8 ms                                                                | 16.8 ms: 1.12x faster                                                           |
| coverage                | 57.1 ms                                                                | 56.2 ms: 1.02x faster                                                           |
| crypto_pyaes            | 52.9 ms                                                                | 52.0 ms: 1.02x faster                                                           |
| dask                    | 322 ms                                                                 | 315 ms: 1.02x faster                                                            |
| deepcopy                | 222 us                                                                 | 215 us: 1.03x faster                                                            |
| deepcopy_reduce         | 1.92 us                                                                | 1.85 us: 1.04x faster                                                           |
| deepcopy_memo           | 26.1 us                                                                | 25.6 us: 1.02x faster                                                           |
| deltablue               | 2.65 ms                                                                | 2.56 ms: 1.04x faster                                                           |
| django_template         | 21.7 ms                                                                | 20.9 ms: 1.04x faster                                                           |
| docutils                | 1.44 sec                                                               | 1.45 sec: 1.00x slower                                                          |
| dulwich_log             | 28.7 ms                                                                | 27.9 ms: 1.03x faster                                                           |
| fannkuch                | 254 ms                                                                 | 232 ms: 1.09x faster                                                            |
| float                   | 51.6 ms                                                                | 52.0 ms: 1.01x slower                                                           |
| create_gc_cycles        | 686 us                                                                 | 677 us: 1.01x faster                                                            |
| gc_traversal            | 2.41 ms                                                                | 2.40 ms: 1.00x faster                                                           |
| generators              | 33.9 ms                                                                | 33.7 ms: 1.01x faster                                                           |
| genshi_text             | 15.2 ms                                                                | 14.4 ms: 1.05x faster                                                           |
| genshi_xml              | 28.3 ms                                                                | 28.5 ms: 1.01x slower                                                           |
| go                      | 109 ms                                                                 | 103 ms: 1.06x faster                                                            |
| hexiom                  | 4.96 ms                                                                | 4.44 ms: 1.12x faster                                                           |
| html5lib                | 34.9 ms                                                                | 33.6 ms: 1.04x faster                                                           |
| json_dumps              | 6.08 ms                                                                | 5.95 ms: 1.02x faster                                                           |
| json_loads              | 16.2 us                                                                | 16.3 us: 1.01x slower                                                           |
| logging_format          | 3.75 us                                                                | 3.59 us: 1.05x faster                                                           |
| logging_silent          | 66.7 ns                                                                | 63.7 ns: 1.05x faster                                                           |
| logging_simple          | 3.45 us                                                                | 3.30 us: 1.04x faster                                                           |
| mako                    | 8.08 ms                                                                | 8.51 ms: 1.05x slower                                                           |
| mdp                     | 1.51 sec                                                               | 1.50 sec: 1.01x faster                                                          |
| meteor_contest          | 74.8 ms                                                                | 74.3 ms: 1.01x faster                                                           |
| nbody                   | 63.7 ms                                                                | 66.3 ms: 1.04x slower                                                           |
| nqueens                 | 60.5 ms                                                                | 55.9 ms: 1.08x faster                                                           |
| pickle                  | 7.52 us                                                                | 7.69 us: 1.02x slower                                                           |
| pickle_dict             | 17.9 us                                                                | 18.1 us: 1.01x slower                                                           |
| pickle_pure_python      | 194 us                                                                 | 187 us: 1.04x faster                                                            |
| pprint_safe_repr        | 464 ms                                                                 | 448 ms: 1.03x faster                                                            |
| pprint_pformat          | 941 ms                                                                 | 910 ms: 1.03x faster                                                            |
| pycparser               | 680 ms                                                                 | 667 ms: 1.02x faster                                                            |
| pyflate                 | 321 ms                                                                 | 319 ms: 1.00x faster                                                            |
| python_startup          | 9.30 ms                                                                | 9.33 ms: 1.00x slower                                                           |
| raytrace                | 224 ms                                                                 | 222 ms: 1.01x faster                                                            |
| regex_compile           | 74.4 ms                                                                | 69.8 ms: 1.07x faster                                                           |
| regex_effbot            | 2.61 ms                                                                | 2.63 ms: 1.01x slower                                                           |
| regex_v8                | 16.1 ms                                                                | 16.1 ms: 1.00x slower                                                           |
| richards                | 30.5 ms                                                                | 28.9 ms: 1.06x faster                                                           |
| scimark_fft             | 195 ms                                                                 | 199 ms: 1.02x slower                                                            |
| scimark_lu              | 72.7 ms                                                                | 75.7 ms: 1.04x slower                                                           |
| scimark_monte_carlo     | 50.7 ms                                                                | 46.2 ms: 1.10x faster                                                           |
| scimark_sor             | 78.4 ms                                                                | 84.0 ms: 1.07x slower                                                           |
| scimark_sparse_mat_mult | 2.82 ms                                                                | 2.90 ms: 1.03x slower                                                           |
| spectral_norm           | 73.7 ms                                                                | 73.0 ms: 1.01x faster                                                           |
| sqlglot_parse           | 1.03 ms                                                                | 991 us: 1.04x faster                                                            |
| sqlglot_transpile       | 1.19 ms                                                                | 1.15 ms: 1.03x faster                                                           |
| sqlglot_optimize        | 31.2 ms                                                                | 31.1 ms: 1.00x faster                                                           |
| sqlglot_normalize       | 171 ms                                                                 | 170 ms: 1.01x faster                                                            |
| sqlite_synth            | 1.39 us                                                                | 1.40 us: 1.00x slower                                                           |
| sympy_expand            | 241 ms                                                                 | 232 ms: 1.04x faster                                                            |
| sympy_integrate         | 11.4 ms                                                                | 11.2 ms: 1.02x faster                                                           |
| sympy_sum               | 85.9 ms                                                                | 83.2 ms: 1.03x faster                                                           |
| sympy_str               | 151 ms                                                                 | 145 ms: 1.05x faster                                                            |
| thrift                  | 439 us                                                                 | 431 us: 1.02x faster                                                            |
| unpack_sequence         | 33.5 ns                                                                | 28.8 ns: 1.17x faster                                                           |
| unpickle                | 9.66 us                                                                | 10.2 us: 1.05x slower                                                           |
| unpickle_list           | 2.71 us                                                                | 2.66 us: 1.02x faster                                                           |
| unpickle_pure_python    | 142 us                                                                 | 143 us: 1.01x slower                                                            |
| xml_etree_parse         | 93.1 ms                                                                | 94.7 ms: 1.02x slower                                                           |
| xml_etree_iterparse     | 66.5 ms                                                                | 66.3 ms: 1.00x faster                                                           |
| xml_etree_generate      | 48.1 ms                                                                | 49.3 ms: 1.03x slower                                                           |
| xml_etree_process       | 34.9 ms                                                                | 35.0 ms: 1.00x slower                                                           |
| Geometric mean          | (ref)                                                                  | 1.02x faster                                                                    |

Benchmark hidden because not significant (10): asyncio_tcp, bench_mp_pool, json, mypy, pathlib, pickle_list, pidigits, python_startup_no_site, regex_dna, telco
