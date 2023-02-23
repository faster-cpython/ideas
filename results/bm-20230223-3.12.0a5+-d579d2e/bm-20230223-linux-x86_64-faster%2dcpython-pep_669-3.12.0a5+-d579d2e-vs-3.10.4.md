
# Results vs. 3.10.4

- fork: faster-cpython
- ref: pep_669
- machine: linux-x86_64
- commit hash: d579d2e
- commit date: 2023-02-23
- overall geometric mean: 1.31x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 247 ms: 1.35x faster                                                |
| chameleon      | 8.86 ms                                                | 6.26 ms: 1.41x faster                                               |
| docutils       | 3.18 sec                                               | 2.51 sec: 1.27x faster                                              |
| html5lib       | 85.8 ms                                                | 59.8 ms: 1.43x faster                                               |
| tornado_http   | 128 ms                                                 | 93.8 ms: 1.37x faster                                               |
| Geometric mean | (ref)                                                  | 1.36x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 136 ms                                                 | 92.2 ms: 1.48x faster                                               |
| float          | 108 ms                                                 | 73.4 ms: 1.47x faster                                               |
| pidigits       | 190 ms                                                 | 192 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                  | 1.29x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 129 ms: 1.35x faster                                                |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.14x faster                                               |
| regex_dna      | 214 ms                                                 | 200 ms: 1.07x faster                                                |
| regex_effbot   | 3.21 ms                                                | 3.63 ms: 1.13x slower                                               |
| Geometric mean | (ref)                                                  | 1.10x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 277 us: 1.63x faster                                                |
| unpickle_pure_python | 297 us                                                 | 194 us: 1.53x faster                                                |
| json_dumps           | 13.5 ms                                                | 9.40 ms: 1.43x faster                                               |
| xml_etree_process    | 74.5 ms                                                | 54.4 ms: 1.37x faster                                               |
| json_loads           | 28.9 us                                                | 23.7 us: 1.22x faster                                               |
| xml_etree_generate   | 93.3 ms                                                | 79.4 ms: 1.18x faster                                               |
| xml_etree_iterparse  | 110 ms                                                 | 99.7 ms: 1.11x faster                                               |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                                |
| pickle_list          | 4.50 us                                                | 4.27 us: 1.05x faster                                               |
| unpickle             | 14.3 us                                                | 13.9 us: 1.03x faster                                               |
| pickle_dict          | 28.3 us                                                | 31.7 us: 1.12x slower                                               |
| Geometric mean       | (ref)                                                  | 1.18x faster                                                        |

