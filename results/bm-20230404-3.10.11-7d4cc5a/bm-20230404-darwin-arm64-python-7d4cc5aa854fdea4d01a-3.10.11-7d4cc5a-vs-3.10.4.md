
# Results vs. 3.10.4

- fork: python
- ref: 7d4cc5aa854fdea4d01a
- machine: darwin-arm64
- commit hash: 7d4cc5a
- commit date: 2023-04-04
- overall geometric mean: 1.02x slower \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 203 ms: 1.09x faster                                                 |
| chameleon      | 5.86 ms                                                | 5.75 ms: 1.02x faster                                                |
| docutils       | 1.76 sec                                               | 1.79 sec: 1.02x slower                                               |
| html5lib       | 44.0 ms                                                | 47.8 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                 |
| nbody          | 94.6 ms                                                | 94.0 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 96.9 ms: 1.01x slower                                                |
| regex_v8       | 17.7 ms                                                | 18.0 ms: 1.01x slower                                                |
| regex_effbot   | 2.45 ms                                                | 2.69 ms: 1.10x slower                                                |
| regex_dna      | 164 ms                                                 | 185 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|---------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle            | 10.0 us                                                | 9.89 us: 1.01x faster                                                |
| json_loads          | 17.0 us                                                | 16.8 us: 1.01x faster                                                |
| json_dumps          | 8.34 ms                                                | 8.27 ms: 1.01x faster                                                |
| xml_etree_process   | 45.1 ms                                                | 44.9 ms: 1.00x faster                                                |
| xml_etree_generate  | 54.5 ms                                                | 54.3 ms: 1.00x faster                                                |
| pickle_pure_python  | 284 us                                                 | 285 us: 1.01x slower                                                 |
| pickle              | 7.50 us                                                | 7.56 us: 1.01x slower                                                |
| unpickle_list       | 2.66 us                                                | 2.69 us: 1.01x slower                                                |
| pickle_list         | 2.83 us                                                | 2.90 us: 1.02x slower                                                |
| pickle_dict         | 18.0 us                                                | 18.8 us: 1.05x slower                                                |
| xml_etree_iterparse | 69.0 ms                                                | 73.2 ms: 1.06x slower                                                |
| xml_etree_parse     | 100 ms                                                 | 113 ms: 1.13x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.1 ms: 1.27x slower                                                |
| python_startup_no_site | 7.00 ms                                                | 9.13 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 37.7 ms                                                | 37.3 ms: 1.01x faster                                                |
| django_template | 27.2 ms                                                | 27.1 ms: 1.01x faster                                                |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 203 ms: 1.09x faster                                                 |
| deltablue               | 5.37 ms                                                | 5.17 ms: 1.04x faster                                                |
| json                    | 3.13 ms                                                | 3.06 ms: 1.02x faster                                                |
| chameleon               | 5.86 ms                                                | 5.75 ms: 1.02x faster                                                |
| unpickle                | 10.0 us                                                | 9.89 us: 1.01x faster                                                |
| sqlite_synth            | 1.50 us                                                | 1.48 us: 1.01x faster                                                |
| sqlglot_normalize       | 198 ms                                                 | 196 ms: 1.01x faster                                                 |
| richards                | 51.4 ms                                                | 50.7 ms: 1.01x faster                                                |
| genshi_xml              | 37.7 ms                                                | 37.3 ms: 1.01x faster                                                |
| json_loads              | 17.0 us                                                | 16.8 us: 1.01x faster                                                |
| pprint_safe_repr        | 608 ms                                                 | 602 ms: 1.01x faster                                                 |
| json_dumps              | 8.34 ms                                                | 8.27 ms: 1.01x faster                                                |
| nqueens                 | 68.6 ms                                                | 68.0 ms: 1.01x faster                                                |
| pprint_pformat          | 1.24 sec                                               | 1.23 sec: 1.01x faster                                               |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                 |
| nbody                   | 94.6 ms                                                | 94.0 ms: 1.01x faster                                                |
| sqlglot_transpile       | 1.54 ms                                                | 1.53 ms: 1.01x faster                                                |
| django_template         | 27.2 ms                                                | 27.1 ms: 1.01x faster                                                |
| xml_etree_process       | 45.1 ms                                                | 44.9 ms: 1.00x faster                                                |
| xml_etree_generate      | 54.5 ms                                                | 54.3 ms: 1.00x faster                                                |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.46 ms: 1.00x faster                                                |
| sqlglot_optimize        | 38.1 ms                                                | 38.0 ms: 1.00x faster                                                |
| coroutines              | 20.1 ms                                                | 20.1 ms: 1.00x slower                                                |
| deepcopy_memo           | 34.4 us                                                | 34.5 us: 1.00x slower                                                |
| unpack_sequence         | 38.2 ns                                                | 38.3 ns: 1.00x slower                                                |
| deepcopy                | 278 us                                                 | 279 us: 1.00x slower                                                 |
| mdp                     | 1.66 sec                                               | 1.67 sec: 1.00x slower                                               |
| hexiom                  | 6.31 ms                                                | 6.33 ms: 1.00x slower                                                |
| meteor_contest          | 77.7 ms                                                | 78.0 ms: 1.00x slower                                                |
| bench_thread_pool       | 531 us                                                 | 532 us: 1.00x slower                                                 |
| thrift                  | 577 us                                                 | 580 us: 1.00x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 78.3 ms: 1.00x slower                                                |
| pickle_pure_python      | 284 us                                                 | 285 us: 1.01x slower                                                 |
| spectral_norm           | 95.8 ms                                                | 96.4 ms: 1.01x slower                                                |
| raytrace                | 329 ms                                                 | 331 ms: 1.01x slower                                                 |
| sympy_expand            | 275 ms                                                 | 277 ms: 1.01x slower                                                 |
| generators              | 32.5 ms                                                | 32.7 ms: 1.01x slower                                                |
| pickle                  | 7.50 us                                                | 7.56 us: 1.01x slower                                                |
| deepcopy_reduce         | 2.36 us                                                | 2.38 us: 1.01x slower                                                |
| regex_compile           | 96.2 ms                                                | 96.9 ms: 1.01x slower                                                |
| sympy_str               | 169 ms                                                 | 170 ms: 1.01x slower                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 75.0 ms: 1.01x slower                                                |
| sympy_integrate         | 13.3 ms                                                | 13.4 ms: 1.01x slower                                                |
| async_tree_memoization  | 485 ms                                                 | 490 ms: 1.01x slower                                                 |
| logging_simple          | 4.61 us                                                | 4.65 us: 1.01x slower                                                |
| async_generators        | 231 ms                                                 | 233 ms: 1.01x slower                                                 |
| unpickle_list           | 2.66 us                                                | 2.69 us: 1.01x slower                                                |
| dulwich_log             | 36.4 ms                                                | 36.9 ms: 1.01x slower                                                |
| regex_v8                | 17.7 ms                                                | 18.0 ms: 1.01x slower                                                |
| docutils                | 1.76 sec                                               | 1.79 sec: 1.02x slower                                               |
| pylint                  | 302 ms                                                 | 307 ms: 1.02x slower                                                 |
| chaos                   | 66.5 ms                                                | 68.0 ms: 1.02x slower                                                |
| logging_format          | 4.95 us                                                | 5.05 us: 1.02x slower                                                |
| pickle_list             | 2.83 us                                                | 2.90 us: 1.02x slower                                                |
| coverage                | 40.8 ms                                                | 41.9 ms: 1.03x slower                                                |
| sympy_sum               | 93.5 ms                                                | 96.4 ms: 1.03x slower                                                |
| pickle_dict             | 18.0 us                                                | 18.8 us: 1.05x slower                                                |
| gunicorn                | 1.28 ms                                                | 1.34 ms: 1.05x slower                                                |
| aiohttp                 | 1.19 ms                                                | 1.26 ms: 1.06x slower                                                |
| xml_etree_iterparse     | 69.0 ms                                                | 73.2 ms: 1.06x slower                                                |
| flaskblogging           | 2.59 ms                                                | 2.76 ms: 1.07x slower                                                |
| html5lib                | 44.0 ms                                                | 47.8 ms: 1.09x slower                                                |
| regex_effbot            | 2.45 ms                                                | 2.69 ms: 1.10x slower                                                |
| regex_dna               | 164 ms                                                 | 185 ms: 1.12x slower                                                 |
| xml_etree_parse         | 100 ms                                                 | 113 ms: 1.13x slower                                                 |
| python_startup          | 9.59 ms                                                | 12.1 ms: 1.27x slower                                                |
| pathlib                 | 22.2 ms                                                | 28.3 ms: 1.27x slower                                                |
| python_startup_no_site  | 7.00 ms                                                | 9.13 ms: 1.30x slower                                                |
| Geometric mean          | (ref)                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (21): bench_mp_pool, pycparser, mako, telco, unpickle_pure_python, sqlalchemy_imperative, scimark_fft, scimark_sor, scimark_monte_carlo, scimark_lu, go, sqlglot_parse, fannkuch, float, pyflate, logging_silent, genshi_text, async_tree_cpu_io_mixed, async_tree_io, async_tree_none, tornado_http
Ignored benchmarks (1) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: mypy
Ignored benchmarks (6) of public/results/bm-20230404-3.10.11-7d4cc5a/bm-20230404-darwin-arm64-python-7d4cc5aa854fdea4d01a-3.10.11-7d4cc5a.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
