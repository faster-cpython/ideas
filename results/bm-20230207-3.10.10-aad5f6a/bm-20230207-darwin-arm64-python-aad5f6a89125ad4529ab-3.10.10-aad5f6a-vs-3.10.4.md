
# Results vs. 3.10.4

- fork: python
- ref: aad5f6a89125ad4529ab
- machine: darwin-arm64
- commit hash: aad5f6a
- commit date: 2023-02-07
- overall geometric mean: 1.02x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 203 ms: 1.10x faster                                                 |
| chameleon      | 5.86 ms                                                | 5.78 ms: 1.01x faster                                                |
| docutils       | 1.76 sec                                               | 1.79 sec: 1.01x slower                                               |
| html5lib       | 44.0 ms                                                | 47.8 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                 |
| nbody          | 94.6 ms                                                | 94.1 ms: 1.01x faster                                                |
| float          | 72.1 ms                                                | 72.3 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                  | 1.00x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 96.9 ms: 1.01x slower                                                |
| regex_v8       | 17.7 ms                                                | 18.2 ms: 1.03x slower                                                |
| regex_effbot   | 2.45 ms                                                | 2.75 ms: 1.12x slower                                                |
| regex_dna      | 164 ms                                                 | 187 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|---------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle            | 10.0 us                                                | 9.86 us: 1.02x faster                                                |
| json_loads          | 17.0 us                                                | 16.9 us: 1.01x faster                                                |
| json_dumps          | 8.34 ms                                                | 8.29 ms: 1.01x faster                                                |
| pickle              | 7.50 us                                                | 7.54 us: 1.00x slower                                                |
| unpickle_list       | 2.66 us                                                | 2.68 us: 1.01x slower                                                |
| xml_etree_generate  | 54.5 ms                                                | 55.0 ms: 1.01x slower                                                |
| pickle_pure_python  | 284 us                                                 | 287 us: 1.01x slower                                                 |
| pickle_list         | 2.83 us                                                | 2.93 us: 1.04x slower                                                |
| pickle_dict         | 18.0 us                                                | 18.7 us: 1.04x slower                                                |
| xml_etree_iterparse | 69.0 ms                                                | 73.1 ms: 1.06x slower                                                |
| xml_etree_parse     | 100 ms                                                 | 107 ms: 1.07x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.7 ms: 1.33x slower                                                |
| python_startup_no_site | 7.00 ms                                                | 9.82 ms: 1.40x slower                                                |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 37.7 ms                                                | 37.3 ms: 1.01x faster                                                |
| mako            | 10.6 ms                                                | 10.5 ms: 1.01x faster                                                |
| django_template | 27.2 ms                                                | 27.2 ms: 1.00x faster                                                |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 203 ms: 1.10x faster                                                 |
| deltablue               | 5.37 ms                                                | 5.18 ms: 1.04x faster                                                |
| richards                | 51.4 ms                                                | 50.2 ms: 1.02x faster                                                |
| sqlite_synth            | 1.50 us                                                | 1.47 us: 1.02x faster                                                |
| unpickle                | 10.0 us                                                | 9.86 us: 1.02x faster                                                |
| chameleon               | 5.86 ms                                                | 5.78 ms: 1.01x faster                                                |
| json                    | 3.13 ms                                                | 3.08 ms: 1.01x faster                                                |
| sqlglot_normalize       | 198 ms                                                 | 196 ms: 1.01x faster                                                 |
| pprint_safe_repr        | 608 ms                                                 | 600 ms: 1.01x faster                                                 |
| logging_silent          | 119 ns                                                 | 118 ns: 1.01x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 37.3 ms: 1.01x faster                                                |
| json_loads              | 17.0 us                                                | 16.9 us: 1.01x faster                                                |
| pprint_pformat          | 1.24 sec                                               | 1.23 sec: 1.01x faster                                               |
| nqueens                 | 68.6 ms                                                | 68.1 ms: 1.01x faster                                                |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                 |
| mako                    | 10.6 ms                                                | 10.5 ms: 1.01x faster                                                |
| json_dumps              | 8.34 ms                                                | 8.29 ms: 1.01x faster                                                |
| nbody                   | 94.6 ms                                                | 94.1 ms: 1.01x faster                                                |
| fannkuch                | 318 ms                                                 | 317 ms: 1.00x faster                                                 |
| deepcopy_reduce         | 2.36 us                                                | 2.35 us: 1.00x faster                                                |
| django_template         | 27.2 ms                                                | 27.2 ms: 1.00x faster                                                |
| meteor_contest          | 77.7 ms                                                | 77.6 ms: 1.00x faster                                                |
| unpack_sequence         | 38.2 ns                                                | 38.3 ns: 1.00x slower                                                |
| crypto_pyaes            | 77.9 ms                                                | 78.0 ms: 1.00x slower                                                |
| sqlglot_parse           | 1.33 ms                                                | 1.33 ms: 1.00x slower                                                |
| coroutines              | 20.1 ms                                                | 20.2 ms: 1.00x slower                                                |
| logging_simple          | 4.61 us                                                | 4.62 us: 1.00x slower                                                |
| raytrace                | 329 ms                                                 | 330 ms: 1.00x slower                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.48 ms: 1.00x slower                                                |
| scimark_fft             | 231 ms                                                 | 232 ms: 1.00x slower                                                 |
| float                   | 72.1 ms                                                | 72.3 ms: 1.00x slower                                                |
| pickle                  | 7.50 us                                                | 7.54 us: 1.00x slower                                                |
| spectral_norm           | 95.8 ms                                                | 96.3 ms: 1.01x slower                                                |
| mdp                     | 1.66 sec                                               | 1.67 sec: 1.01x slower                                               |
| bench_thread_pool       | 531 us                                                 | 534 us: 1.01x slower                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 74.8 ms: 1.01x slower                                                |
| generators              | 32.5 ms                                                | 32.7 ms: 1.01x slower                                                |
| telco                   | 3.63 ms                                                | 3.65 ms: 1.01x slower                                                |
| regex_compile           | 96.2 ms                                                | 96.9 ms: 1.01x slower                                                |
| unpickle_list           | 2.66 us                                                | 2.68 us: 1.01x slower                                                |
| chaos                   | 66.5 ms                                                | 67.1 ms: 1.01x slower                                                |
| deepcopy                | 278 us                                                 | 280 us: 1.01x slower                                                 |
| xml_etree_generate      | 54.5 ms                                                | 55.0 ms: 1.01x slower                                                |
| sqlalchemy_imperative   | 9.01 ms                                                | 9.10 ms: 1.01x slower                                                |
| sympy_expand            | 275 ms                                                 | 278 ms: 1.01x slower                                                 |
| sympy_str               | 169 ms                                                 | 171 ms: 1.01x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 287 us: 1.01x slower                                                 |
| sympy_integrate         | 13.3 ms                                                | 13.4 ms: 1.01x slower                                                |
| logging_format          | 4.95 us                                                | 5.01 us: 1.01x slower                                                |
| docutils                | 1.76 sec                                               | 1.79 sec: 1.01x slower                                               |
| thrift                  | 577 us                                                 | 586 us: 1.02x slower                                                 |
| async_generators        | 231 ms                                                 | 234 ms: 1.02x slower                                                 |
| pylint                  | 302 ms                                                 | 307 ms: 1.02x slower                                                 |
| dulwich_log             | 36.4 ms                                                | 37.2 ms: 1.02x slower                                                |
| coverage                | 40.8 ms                                                | 41.8 ms: 1.03x slower                                                |
| regex_v8                | 17.7 ms                                                | 18.2 ms: 1.03x slower                                                |
| sympy_sum               | 93.5 ms                                                | 96.8 ms: 1.04x slower                                                |
| pickle_list             | 2.83 us                                                | 2.93 us: 1.04x slower                                                |
| pickle_dict             | 18.0 us                                                | 18.7 us: 1.04x slower                                                |
| gunicorn                | 1.28 ms                                                | 1.34 ms: 1.05x slower                                                |
| aiohttp                 | 1.19 ms                                                | 1.26 ms: 1.06x slower                                                |
| xml_etree_iterparse     | 69.0 ms                                                | 73.1 ms: 1.06x slower                                                |
| flaskblogging           | 2.59 ms                                                | 2.74 ms: 1.06x slower                                                |
| xml_etree_parse         | 100 ms                                                 | 107 ms: 1.07x slower                                                 |
| html5lib                | 44.0 ms                                                | 47.8 ms: 1.09x slower                                                |
| regex_effbot            | 2.45 ms                                                | 2.75 ms: 1.12x slower                                                |
| regex_dna               | 164 ms                                                 | 187 ms: 1.14x slower                                                 |
| pathlib                 | 22.2 ms                                                | 28.7 ms: 1.29x slower                                                |
| python_startup          | 9.59 ms                                                | 12.7 ms: 1.33x slower                                                |
| python_startup_no_site  | 7.00 ms                                                | 9.82 ms: 1.40x slower                                                |
| Geometric mean          | (ref)                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (19): pycparser, unpickle_pure_python, sqlglot_optimize, xml_etree_process, go, sqlglot_transpile, deepcopy_memo, genshi_text, pyflate, hexiom, scimark_lu, scimark_sor, async_tree_cpu_io_mixed, bench_mp_pool, async_tree_io, scimark_monte_carlo, async_tree_memoization, async_tree_none, tornado_http
Ignored benchmarks (1) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: mypy
Ignored benchmarks (6) of public/results/bm-20230207-3.10.10-aad5f6a/bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
