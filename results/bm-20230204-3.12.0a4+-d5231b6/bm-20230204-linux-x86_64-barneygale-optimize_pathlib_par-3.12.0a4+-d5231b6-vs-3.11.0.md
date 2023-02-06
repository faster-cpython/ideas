
# Results vs. 3.11.0

- fork: barneygale
- ref: optimize_pathlib_par
- machine: linux-x86_64
- commit hash: d5231b6
- commit date: 2023-02-04
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                                       |
| chameleon      | 6.41 ms                                                | 6.27 ms: 1.02x faster                                                      |
| docutils       | 2.60 sec                                               | 2.51 sec: 1.03x faster                                                     |
| html5lib       | 63.2 ms                                                | 60.4 ms: 1.05x faster                                                      |
| tornado_http   | 96.6 ms                                                | 93.7 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.2 ms: 1.06x faster                                                      |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                                       |
| nbody          | 95.0 ms                                                | 92.6 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                  | 1.05x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                                       |
| regex_v8       | 22.3 ms                                                | 22.6 ms: 1.01x slower                                                      |
| regex_dna      | 203 ms                                                 | 216 ms: 1.06x slower                                                       |
| regex_effbot   | 3.36 ms                                                | 3.59 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.22 ms: 1.37x faster                                                      |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.14x faster                                                       |
| json_loads           | 26.2 us                                                | 23.9 us: 1.10x faster                                                      |
| pickle_pure_python   | 304 us                                                 | 280 us: 1.08x faster                                                       |
| xml_etree_parse      | 158 ms                                                 | 146 ms: 1.08x faster                                                       |
| pickle_dict          | 31.4 us                                                | 30.6 us: 1.03x faster                                                      |
| xml_etree_process    | 53.8 ms                                                | 54.0 ms: 1.00x slower                                                      |
| unpickle_list        | 4.95 us                                                | 4.98 us: 1.01x slower                                                      |
| xml_etree_generate   | 76.2 ms                                                | 77.7 ms: 1.02x slower                                                      |
| pickle               | 9.79 us                                                | 10.1 us: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                               |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.91 ms: 1.07x slower                                                      |
| python_startup_no_site | 5.96 ms                                                | 6.44 ms: 1.08x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml     | 52.1 ms                                                | 46.5 ms: 1.12x faster                                                      |
| genshi_text    | 22.1 ms                                                | 20.8 ms: 1.07x faster                                                      |
| mako           | 9.85 ms                                                | 9.74 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                  | 1.05x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.22 ms: 1.37x faster                                                      |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.14x faster                                                       |
| deltablue               | 3.64 ms                                                | 3.19 ms: 1.14x faster                                                      |
| genshi_xml              | 52.1 ms                                                | 46.5 ms: 1.12x faster                                                      |
| nqueens                 | 85.0 ms                                                | 77.0 ms: 1.10x faster                                                      |
| scimark_sparse_mat_mult | 4.40 ms                                                | 3.99 ms: 1.10x faster                                                      |
| json_loads              | 26.2 us                                                | 23.9 us: 1.10x faster                                                      |
| richards                | 46.2 ms                                                | 42.3 ms: 1.09x faster                                                      |
| scimark_fft             | 329 ms                                                 | 302 ms: 1.09x faster                                                       |
| pickle_pure_python      | 304 us                                                 | 280 us: 1.08x faster                                                       |
| fannkuch                | 388 ms                                                 | 359 ms: 1.08x faster                                                       |
| xml_etree_parse         | 158 ms                                                 | 146 ms: 1.08x faster                                                       |
| chaos                   | 68.6 ms                                                | 63.6 ms: 1.08x faster                                                      |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                                       |
| mdp                     | 2.62 sec                                               | 2.44 sec: 1.07x faster                                                     |
| sympy_sum               | 166 ms                                                 | 155 ms: 1.07x faster                                                       |
| json                    | 4.95 ms                                                | 4.63 ms: 1.07x faster                                                      |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                                       |
| sympy_str               | 287 ms                                                 | 269 ms: 1.07x faster                                                       |
| genshi_text             | 22.1 ms                                                | 20.8 ms: 1.07x faster                                                      |
| logging_simple          | 6.06 us                                                | 5.72 us: 1.06x faster                                                      |
| go                      | 143 ms                                                 | 135 ms: 1.06x faster                                                       |
| spectral_norm           | 99.9 ms                                                | 94.5 ms: 1.06x faster                                                      |
| float                   | 76.3 ms                                                | 72.2 ms: 1.06x faster                                                      |
| coverage                | 101 ms                                                 | 95.1 ms: 1.06x faster                                                      |
| deepcopy_memo           | 36.4 us                                                | 34.5 us: 1.06x faster                                                      |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.06x faster                                                     |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                                       |
| hexiom                  | 6.35 ms                                                | 6.03 ms: 1.05x faster                                                      |
| coroutines              | 26.1 ms                                                | 24.8 ms: 1.05x faster                                                      |
| sympy_integrate         | 20.9 ms                                                | 19.8 ms: 1.05x faster                                                      |
| aiohttp                 | 1.05 ms                                                | 995 us: 1.05x faster                                                       |
| pyflate                 | 417 ms                                                 | 397 ms: 1.05x faster                                                       |
| scimark_monte_carlo     | 68.3 ms                                                | 65.1 ms: 1.05x faster                                                      |
| logging_silent          | 98.5 ns                                                | 94.0 ns: 1.05x faster                                                      |
| deepcopy                | 344 us                                                 | 328 us: 1.05x faster                                                       |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                                      |
| html5lib                | 63.2 ms                                                | 60.4 ms: 1.05x faster                                                      |
| logging_format          | 6.62 us                                                | 6.36 us: 1.04x faster                                                      |
| pprint_safe_repr        | 691 ms                                                 | 666 ms: 1.04x faster                                                       |
| sqlglot_optimize        | 53.0 ms                                                | 51.1 ms: 1.04x faster                                                      |
| sympy_expand            | 472 ms                                                 | 456 ms: 1.04x faster                                                       |
| docutils                | 2.60 sec                                               | 2.51 sec: 1.03x faster                                                     |
| raytrace                | 290 ms                                                 | 281 ms: 1.03x faster                                                       |
| telco                   | 6.62 ms                                                | 6.41 ms: 1.03x faster                                                      |
| bench_thread_pool       | 810 us                                                 | 785 us: 1.03x faster                                                       |
| tornado_http            | 96.6 ms                                                | 93.7 ms: 1.03x faster                                                      |
| nbody                   | 95.0 ms                                                | 92.6 ms: 1.03x faster                                                      |
| pickle_dict             | 31.4 us                                                | 30.6 us: 1.03x faster                                                      |
| async_generators        | 359 ms                                                 | 350 ms: 1.03x faster                                                       |
| chameleon               | 6.41 ms                                                | 6.27 ms: 1.02x faster                                                      |
| sqlglot_normalize       | 108 ms                                                 | 106 ms: 1.02x faster                                                       |
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                                       |
| pycparser               | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                     |
| dulwich_log             | 63.9 ms                                                | 62.8 ms: 1.02x faster                                                      |
| deepcopy_reduce         | 2.97 us                                                | 2.93 us: 1.01x faster                                                      |
| mako                    | 9.85 ms                                                | 9.74 ms: 1.01x faster                                                      |
| crypto_pyaes            | 73.9 ms                                                | 73.4 ms: 1.01x faster                                                      |
| xml_etree_process       | 53.8 ms                                                | 54.0 ms: 1.00x slower                                                      |
| unpickle_list           | 4.95 us                                                | 4.98 us: 1.01x slower                                                      |
| async_tree_cpu_io_mixed | 752 ms                                                 | 757 ms: 1.01x slower                                                       |
| regex_v8                | 22.3 ms                                                | 22.6 ms: 1.01x slower                                                      |
| xml_etree_generate      | 76.2 ms                                                | 77.7 ms: 1.02x slower                                                      |
| scimark_lu              | 107 ms                                                 | 110 ms: 1.02x slower                                                       |
| generators              | 72.2 ms                                                | 74.2 ms: 1.03x slower                                                      |
| pickle                  | 9.79 us                                                | 10.1 us: 1.03x slower                                                      |
| sqlglot_transpile       | 1.66 ms                                                | 1.72 ms: 1.04x slower                                                      |
| pathlib                 | 18.2 ms                                                | 19.0 ms: 1.04x slower                                                      |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.04x slower                                                      |
| async_tree_memoization  | 625 ms                                                 | 654 ms: 1.05x slower                                                       |
| sqlite_synth            | 2.49 us                                                | 2.61 us: 1.05x slower                                                      |
| regex_dna               | 203 ms                                                 | 216 ms: 1.06x slower                                                       |
| python_startup          | 8.36 ms                                                | 8.91 ms: 1.07x slower                                                      |
| regex_effbot            | 3.36 ms                                                | 3.59 ms: 1.07x slower                                                      |
| python_startup_no_site  | 5.96 ms                                                | 6.44 ms: 1.08x slower                                                      |
| mypy                    | 669 ms                                                 | 810 ms: 1.21x slower                                                       |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (10): unpack_sequence, async_tree_none, meteor_contest, xml_etree_iterparse, pickle_list, bench_mp_pool, async_tree_io, thrift, django_template, unpickle
Ignored benchmarks (4) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230204-3.12.0a4+-d5231b6/bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
