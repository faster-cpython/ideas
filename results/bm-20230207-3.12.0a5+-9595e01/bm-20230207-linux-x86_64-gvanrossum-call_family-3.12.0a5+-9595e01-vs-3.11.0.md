
# Results vs. 3.11.0

- fork: gvanrossum
- ref: call_family
- machine: linux-x86_64
- commit hash: 9595e01
- commit date: 2023-02-07
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 251 ms: 1.03x faster                                              |
| chameleon      | 6.41 ms                                                | 6.36 ms: 1.01x faster                                             |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                            |
| html5lib       | 63.2 ms                                                | 61.1 ms: 1.03x faster                                             |
| tornado_http   | 96.6 ms                                                | 93.7 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 76.3 ms                                                | 73.7 ms: 1.04x faster                                             |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                              |
| nbody          | 95.0 ms                                                | 96.0 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                  | 1.01x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.06x faster                                              |
| regex_v8       | 22.3 ms                                                | 21.7 ms: 1.03x faster                                             |
| regex_dna      | 203 ms                                                 | 205 ms: 1.01x slower                                              |
| regex_effbot   | 3.36 ms                                                | 3.62 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                  | 1.00x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.53 ms: 1.33x faster                                             |
| unpickle_pure_python | 225 us                                                 | 199 us: 1.13x faster                                              |
| json_loads           | 26.2 us                                                | 24.3 us: 1.08x faster                                             |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                              |
| pickle_pure_python   | 304 us                                                 | 286 us: 1.06x faster                                              |
| xml_etree_process    | 53.8 ms                                                | 53.2 ms: 1.01x faster                                             |
| pickle_list          | 4.17 us                                                | 4.14 us: 1.01x faster                                             |
| pickle_dict          | 31.4 us                                                | 31.6 us: 1.00x slower                                             |
| unpickle_list        | 4.95 us                                                | 5.01 us: 1.01x slower                                             |
| xml_etree_generate   | 76.2 ms                                                | 77.4 ms: 1.02x slower                                             |
| pickle               | 9.79 us                                                | 10.4 us: 1.06x slower                                             |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.91 ms: 1.07x slower                                             |
| python_startup_no_site | 5.96 ms                                                | 6.47 ms: 1.08x slower                                             |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 46.5 ms: 1.12x faster                                             |
| genshi_text     | 22.1 ms                                                | 20.7 ms: 1.07x faster                                             |
| django_template | 32.5 ms                                                | 32.6 ms: 1.01x slower                                             |
| mako            | 9.85 ms                                                | 9.92 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                      |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.53 ms: 1.33x faster                                             |
| deltablue               | 3.64 ms                                                | 3.16 ms: 1.15x faster                                             |
| unpickle_pure_python    | 225 us                                                 | 199 us: 1.13x faster                                              |
| genshi_xml              | 52.1 ms                                                | 46.5 ms: 1.12x faster                                             |
| fannkuch                | 388 ms                                                 | 355 ms: 1.09x faster                                              |
| richards                | 46.2 ms                                                | 42.2 ms: 1.09x faster                                             |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.04 ms: 1.09x faster                                             |
| json_loads              | 26.2 us                                                | 24.3 us: 1.08x faster                                             |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                              |
| genshi_text             | 22.1 ms                                                | 20.7 ms: 1.07x faster                                             |
| sympy_str               | 287 ms                                                 | 270 ms: 1.07x faster                                              |
| sympy_sum               | 166 ms                                                 | 156 ms: 1.07x faster                                              |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                              |
| hexiom                  | 6.35 ms                                                | 5.96 ms: 1.06x faster                                             |
| scimark_sor             | 115 ms                                                 | 108 ms: 1.06x faster                                              |
| regex_compile           | 136 ms                                                 | 128 ms: 1.06x faster                                              |
| scimark_fft             | 329 ms                                                 | 309 ms: 1.06x faster                                              |
| pickle_pure_python      | 304 us                                                 | 286 us: 1.06x faster                                              |
| coroutines              | 26.1 ms                                                | 24.5 ms: 1.06x faster                                             |
| sympy_integrate         | 20.9 ms                                                | 19.7 ms: 1.06x faster                                             |
| logging_silent          | 98.5 ns                                                | 93.3 ns: 1.06x faster                                             |
| json                    | 4.95 ms                                                | 4.70 ms: 1.05x faster                                             |
| coverage                | 101 ms                                                 | 95.6 ms: 1.05x faster                                             |
| nqueens                 | 85.0 ms                                                | 81.0 ms: 1.05x faster                                             |
| spectral_norm           | 99.9 ms                                                | 95.4 ms: 1.05x faster                                             |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.04x faster                                             |
| unpack_sequence         | 43.4 ns                                                | 41.6 ns: 1.04x faster                                             |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                             |
| deepcopy_memo           | 36.4 us                                                | 35.0 us: 1.04x faster                                             |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                            |
| sympy_expand            | 472 ms                                                 | 454 ms: 1.04x faster                                              |
| chaos                   | 68.6 ms                                                | 66.1 ms: 1.04x faster                                             |
| async_generators        | 359 ms                                                 | 347 ms: 1.04x faster                                              |
| bench_thread_pool       | 810 us                                                 | 781 us: 1.04x faster                                              |
| float                   | 76.3 ms                                                | 73.7 ms: 1.04x faster                                             |
| html5lib                | 63.2 ms                                                | 61.1 ms: 1.03x faster                                             |
| pyflate                 | 417 ms                                                 | 404 ms: 1.03x faster                                              |
| sqlglot_optimize        | 53.0 ms                                                | 51.4 ms: 1.03x faster                                             |
| scimark_monte_carlo     | 68.3 ms                                                | 66.2 ms: 1.03x faster                                             |
| tornado_http            | 96.6 ms                                                | 93.7 ms: 1.03x faster                                             |
| logging_simple          | 6.06 us                                                | 5.89 us: 1.03x faster                                             |
| regex_v8                | 22.3 ms                                                | 21.7 ms: 1.03x faster                                             |
| raytrace                | 290 ms                                                 | 283 ms: 1.03x faster                                              |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                            |
| telco                   | 6.62 ms                                                | 6.45 ms: 1.03x faster                                             |
| 2to3                    | 257 ms                                                 | 251 ms: 1.03x faster                                              |
| deepcopy                | 344 us                                                 | 336 us: 1.02x faster                                              |
| thrift                  | 752 us                                                 | 735 us: 1.02x faster                                              |
| sqlglot_normalize       | 108 ms                                                 | 105 ms: 1.02x faster                                              |
| logging_format          | 6.62 us                                                | 6.48 us: 1.02x faster                                             |
| crypto_pyaes            | 73.9 ms                                                | 72.6 ms: 1.02x faster                                             |
| pycparser               | 1.17 sec                                               | 1.15 sec: 1.02x faster                                            |
| dulwich_log             | 63.9 ms                                                | 63.0 ms: 1.01x faster                                             |
| async_tree_none         | 529 ms                                                 | 522 ms: 1.01x faster                                              |
| mdp                     | 2.62 sec                                               | 2.59 sec: 1.01x faster                                            |
| pathlib                 | 18.2 ms                                                | 18.0 ms: 1.01x faster                                             |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                              |
| xml_etree_process       | 53.8 ms                                                | 53.2 ms: 1.01x faster                                             |
| pickle_list             | 4.17 us                                                | 4.14 us: 1.01x faster                                             |
| chameleon               | 6.41 ms                                                | 6.36 ms: 1.01x faster                                             |
| pickle_dict             | 31.4 us                                                | 31.6 us: 1.00x slower                                             |
| django_template         | 32.5 ms                                                | 32.6 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed | 752 ms                                                 | 757 ms: 1.01x slower                                              |
| mako                    | 9.85 ms                                                | 9.92 ms: 1.01x slower                                             |
| regex_dna               | 203 ms                                                 | 205 ms: 1.01x slower                                              |
| nbody                   | 95.0 ms                                                | 96.0 ms: 1.01x slower                                             |
| unpickle_list           | 4.95 us                                                | 5.01 us: 1.01x slower                                             |
| xml_etree_generate      | 76.2 ms                                                | 77.4 ms: 1.02x slower                                             |
| meteor_contest          | 105 ms                                                 | 108 ms: 1.03x slower                                              |
| sqlite_synth            | 2.49 us                                                | 2.58 us: 1.03x slower                                             |
| async_tree_memoization  | 625 ms                                                 | 647 ms: 1.04x slower                                              |
| sqlglot_transpile       | 1.66 ms                                                | 1.72 ms: 1.04x slower                                             |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.04x slower                                             |
| generators              | 72.2 ms                                                | 75.7 ms: 1.05x slower                                             |
| pickle                  | 9.79 us                                                | 10.4 us: 1.06x slower                                             |
| python_startup          | 8.36 ms                                                | 8.91 ms: 1.07x slower                                             |
| regex_effbot            | 3.36 ms                                                | 3.62 ms: 1.08x slower                                             |
| python_startup_no_site  | 5.96 ms                                                | 6.47 ms: 1.08x slower                                             |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                      |

Benchmark hidden because not significant (9): sqlalchemy_imperative, scimark_lu, sqlalchemy_declarative, pprint_safe_repr, bench_mp_pool, xml_etree_iterparse, unpickle, async_tree_io, deepcopy_reduce
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230207-3.12.0a5+-9595e01/bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