Benchmark hidden because not significant (2): unpickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.06 ms: 1.54x faster                                               |
| python_startup_no_site | 5.76 ms                                                | 6.58 ms: 1.14x slower                                               |
| Geometric mean         | (ref)                                                  | 1.16x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.5 ms: 1.50x faster                                               |
| mako            | 14.3 ms                                                | 9.75 ms: 1.46x faster                                               |
| django_template | 46.3 ms                                                | 32.8 ms: 1.41x faster                                               |
| genshi_xml      | 63.6 ms                                                | 45.9 ms: 1.38x faster                                               |
| Geometric mean  | (ref)                                                  | 1.44x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 31.6 ms: 2.40x faster                                               |
| deltablue               | 7.39 ms                                                | 3.14 ms: 2.36x faster                                               |
| logging_silent          | 173 ns                                                 | 91.7 ns: 1.89x faster                                               |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.86x faster                                                |
| go                      | 226 ms                                                 | 130 ms: 1.74x faster                                                |
| richards                | 71.4 ms                                                | 41.6 ms: 1.71x faster                                               |
| pyflate                 | 675 ms                                                 | 401 ms: 1.69x faster                                                |
| raytrace                | 461 ms                                                 | 280 ms: 1.65x faster                                                |
| pickle_pure_python      | 453 us                                                 | 277 us: 1.63x faster                                                |
| scimark_monte_carlo     | 105 ms                                                 | 64.2 ms: 1.63x faster                                               |
| crypto_pyaes            | 118 ms                                                 | 72.4 ms: 1.62x faster                                               |
| chaos                   | 104 ms                                                 | 66.2 ms: 1.57x faster                                               |
| hexiom                  | 9.42 ms                                                | 6.00 ms: 1.57x faster                                               |
| spectral_norm           | 148 ms                                                 | 94.6 ms: 1.57x faster                                               |
| python_startup          | 13.9 ms                                                | 9.06 ms: 1.54x faster                                               |
| unpickle_pure_python    | 297 us                                                 | 194 us: 1.53x faster                                                |
| deepcopy_memo           | 50.0 us                                                | 33.1 us: 1.51x faster                                               |
| genshi_text             | 30.6 ms                                                | 20.5 ms: 1.50x faster                                               |
| scimark_lu              | 158 ms                                                 | 106 ms: 1.49x faster                                                |
| nbody                   | 136 ms                                                 | 92.2 ms: 1.48x faster                                               |
| float                   | 108 ms                                                 | 73.4 ms: 1.47x faster                                               |
| mako                    | 14.3 ms                                                | 9.75 ms: 1.46x faster                                               |
| sqlglot_parse           | 2.04 ms                                                | 1.39 ms: 1.46x faster                                               |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                              |
| sqlglot_transpile       | 2.42 ms                                                | 1.68 ms: 1.44x faster                                               |
| coroutines              | 31.7 ms                                                | 22.0 ms: 1.44x faster                                               |
| json_dumps              | 13.5 ms                                                | 9.40 ms: 1.43x faster                                               |
| html5lib                | 85.8 ms                                                | 59.8 ms: 1.43x faster                                               |
| pprint_safe_repr        | 943 ms                                                 | 662 ms: 1.42x faster                                                |
| chameleon               | 8.86 ms                                                | 6.26 ms: 1.41x faster                                               |
| django_template         | 46.3 ms                                                | 32.8 ms: 1.41x faster                                               |
| logging_simple          | 8.06 us                                                | 5.78 us: 1.39x faster                                               |
| genshi_xml              | 63.6 ms                                                | 45.9 ms: 1.38x faster                                               |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.38x faster                                              |
| logging_format          | 8.92 us                                                | 6.46 us: 1.38x faster                                               |
| unpack_sequence         | 59.5 ns                                                | 43.1 ns: 1.38x faster                                               |
| tornado_http            | 128 ms                                                 | 93.8 ms: 1.37x faster                                               |
| scimark_fft             | 414 ms                                                 | 302 ms: 1.37x faster                                                |
| xml_etree_process       | 74.5 ms                                                | 54.4 ms: 1.37x faster                                               |
| thrift                  | 1.03 ms                                                | 756 us: 1.36x faster                                                |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.36x faster                                              |
| async_tree_none         | 713 ms                                                 | 526 ms: 1.35x faster                                                |
| regex_compile           | 174 ms                                                 | 129 ms: 1.35x faster                                                |
| 2to3                    | 332 ms                                                 | 247 ms: 1.35x faster                                                |
| fannkuch                | 477 ms                                                 | 357 ms: 1.34x faster                                                |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.34x faster                                               |
| deepcopy                | 429 us                                                 | 323 us: 1.33x faster                                                |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                               |
| sqlglot_normalize       | 135 ms                                                 | 102 ms: 1.33x faster                                                |
| async_tree_memoization  | 854 ms                                                 | 646 ms: 1.32x faster                                                |
| sqlglot_optimize        | 65.3 ms                                                | 50.1 ms: 1.30x faster                                               |
| deepcopy_reduce         | 3.75 us                                                | 2.92 us: 1.28x faster                                               |
| async_tree_cpu_io_mixed | 949 ms                                                 | 741 ms: 1.28x faster                                                |
| nqueens                 | 99.3 ms                                                | 78.4 ms: 1.27x faster                                               |
| docutils                | 3.18 sec                                               | 2.51 sec: 1.27x faster                                              |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.34 ms: 1.26x faster                                               |
| dulwich_log             | 75.5 ms                                                | 61.6 ms: 1.22x faster                                               |
| sqlalchemy_declarative  | 165 ms                                                 | 136 ms: 1.22x faster                                                |
| json_loads              | 28.9 us                                                | 23.7 us: 1.22x faster                                               |
| bench_thread_pool       | 943 us                                                 | 782 us: 1.21x faster                                                |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.6 ms: 1.20x faster                                               |
| sympy_expand            | 537 ms                                                 | 451 ms: 1.19x faster                                                |
| sympy_integrate         | 23.9 ms                                                | 20.2 ms: 1.18x faster                                               |
| xml_etree_generate      | 93.3 ms                                                | 79.4 ms: 1.18x faster                                               |
| json                    | 5.35 ms                                                | 4.58 ms: 1.17x faster                                               |
| sympy_str               | 324 ms                                                 | 279 ms: 1.16x faster                                                |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.14x faster                                               |
| pathlib                 | 20.0 ms                                                | 17.6 ms: 1.13x faster                                               |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.12x faster                                                |
| sympy_sum               | 183 ms                                                 | 165 ms: 1.11x faster                                                |
| xml_etree_iterparse     | 110 ms                                                 | 99.7 ms: 1.11x faster                                               |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                                |
| mdp                     | 2.82 sec                                               | 2.60 sec: 1.08x faster                                              |
| regex_dna               | 214 ms                                                 | 200 ms: 1.07x faster                                                |
| sqlite_synth            | 2.90 us                                                | 2.73 us: 1.07x faster                                               |
| telco                   | 6.68 ms                                                | 6.35 ms: 1.05x faster                                               |
| pickle_list             | 4.50 us                                                | 4.27 us: 1.05x faster                                               |
| unpickle                | 14.3 us                                                | 13.9 us: 1.03x faster                                               |
| async_generators        | 428 ms                                                 | 430 ms: 1.00x slower                                                |
| pidigits                | 190 ms                                                 | 192 ms: 1.01x slower                                                |
| pickle_dict             | 28.3 us                                                | 31.7 us: 1.12x slower                                               |
| regex_effbot            | 3.21 ms                                                | 3.63 ms: 1.13x slower                                               |
| python_startup_no_site  | 5.76 ms                                                | 6.58 ms: 1.14x slower                                               |
| coverage                | 75.3 ms                                                | 96.9 ms: 1.29x slower                                               |
| Geometric mean          | (ref)                                                  | 1.31x faster                                                        |

Benchmark hidden because not significant (3): unpickle_list, bench_mp_pool, pickle
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230223-3.12.0a5+-d579d2e/bm-20230223-linux-x86_64-faster%2dcpython-pep_669-3.12.0a5+-d579d2e.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
