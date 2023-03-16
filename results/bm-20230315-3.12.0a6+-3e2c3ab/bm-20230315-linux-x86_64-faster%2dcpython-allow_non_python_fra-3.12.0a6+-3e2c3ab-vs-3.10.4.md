
# Results vs. 3.10.4

- fork: faster-cpython
- ref: allow_non_python_fra
- machine: linux-x86_64
- commit hash: 3e2c3ab
- commit date: 2023-03-15
- overall geometric mean: 1.29x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                                             |
| chameleon      | 8.86 ms                                                | 6.42 ms: 1.38x faster                                                            |
| docutils       | 3.18 sec                                               | 2.55 sec: 1.25x faster                                                           |
| html5lib       | 85.8 ms                                                | 62.1 ms: 1.38x faster                                                            |
| tornado_http   | 128 ms                                                 | 95.2 ms: 1.35x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 75.2 ms: 1.43x faster                                                            |
| nbody          | 136 ms                                                 | 95.6 ms: 1.43x faster                                                            |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 134 ms: 1.30x faster                                                             |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.14x faster                                                            |
| regex_dna      | 214 ms                                                 | 203 ms: 1.05x faster                                                             |
| regex_effbot   | 3.21 ms                                                | 3.36 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 286 us: 1.59x faster                                                             |
| unpickle_pure_python | 297 us                                                 | 201 us: 1.47x faster                                                             |
| json_dumps           | 13.5 ms                                                | 9.55 ms: 1.41x faster                                                            |
| xml_etree_process    | 74.5 ms                                                | 55.2 ms: 1.35x faster                                                            |
| json_loads           | 28.9 us                                                | 24.4 us: 1.18x faster                                                            |
| xml_etree_generate   | 93.3 ms                                                | 81.0 ms: 1.15x faster                                                            |
| xml_etree_iterparse  | 110 ms                                                 | 99.4 ms: 1.11x faster                                                            |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                                             |
| pickle_list          | 4.50 us                                                | 4.12 us: 1.09x faster                                                            |
| unpickle             | 14.3 us                                                | 13.8 us: 1.04x faster                                                            |
| pickle               | 10.1 us                                                | 10.2 us: 1.01x slower                                                            |
| unpickle_list        | 4.99 us                                                | 5.05 us: 1.01x slower                                                            |
| pickle_dict          | 28.3 us                                                | 31.1 us: 1.10x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.02 ms: 1.54x faster                                                            |
| python_startup_no_site | 5.76 ms                                                | 6.54 ms: 1.13x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.5 ms: 1.43x faster                                                            |
| mako            | 14.3 ms                                                | 10.0 ms: 1.42x faster                                                            |
| django_template | 46.3 ms                                                | 33.5 ms: 1.38x faster                                                            |
| genshi_xml      | 63.6 ms                                                | 47.7 ms: 1.33x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.3 ms: 2.58x faster                                                            |
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.30x faster                                                            |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.81x faster                                                             |
| logging_silent          | 173 ns                                                 | 96.1 ns: 1.80x faster                                                            |
| go                      | 226 ms                                                 | 137 ms: 1.66x faster                                                             |
| pyflate                 | 675 ms                                                 | 409 ms: 1.65x faster                                                             |
| richards                | 71.4 ms                                                | 44.0 ms: 1.62x faster                                                            |
| raytrace                | 461 ms                                                 | 287 ms: 1.61x faster                                                             |
| pickle_pure_python      | 453 us                                                 | 286 us: 1.59x faster                                                             |
| crypto_pyaes            | 118 ms                                                 | 74.2 ms: 1.58x faster                                                            |
| python_startup          | 13.9 ms                                                | 9.02 ms: 1.54x faster                                                            |
| scimark_monte_carlo     | 105 ms                                                 | 67.8 ms: 1.54x faster                                                            |
| chaos                   | 104 ms                                                 | 67.9 ms: 1.53x faster                                                            |
| spectral_norm           | 148 ms                                                 | 97.8 ms: 1.51x faster                                                            |
| hexiom                  | 9.42 ms                                                | 6.27 ms: 1.50x faster                                                            |
| unpickle_pure_python    | 297 us                                                 | 201 us: 1.47x faster                                                             |
| deepcopy_memo           | 50.0 us                                                | 34.4 us: 1.46x faster                                                            |
| float                   | 108 ms                                                 | 75.2 ms: 1.43x faster                                                            |
| genshi_text             | 30.6 ms                                                | 21.5 ms: 1.43x faster                                                            |
| nbody                   | 136 ms                                                 | 95.6 ms: 1.43x faster                                                            |
| mako                    | 14.3 ms                                                | 10.0 ms: 1.42x faster                                                            |
| sqlglot_parse           | 2.04 ms                                                | 1.44 ms: 1.42x faster                                                            |
| pprint_pformat          | 1.97 sec                                               | 1.39 sec: 1.42x faster                                                           |
| scimark_lu              | 158 ms                                                 | 112 ms: 1.41x faster                                                             |
| json_dumps              | 13.5 ms                                                | 9.55 ms: 1.41x faster                                                            |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.40x faster                                                            |
| logging_format          | 8.92 us                                                | 6.41 us: 1.39x faster                                                            |
| coroutines              | 31.7 ms                                                | 22.9 ms: 1.39x faster                                                            |
| django_template         | 46.3 ms                                                | 33.5 ms: 1.38x faster                                                            |
| html5lib                | 85.8 ms                                                | 62.1 ms: 1.38x faster                                                            |
| pprint_safe_repr        | 943 ms                                                 | 683 ms: 1.38x faster                                                             |
| chameleon               | 8.86 ms                                                | 6.42 ms: 1.38x faster                                                            |
| logging_simple          | 8.06 us                                                | 5.86 us: 1.37x faster                                                            |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.36x faster                                                           |
| unpack_sequence         | 59.5 ns                                                | 43.8 ns: 1.36x faster                                                            |
| async_tree_none         | 713 ms                                                 | 526 ms: 1.35x faster                                                             |
| xml_etree_process       | 74.5 ms                                                | 55.2 ms: 1.35x faster                                                            |
| tornado_http            | 128 ms                                                 | 95.2 ms: 1.35x faster                                                            |
| pycparser               | 1.51 sec                                               | 1.13 sec: 1.34x faster                                                           |
| genshi_xml              | 63.6 ms                                                | 47.7 ms: 1.33x faster                                                            |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                                            |
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                                             |
| gunicorn                | 1.43 ms                                                | 1.10 ms: 1.31x faster                                                            |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                                             |
| regex_compile           | 174 ms                                                 | 134 ms: 1.30x faster                                                             |
| scimark_fft             | 414 ms                                                 | 319 ms: 1.30x faster                                                             |
| thrift                  | 1.03 ms                                                | 796 us: 1.30x faster                                                             |
| async_tree_memoization  | 854 ms                                                 | 660 ms: 1.29x faster                                                             |
| fannkuch                | 477 ms                                                 | 371 ms: 1.29x faster                                                             |
| sqlglot_optimize        | 65.3 ms                                                | 50.8 ms: 1.29x faster                                                            |
| deepcopy                | 429 us                                                 | 335 us: 1.28x faster                                                             |
| async_tree_cpu_io_mixed | 949 ms                                                 | 745 ms: 1.27x faster                                                             |
| deepcopy_reduce         | 3.75 us                                                | 2.96 us: 1.27x faster                                                            |
| docutils                | 3.18 sec                                               | 2.55 sec: 1.25x faster                                                           |
| nqueens                 | 99.3 ms                                                | 81.1 ms: 1.22x faster                                                            |
| sqlalchemy_declarative  | 165 ms                                                 | 138 ms: 1.20x faster                                                             |
| bench_thread_pool       | 943 us                                                 | 793 us: 1.19x faster                                                             |
| dulwich_log             | 75.5 ms                                                | 63.8 ms: 1.18x faster                                                            |
| json_loads              | 28.9 us                                                | 24.4 us: 1.18x faster                                                            |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.68 ms: 1.17x faster                                                            |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.0 ms: 1.17x faster                                                            |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                                            |
| sympy_expand            | 537 ms                                                 | 462 ms: 1.16x faster                                                             |
| json                    | 5.35 ms                                                | 4.64 ms: 1.15x faster                                                            |
| xml_etree_generate      | 93.3 ms                                                | 81.0 ms: 1.15x faster                                                            |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.14x faster                                                            |
| sympy_str               | 324 ms                                                 | 285 ms: 1.14x faster                                                             |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.12x faster                                                            |
| xml_etree_iterparse     | 110 ms                                                 | 99.4 ms: 1.11x faster                                                            |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                                             |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.10x faster                                                             |
| sqlite_synth            | 2.90 us                                                | 2.65 us: 1.10x faster                                                            |
| pickle_list             | 4.50 us                                                | 4.12 us: 1.09x faster                                                            |
| sympy_sum               | 183 ms                                                 | 168 ms: 1.09x faster                                                             |
| mdp                     | 2.82 sec                                               | 2.63 sec: 1.07x faster                                                           |
| regex_dna               | 214 ms                                                 | 203 ms: 1.05x faster                                                             |
| unpickle                | 14.3 us                                                | 13.8 us: 1.04x faster                                                            |
| async_generators        | 428 ms                                                 | 413 ms: 1.04x faster                                                             |
| telco                   | 6.68 ms                                                | 6.52 ms: 1.02x faster                                                            |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                                             |
| pickle                  | 10.1 us                                                | 10.2 us: 1.01x slower                                                            |
| unpickle_list           | 4.99 us                                                | 5.05 us: 1.01x slower                                                            |
| regex_effbot            | 3.21 ms                                                | 3.36 ms: 1.05x slower                                                            |
| pickle_dict             | 28.3 us                                                | 31.1 us: 1.10x slower                                                            |
| python_startup_no_site  | 5.76 ms                                                | 6.54 ms: 1.13x slower                                                            |
| coverage                | 75.3 ms                                                | 93.6 ms: 1.24x slower                                                            |
| Geometric mean          | (ref)                                                  | 1.29x faster                                                                     |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230315-3.12.0a6+-3e2c3ab/bm-20230315-linux-x86_64-faster%2dcpython-allow_non_python_fra-3.12.0a6+-3e2c3ab.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
