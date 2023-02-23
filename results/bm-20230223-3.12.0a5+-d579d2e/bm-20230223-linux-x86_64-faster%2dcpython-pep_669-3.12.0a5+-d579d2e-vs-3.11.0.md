
# Results vs. 3.11.0

- fork: faster-cpython
- ref: pep_669
- machine: linux-x86_64
- commit hash: d579d2e
- commit date: 2023-02-23
- overall geometric mean: 1.04x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 247 ms: 1.04x faster                                                |
| chameleon      | 6.41 ms                                                | 6.26 ms: 1.02x faster                                               |
| docutils       | 2.60 sec                                               | 2.51 sec: 1.03x faster                                              |
| html5lib       | 63.2 ms                                                | 59.8 ms: 1.06x faster                                               |
| tornado_http   | 96.6 ms                                                | 93.8 ms: 1.03x faster                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 73.4 ms: 1.04x faster                                               |
| pidigits       | 199 ms                                                 | 192 ms: 1.04x faster                                                |
| nbody          | 95.0 ms                                                | 92.2 ms: 1.03x faster                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 129 ms: 1.06x faster                                                |
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                               |
| regex_dna      | 203 ms                                                 | 200 ms: 1.01x faster                                                |
| regex_effbot   | 3.36 ms                                                | 3.63 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                  | 1.00x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.40 ms: 1.35x faster                                               |
| unpickle_pure_python | 225 us                                                 | 194 us: 1.16x faster                                                |
| json_loads           | 26.2 us                                                | 23.7 us: 1.10x faster                                               |
| pickle_pure_python   | 304 us                                                 | 277 us: 1.10x faster                                                |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                |
| xml_etree_iterparse  | 103 ms                                                 | 99.7 ms: 1.03x faster                                               |
| unpickle_list        | 4.95 us                                                | 4.98 us: 1.01x slower                                               |
| pickle_dict          | 31.4 us                                                | 31.7 us: 1.01x slower                                               |
| xml_etree_process    | 53.8 ms                                                | 54.4 ms: 1.01x slower                                               |
| pickle_list          | 4.17 us                                                | 4.27 us: 1.02x slower                                               |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                               |
| xml_etree_generate   | 76.2 ms                                                | 79.4 ms: 1.04x slower                                               |
| unpickle             | 13.3 us                                                | 13.9 us: 1.05x slower                                               |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.06 ms: 1.08x slower                                               |
| python_startup_no_site | 5.96 ms                                                | 6.58 ms: 1.10x slower                                               |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 45.9 ms: 1.13x faster                                               |
| genshi_text     | 22.1 ms                                                | 20.5 ms: 1.08x faster                                               |
| mako            | 9.85 ms                                                | 9.75 ms: 1.01x faster                                               |
| django_template | 32.5 ms                                                | 32.8 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 31.6 ms: 2.28x faster                                               |
| json_dumps              | 12.7 ms                                                | 9.40 ms: 1.35x faster                                               |
| coroutines              | 26.1 ms                                                | 22.0 ms: 1.18x faster                                               |
| deltablue               | 3.64 ms                                                | 3.14 ms: 1.16x faster                                               |
| unpickle_pure_python    | 225 us                                                 | 194 us: 1.16x faster                                                |
| genshi_xml              | 52.1 ms                                                | 45.9 ms: 1.13x faster                                               |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.11x faster                                                |
| richards                | 46.2 ms                                                | 41.6 ms: 1.11x faster                                               |
| json_loads              | 26.2 us                                                | 23.7 us: 1.10x faster                                               |
| deepcopy_memo           | 36.4 us                                                | 33.1 us: 1.10x faster                                               |
| go                      | 143 ms                                                 | 130 ms: 1.10x faster                                                |
| pickle_pure_python      | 304 us                                                 | 277 us: 1.10x faster                                                |
| fannkuch                | 388 ms                                                 | 357 ms: 1.09x faster                                                |
| scimark_fft             | 329 ms                                                 | 302 ms: 1.09x faster                                                |
| nqueens                 | 85.0 ms                                                | 78.4 ms: 1.09x faster                                               |
| json                    | 4.95 ms                                                | 4.58 ms: 1.08x faster                                               |
| genshi_text             | 22.1 ms                                                | 20.5 ms: 1.08x faster                                               |
| logging_silent          | 98.5 ns                                                | 91.7 ns: 1.07x faster                                               |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.07x faster                                              |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                |
| deepcopy                | 344 us                                                 | 323 us: 1.07x faster                                                |
| scimark_monte_carlo     | 68.3 ms                                                | 64.2 ms: 1.06x faster                                               |
| sqlglot_normalize       | 108 ms                                                 | 102 ms: 1.06x faster                                                |
| hexiom                  | 6.35 ms                                                | 6.00 ms: 1.06x faster                                               |
| regex_compile           | 136 ms                                                 | 129 ms: 1.06x faster                                                |
| sqlglot_optimize        | 53.0 ms                                                | 50.1 ms: 1.06x faster                                               |
| spectral_norm           | 99.9 ms                                                | 94.6 ms: 1.06x faster                                               |
| html5lib                | 63.2 ms                                                | 59.8 ms: 1.06x faster                                               |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                              |
| logging_simple          | 6.06 us                                                | 5.78 us: 1.05x faster                                               |
| sympy_expand            | 472 ms                                                 | 451 ms: 1.05x faster                                                |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.05x faster                                               |
| telco                   | 6.62 ms                                                | 6.35 ms: 1.04x faster                                               |
| 2to3                    | 257 ms                                                 | 247 ms: 1.04x faster                                                |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                               |
| pprint_safe_repr        | 691 ms                                                 | 662 ms: 1.04x faster                                                |
| pyflate                 | 417 ms                                                 | 401 ms: 1.04x faster                                                |
| float                   | 76.3 ms                                                | 73.4 ms: 1.04x faster                                               |
| coverage                | 101 ms                                                 | 96.9 ms: 1.04x faster                                               |
| raytrace                | 290 ms                                                 | 280 ms: 1.04x faster                                                |
| pidigits                | 199 ms                                                 | 192 ms: 1.04x faster                                                |
| dulwich_log             | 63.9 ms                                                | 61.6 ms: 1.04x faster                                               |
| chaos                   | 68.6 ms                                                | 66.2 ms: 1.04x faster                                               |
| bench_thread_pool       | 810 us                                                 | 782 us: 1.04x faster                                                |
| docutils                | 2.60 sec                                               | 2.51 sec: 1.03x faster                                              |
| sympy_integrate         | 20.9 ms                                                | 20.2 ms: 1.03x faster                                               |
| tornado_http            | 96.6 ms                                                | 93.8 ms: 1.03x faster                                               |
| nbody                   | 95.0 ms                                                | 92.2 ms: 1.03x faster                                               |
| xml_etree_iterparse     | 103 ms                                                 | 99.7 ms: 1.03x faster                                               |
| pathlib                 | 18.2 ms                                                | 17.6 ms: 1.03x faster                                               |
| sympy_str               | 287 ms                                                 | 279 ms: 1.03x faster                                                |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.03x faster                                                |
| logging_format          | 6.62 us                                                | 6.46 us: 1.03x faster                                               |
| sqlalchemy_imperative   | 18.0 ms                                                | 17.6 ms: 1.02x faster                                               |
| chameleon               | 6.41 ms                                                | 6.26 ms: 1.02x faster                                               |
| sqlalchemy_declarative  | 139 ms                                                 | 136 ms: 1.02x faster                                                |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                               |
| crypto_pyaes            | 73.9 ms                                                | 72.4 ms: 1.02x faster                                               |
| deepcopy_reduce         | 2.97 us                                                | 2.92 us: 1.02x faster                                               |
| async_tree_cpu_io_mixed | 752 ms                                                 | 741 ms: 1.01x faster                                                |
| regex_dna               | 203 ms                                                 | 200 ms: 1.01x faster                                                |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.34 ms: 1.01x faster                                               |
| scimark_lu              | 107 ms                                                 | 106 ms: 1.01x faster                                                |
| mako                    | 9.85 ms                                                | 9.75 ms: 1.01x faster                                               |
| sympy_sum               | 166 ms                                                 | 165 ms: 1.01x faster                                                |
| mdp                     | 2.62 sec                                               | 2.60 sec: 1.01x faster                                              |
| thrift                  | 752 us                                                 | 756 us: 1.01x slower                                                |
| unpickle_list           | 4.95 us                                                | 4.98 us: 1.01x slower                                               |
| pickle_dict             | 31.4 us                                                | 31.7 us: 1.01x slower                                               |
| django_template         | 32.5 ms                                                | 32.8 ms: 1.01x slower                                               |
| xml_etree_process       | 53.8 ms                                                | 54.4 ms: 1.01x slower                                               |
| sqlglot_transpile       | 1.66 ms                                                | 1.68 ms: 1.01x slower                                               |
| sqlglot_parse           | 1.37 ms                                                | 1.39 ms: 1.02x slower                                               |
| pickle_list             | 4.17 us                                                | 4.27 us: 1.02x slower                                               |
| async_tree_memoization  | 625 ms                                                 | 646 ms: 1.03x slower                                                |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                               |
| xml_etree_generate      | 76.2 ms                                                | 79.4 ms: 1.04x slower                                               |
| unpickle                | 13.3 us                                                | 13.9 us: 1.05x slower                                               |
| regex_effbot            | 3.36 ms                                                | 3.63 ms: 1.08x slower                                               |
| python_startup          | 8.36 ms                                                | 9.06 ms: 1.08x slower                                               |
| sqlite_synth            | 2.49 us                                                | 2.73 us: 1.09x slower                                               |
| python_startup_no_site  | 5.96 ms                                                | 6.58 ms: 1.10x slower                                               |
| async_generators        | 359 ms                                                 | 430 ms: 1.20x slower                                                |
| Geometric mean          | (ref)                                                  | 1.04x faster                                                        |

Benchmark hidden because not significant (4): unpack_sequence, async_tree_none, async_tree_io, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230223-3.12.0a5+-d579d2e/bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
