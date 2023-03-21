
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8d32a5c
- commit date: 2022-05-06
- overall geometric mean: 1.01x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 257 ms                                                 | 256 ms: 1.00x faster                                  |
| chameleon      | 6.41 ms                                                | 6.57 ms: 1.02x slower                                 |
| html5lib       | 63.2 ms                                                | 60.1 ms: 1.05x faster                                 |
| tornado_http   | 96.6 ms                                                | 94.6 ms: 1.02x faster                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 76.3 ms                                                | 72.5 ms: 1.05x faster                                 |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 93.1 ms: 1.02x faster                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 3.36 ms                                                | 2.93 ms: 1.14x faster                                 |
| regex_v8       | 22.3 ms                                                | 21.6 ms: 1.03x faster                                 |
| regex_compile  | 136 ms                                                 | 135 ms: 1.01x faster                                  |
| regex_dna      | 203 ms                                                 | 204 ms: 1.00x slower                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 31.4 us                                                | 25.6 us: 1.23x faster                                 |
| json_loads           | 26.2 us                                                | 25.4 us: 1.03x faster                                 |
| json_dumps           | 12.7 ms                                                | 12.4 ms: 1.02x faster                                 |
| pickle               | 9.79 us                                                | 9.56 us: 1.02x faster                                 |
| xml_etree_generate   | 76.2 ms                                                | 76.5 ms: 1.00x slower                                 |
| pickle_pure_python   | 304 us                                                 | 305 us: 1.00x slower                                  |
| unpickle_pure_python | 225 us                                                 | 229 us: 1.01x slower                                  |
| xml_etree_iterparse  | 103 ms                                                 | 104 ms: 1.02x slower                                  |
| pickle_list          | 4.17 us                                                | 4.26 us: 1.02x slower                                 |
| unpickle_list        | 4.95 us                                                | 5.05 us: 1.02x slower                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                          |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.25 ms: 1.01x faster                                 |
| python_startup_no_site | 5.96 ms                                                | 6.16 ms: 1.03x slower                                 |
| Geometric mean         | (ref)                                                  | 1.01x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| mako            | 9.85 ms                                                | 9.88 ms: 1.00x slower                                 |
| django_template | 32.5 ms                                                | 32.8 ms: 1.01x slower                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict             | 31.4 us                                                | 25.6 us: 1.23x faster                                 |
| regex_effbot            | 3.36 ms                                                | 2.93 ms: 1.14x faster                                 |
| go                      | 143 ms                                                 | 136 ms: 1.05x faster                                  |
| float                   | 76.3 ms                                                | 72.5 ms: 1.05x faster                                 |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 60.1 ms: 1.05x faster                                 |
| json_loads              | 26.2 us                                                | 25.4 us: 1.03x faster                                 |
| regex_v8                | 22.3 ms                                                | 21.6 ms: 1.03x faster                                 |
| sympy_sum               | 166 ms                                                 | 161 ms: 1.03x faster                                  |
| logging_simple          | 6.06 us                                                | 5.89 us: 1.03x faster                                 |
| scimark_monte_carlo     | 68.3 ms                                                | 66.5 ms: 1.03x faster                                 |
| logging_format          | 6.62 us                                                | 6.44 us: 1.03x faster                                 |
| json_dumps              | 12.7 ms                                                | 12.4 ms: 1.02x faster                                 |
| spectral_norm           | 99.9 ms                                                | 97.6 ms: 1.02x faster                                 |
| pickle                  | 9.79 us                                                | 9.56 us: 1.02x faster                                 |
| tornado_http            | 96.6 ms                                                | 94.6 ms: 1.02x faster                                 |
| nbody                   | 95.0 ms                                                | 93.1 ms: 1.02x faster                                 |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.8 ms: 1.02x faster                                 |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.02x faster                                 |
| pyflate                 | 417 ms                                                 | 411 ms: 1.02x faster                                  |
| thrift                  | 752 us                                                 | 741 us: 1.01x faster                                  |
| sympy_str               | 287 ms                                                 | 284 ms: 1.01x faster                                  |
| python_startup          | 8.36 ms                                                | 8.25 ms: 1.01x faster                                 |
| scimark_fft             | 329 ms                                                 | 325 ms: 1.01x faster                                  |
| regex_compile           | 136 ms                                                 | 135 ms: 1.01x faster                                  |
| deltablue               | 3.64 ms                                                | 3.61 ms: 1.01x faster                                 |
| sympy_expand            | 472 ms                                                 | 468 ms: 1.01x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.29 ms: 1.01x faster                                 |
| fannkuch                | 388 ms                                                 | 385 ms: 1.01x faster                                  |
| json                    | 4.95 ms                                                | 4.91 ms: 1.01x faster                                 |
| 2to3                    | 257 ms                                                 | 256 ms: 1.00x faster                                  |
| nqueens                 | 85.0 ms                                                | 84.7 ms: 1.00x faster                                 |
| logging_silent          | 98.5 ns                                                | 98.2 ns: 1.00x faster                                 |
| mako                    | 9.85 ms                                                | 9.88 ms: 1.00x slower                                 |
| xml_etree_generate      | 76.2 ms                                                | 76.5 ms: 1.00x slower                                 |
| regex_dna               | 203 ms                                                 | 204 ms: 1.00x slower                                  |
| pickle_pure_python      | 304 us                                                 | 305 us: 1.00x slower                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.3 ms: 1.00x slower                                 |
| pycparser               | 1.17 sec                                               | 1.18 sec: 1.01x slower                                |
| django_template         | 32.5 ms                                                | 32.8 ms: 1.01x slower                                 |
| raytrace                | 290 ms                                                 | 294 ms: 1.01x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.53 us: 1.01x slower                                 |
| unpickle_pure_python    | 225 us                                                 | 229 us: 1.01x slower                                  |
| scimark_lu              | 107 ms                                                 | 109 ms: 1.02x slower                                  |
| xml_etree_iterparse     | 103 ms                                                 | 104 ms: 1.02x slower                                  |
| pickle_list             | 4.17 us                                                | 4.26 us: 1.02x slower                                 |
| unpack_sequence         | 43.4 ns                                                | 44.3 ns: 1.02x slower                                 |
| unpickle_list           | 4.95 us                                                | 5.05 us: 1.02x slower                                 |
| chameleon               | 6.41 ms                                                | 6.57 ms: 1.02x slower                                 |
| telco                   | 6.62 ms                                                | 6.84 ms: 1.03x slower                                 |
| python_startup_no_site  | 5.96 ms                                                | 6.16 ms: 1.03x slower                                 |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.57 ms: 1.04x slower                                 |
| Geometric mean          | (ref)                                                  | 1.01x faster                                          |

Benchmark hidden because not significant (7): xml_etree_parse, scimark_sor, xml_etree_process, meteor_contest, chaos, richards, unpickle
Ignored benchmarks (30) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
