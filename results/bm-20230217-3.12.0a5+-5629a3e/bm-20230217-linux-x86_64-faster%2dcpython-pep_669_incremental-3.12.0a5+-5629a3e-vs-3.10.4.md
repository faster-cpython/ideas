
# Results vs. 3.10.4

- fork: faster-cpython
- ref: pep_669_incremental
- machine: linux-x86_64
- commit hash: 5629a3e
- commit date: 2023-02-17
- overall geometric mean: 1.32x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 244 ms: 1.36x faster                                                            |
| chameleon      | 8.86 ms                                                | 6.33 ms: 1.40x faster                                                           |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                                          |
| html5lib       | 85.8 ms                                                | 59.7 ms: 1.44x faster                                                           |
| tornado_http   | 128 ms                                                 | 93.3 ms: 1.37x faster                                                           |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 72.4 ms: 1.49x faster                                                           |
| nbody          | 136 ms                                                 | 92.4 ms: 1.47x faster                                                           |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 125 ms: 1.39x faster                                                            |
| regex_v8       | 25.0 ms                                                | 22.5 ms: 1.11x faster                                                           |
| regex_dna      | 214 ms                                                 | 205 ms: 1.04x faster                                                            |
| regex_effbot   | 3.21 ms                                                | 3.65 ms: 1.14x slower                                                           |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 279 us: 1.63x faster                                                            |
| unpickle_pure_python | 297 us                                                 | 193 us: 1.53x faster                                                            |
| json_dumps           | 13.5 ms                                                | 9.37 ms: 1.44x faster                                                           |
| xml_etree_process    | 74.5 ms                                                | 55.0 ms: 1.35x faster                                                           |
| json_loads           | 28.9 us                                                | 23.7 us: 1.22x faster                                                           |
| xml_etree_generate   | 93.3 ms                                                | 80.3 ms: 1.16x faster                                                           |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                                            |
| xml_etree_iterparse  | 110 ms                                                 | 100 ms: 1.10x faster                                                            |
| pickle_list          | 4.50 us                                                | 4.25 us: 1.06x faster                                                           |
| unpickle             | 14.3 us                                                | 13.7 us: 1.04x faster                                                           |
| unpickle_list        | 4.99 us                                                | 5.08 us: 1.02x slower                                                           |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                                           |
| pickle_dict          | 28.3 us                                                | 30.8 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.18x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.97 ms: 1.55x faster                                                           |
| python_startup_no_site | 5.76 ms                                                | 6.52 ms: 1.13x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.6 ms: 1.49x faster                                                           |
| mako            | 14.3 ms                                                | 9.76 ms: 1.46x faster                                                           |
| django_template | 46.3 ms                                                | 33.1 ms: 1.40x faster                                                           |
| genshi_xml      | 63.6 ms                                                | 46.0 ms: 1.38x faster                                                           |
| Geometric mean  | (ref)                                                  | 1.43x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 30.8 ms: 2.46x faster                                                           |
| deltablue               | 7.39 ms                                                | 3.13 ms: 2.36x faster                                                           |
| logging_silent          | 173 ns                                                 | 93.8 ns: 1.85x faster                                                           |
| scimark_sor             | 193 ms                                                 | 106 ms: 1.83x faster                                                            |
| richards                | 71.4 ms                                                | 41.9 ms: 1.70x faster                                                           |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                                            |
| pyflate                 | 675 ms                                                 | 401 ms: 1.69x faster                                                            |
| raytrace                | 461 ms                                                 | 280 ms: 1.64x faster                                                            |
| pickle_pure_python      | 453 us                                                 | 279 us: 1.63x faster                                                            |
| crypto_pyaes            | 118 ms                                                 | 72.6 ms: 1.62x faster                                                           |
| chaos                   | 104 ms                                                 | 64.5 ms: 1.61x faster                                                           |
| scimark_monte_carlo     | 105 ms                                                 | 65.2 ms: 1.61x faster                                                           |
| spectral_norm           | 148 ms                                                 | 92.7 ms: 1.60x faster                                                           |
| hexiom                  | 9.42 ms                                                | 5.99 ms: 1.57x faster                                                           |
| python_startup          | 13.9 ms                                                | 8.97 ms: 1.55x faster                                                           |
| unpickle_pure_python    | 297 us                                                 | 193 us: 1.53x faster                                                            |
| coroutines              | 31.7 ms                                                | 21.1 ms: 1.50x faster                                                           |
| deepcopy_memo           | 50.0 us                                                | 33.4 us: 1.50x faster                                                           |
| genshi_text             | 30.6 ms                                                | 20.6 ms: 1.49x faster                                                           |
| float                   | 108 ms                                                 | 72.4 ms: 1.49x faster                                                           |
| nbody                   | 136 ms                                                 | 92.4 ms: 1.47x faster                                                           |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.47x faster                                                            |
| mako                    | 14.3 ms                                                | 9.76 ms: 1.46x faster                                                           |
| sqlglot_parse           | 2.04 ms                                                | 1.41 ms: 1.45x faster                                                           |
| json_dumps              | 13.5 ms                                                | 9.37 ms: 1.44x faster                                                           |
| html5lib                | 85.8 ms                                                | 59.7 ms: 1.44x faster                                                           |
| pprint_pformat          | 1.97 sec                                               | 1.38 sec: 1.43x faster                                                          |
| sqlglot_transpile       | 2.42 ms                                                | 1.69 ms: 1.43x faster                                                           |
| logging_format          | 8.92 us                                                | 6.33 us: 1.41x faster                                                           |
| logging_simple          | 8.06 us                                                | 5.72 us: 1.41x faster                                                           |
| pprint_safe_repr        | 943 ms                                                 | 671 ms: 1.40x faster                                                            |
| unpack_sequence         | 59.5 ns                                                | 42.4 ns: 1.40x faster                                                           |
| chameleon               | 8.86 ms                                                | 6.33 ms: 1.40x faster                                                           |
| django_template         | 46.3 ms                                                | 33.1 ms: 1.40x faster                                                           |
| regex_compile           | 174 ms                                                 | 125 ms: 1.39x faster                                                            |
| genshi_xml              | 63.6 ms                                                | 46.0 ms: 1.38x faster                                                           |
| async_tree_none         | 713 ms                                                 | 518 ms: 1.38x faster                                                            |
| tornado_http            | 128 ms                                                 | 93.3 ms: 1.37x faster                                                           |
| async_tree_io           | 1.78 sec                                               | 1.29 sec: 1.37x faster                                                          |
| 2to3                    | 332 ms                                                 | 244 ms: 1.36x faster                                                            |
| scimark_fft             | 414 ms                                                 | 305 ms: 1.36x faster                                                            |
| thrift                  | 1.03 ms                                                | 761 us: 1.35x faster                                                            |
| xml_etree_process       | 74.5 ms                                                | 55.0 ms: 1.35x faster                                                           |
| gunicorn                | 1.43 ms                                                | 1.06 ms: 1.35x faster                                                           |
| fannkuch                | 477 ms                                                 | 356 ms: 1.34x faster                                                            |
| aiohttp                 | 1.34 ms                                                | 1000 us: 1.34x faster                                                           |
| pycparser               | 1.51 sec                                               | 1.13 sec: 1.34x faster                                                          |
| deepcopy                | 429 us                                                 | 325 us: 1.32x faster                                                            |
| sqlglot_normalize       | 135 ms                                                 | 103 ms: 1.31x faster                                                            |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.20 ms: 1.31x faster                                                           |
| async_tree_memoization  | 854 ms                                                 | 655 ms: 1.30x faster                                                            |
| deepcopy_reduce         | 3.75 us                                                | 2.90 us: 1.29x faster                                                           |
| nqueens                 | 99.3 ms                                                | 76.9 ms: 1.29x faster                                                           |
| sqlglot_optimize        | 65.3 ms                                                | 50.6 ms: 1.29x faster                                                           |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                                          |
| async_tree_cpu_io_mixed | 949 ms                                                 | 750 ms: 1.26x faster                                                            |
| dulwich_log             | 75.5 ms                                                | 61.2 ms: 1.23x faster                                                           |
| sqlalchemy_declarative  | 165 ms                                                 | 135 ms: 1.23x faster                                                            |
| sympy_integrate         | 23.9 ms                                                | 19.5 ms: 1.23x faster                                                           |
| sympy_str               | 324 ms                                                 | 265 ms: 1.22x faster                                                            |
| json_loads              | 28.9 us                                                | 23.7 us: 1.22x faster                                                           |
| bench_thread_pool       | 943 us                                                 | 779 us: 1.21x faster                                                            |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.6 ms: 1.20x faster                                                           |
| sympy_expand            | 537 ms                                                 | 449 ms: 1.20x faster                                                            |
| sympy_sum               | 183 ms                                                 | 155 ms: 1.18x faster                                                            |
| xml_etree_generate      | 93.3 ms                                                | 80.3 ms: 1.16x faster                                                           |
| json                    | 5.35 ms                                                | 4.62 ms: 1.16x faster                                                           |
| mdp                     | 2.82 sec                                               | 2.46 sec: 1.15x faster                                                          |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                                           |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.11x faster                                                            |
| regex_v8                | 25.0 ms                                                | 22.5 ms: 1.11x faster                                                           |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                                            |
| xml_etree_iterparse     | 110 ms                                                 | 100 ms: 1.10x faster                                                            |
| pathlib                 | 20.0 ms                                                | 18.2 ms: 1.10x faster                                                           |
| pickle_list             | 4.50 us                                                | 4.25 us: 1.06x faster                                                           |
| telco                   | 6.68 ms                                                | 6.38 ms: 1.05x faster                                                           |
| regex_dna               | 214 ms                                                 | 205 ms: 1.04x faster                                                            |
| unpickle                | 14.3 us                                                | 13.7 us: 1.04x faster                                                           |
| async_generators        | 428 ms                                                 | 422 ms: 1.01x faster                                                            |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                                            |
| unpickle_list           | 4.99 us                                                | 5.08 us: 1.02x slower                                                           |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                                           |
| pickle_dict             | 28.3 us                                                | 30.8 us: 1.09x slower                                                           |
| python_startup_no_site  | 5.76 ms                                                | 6.52 ms: 1.13x slower                                                           |
| regex_effbot            | 3.21 ms                                                | 3.65 ms: 1.14x slower                                                           |
| coverage                | 75.3 ms                                                | 99.2 ms: 1.32x slower                                                           |
| Geometric mean          | (ref)                                                  | 1.32x faster                                                                    |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230217-3.12.0a5+-5629a3e/bm-20230217-linux-x86_64-faster%2dcpython-pep_669_incremental-3.12.0a5+-5629a3e.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
