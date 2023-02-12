
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3eb12df
- commit date: 2023-02-11
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| chameleon      | 6.41 ms                                                | 6.58 ms: 1.03x slower                                  |
| docutils       | 2.60 sec                                               | 2.52 sec: 1.03x faster                                 |
| html5lib       | 63.2 ms                                                | 61.1 ms: 1.03x faster                                  |
| tornado_http   | 96.6 ms                                                | 94.5 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.1 ms: 1.06x faster                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.04x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 129 ms: 1.06x faster                                   |
| regex_v8       | 22.3 ms                                                | 21.2 ms: 1.05x faster                                  |
| regex_dna      | 203 ms                                                 | 199 ms: 1.02x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.56 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.51 ms: 1.33x faster                                  |
| unpickle_pure_python | 225 us                                                 | 196 us: 1.15x faster                                   |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                  |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| pickle_pure_python   | 304 us                                                 | 288 us: 1.05x faster                                   |
| pickle_list          | 4.17 us                                                | 4.05 us: 1.03x faster                                  |
| pickle_dict          | 31.4 us                                                | 30.8 us: 1.02x faster                                  |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_process    | 53.8 ms                                                | 55.2 ms: 1.03x slower                                  |
| pickle               | 9.79 us                                                | 10.1 us: 1.03x slower                                  |
| xml_etree_generate   | 76.2 ms                                                | 80.5 ms: 1.06x slower                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (2): unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.92 ms: 1.07x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.47 ms: 1.09x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 46.6 ms: 1.12x faster                                  |
| genshi_text     | 22.1 ms                                                | 20.6 ms: 1.08x faster                                  |
| mako            | 9.85 ms                                                | 9.95 ms: 1.01x slower                                  |
| django_template | 32.5 ms                                                | 33.3 ms: 1.02x slower                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps              | 12.7 ms                                                | 9.51 ms: 1.33x faster                                  |
| deltablue               | 3.64 ms                                                | 3.11 ms: 1.17x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 196 us: 1.15x faster                                   |
| genshi_xml              | 52.1 ms                                                | 46.6 ms: 1.12x faster                                  |
| nqueens                 | 85.0 ms                                                | 77.6 ms: 1.10x faster                                  |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                  |
| richards                | 46.2 ms                                                | 42.3 ms: 1.09x faster                                  |
| logging_silent          | 98.5 ns                                                | 91.0 ns: 1.08x faster                                  |
| scimark_sor             | 115 ms                                                 | 106 ms: 1.08x faster                                   |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                   |
| genshi_text             | 22.1 ms                                                | 20.6 ms: 1.08x faster                                  |
| hexiom                  | 6.35 ms                                                | 5.91 ms: 1.07x faster                                  |
| fannkuch                | 388 ms                                                 | 363 ms: 1.07x faster                                   |
| json                    | 4.95 ms                                                | 4.63 ms: 1.07x faster                                  |
| pycparser               | 1.17 sec                                               | 1.10 sec: 1.07x faster                                 |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.13 ms: 1.07x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.3 us: 1.06x faster                                  |
| mdp                     | 2.62 sec                                               | 2.47 sec: 1.06x faster                                 |
| float                   | 76.3 ms                                                | 72.1 ms: 1.06x faster                                  |
| regex_compile           | 136 ms                                                 | 129 ms: 1.06x faster                                   |
| scimark_fft             | 329 ms                                                 | 312 ms: 1.06x faster                                   |
| pickle_pure_python      | 304 us                                                 | 288 us: 1.05x faster                                   |
| regex_v8                | 22.3 ms                                                | 21.2 ms: 1.05x faster                                  |
| sympy_str               | 287 ms                                                 | 273 ms: 1.05x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 19.9 ms: 1.05x faster                                  |
| pyflate                 | 417 ms                                                 | 398 ms: 1.05x faster                                   |
| telco                   | 6.62 ms                                                | 6.34 ms: 1.04x faster                                  |
| deepcopy                | 344 us                                                 | 329 us: 1.04x faster                                   |
| sqlglot_optimize        | 53.0 ms                                                | 50.8 ms: 1.04x faster                                  |
| sympy_sum               | 166 ms                                                 | 159 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                  |
| coverage                | 101 ms                                                 | 96.8 ms: 1.04x faster                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 65.8 ms: 1.04x faster                                  |
| pidigits                | 199 ms                                                 | 193 ms: 1.04x faster                                   |
| html5lib                | 63.2 ms                                                | 61.1 ms: 1.03x faster                                  |
| coroutines              | 26.1 ms                                                | 25.2 ms: 1.03x faster                                  |
| logging_simple          | 6.06 us                                                | 5.87 us: 1.03x faster                                  |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                  |
| raytrace                | 290 ms                                                 | 281 ms: 1.03x faster                                   |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.03x faster                                   |
| chaos                   | 68.6 ms                                                | 66.5 ms: 1.03x faster                                  |
| pickle_list             | 4.17 us                                                | 4.05 us: 1.03x faster                                  |
| docutils                | 2.60 sec                                               | 2.52 sec: 1.03x faster                                 |
| bench_thread_pool       | 810 us                                                 | 786 us: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                 |
| logging_format          | 6.62 us                                                | 6.43 us: 1.03x faster                                  |
| 2to3                    | 257 ms                                                 | 250 ms: 1.03x faster                                   |
| sympy_expand            | 472 ms                                                 | 459 ms: 1.03x faster                                   |
| pathlib                 | 18.2 ms                                                | 17.7 ms: 1.02x faster                                  |
| tornado_http            | 96.6 ms                                                | 94.5 ms: 1.02x faster                                  |
| regex_dna               | 203 ms                                                 | 199 ms: 1.02x faster                                   |
| pickle_dict             | 31.4 us                                                | 30.8 us: 1.02x faster                                  |
| sqlalchemy_declarative  | 139 ms                                                 | 137 ms: 1.02x faster                                   |
| spectral_norm           | 99.9 ms                                                | 98.5 ms: 1.01x faster                                  |
| dulwich_log             | 63.9 ms                                                | 63.1 ms: 1.01x faster                                  |
| async_tree_none         | 529 ms                                                 | 522 ms: 1.01x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 684 ms: 1.01x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| mako                    | 9.85 ms                                                | 9.95 ms: 1.01x slower                                  |
| unpack_sequence         | 43.4 ns                                                | 43.9 ns: 1.01x slower                                  |
| thrift                  | 752 us                                                 | 761 us: 1.01x slower                                   |
| crypto_pyaes            | 73.9 ms                                                | 75.6 ms: 1.02x slower                                  |
| django_template         | 32.5 ms                                                | 33.3 ms: 1.02x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 55.2 ms: 1.03x slower                                  |
| chameleon               | 6.41 ms                                                | 6.58 ms: 1.03x slower                                  |
| pickle                  | 9.79 us                                                | 10.1 us: 1.03x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.71 ms: 1.03x slower                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.42 ms: 1.04x slower                                  |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                  |
| xml_etree_generate      | 76.2 ms                                                | 80.5 ms: 1.06x slower                                  |
| regex_effbot            | 3.36 ms                                                | 3.56 ms: 1.06x slower                                  |
| python_startup          | 8.36 ms                                                | 8.92 ms: 1.07x slower                                  |
| generators              | 72.2 ms                                                | 77.5 ms: 1.07x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.47 ms: 1.09x slower                                  |
| async_generators        | 359 ms                                                 | 428 ms: 1.19x slower                                   |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (11): async_tree_memoization, nbody, unpickle_list, meteor_contest, bench_mp_pool, deepcopy_reduce, sqlalchemy_imperative, async_tree_cpu_io_mixed, async_tree_io, scimark_lu, unpickle
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230211-3.12.0a5+-3eb12df/bm-20230211-linux-x86_64-python-main-3.12.0a5+-3eb12df.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
