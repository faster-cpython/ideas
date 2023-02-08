
# Results vs. 3.10.4

- fork: gvanrossum
- ref: call_family
- machine: linux-x86_64
- commit hash: 9595e01
- commit date: 2023-02-07
- overall geometric mean: 1.29x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 251 ms: 1.32x faster                                              |
| chameleon      | 8.86 ms                                                | 6.36 ms: 1.39x faster                                             |
| docutils       | 3.18 sec                                               | 2.50 sec: 1.27x faster                                            |
| html5lib       | 85.8 ms                                                | 61.1 ms: 1.40x faster                                             |
| tornado_http   | 128 ms                                                 | 93.7 ms: 1.37x faster                                             |
| Geometric mean | (ref)                                                  | 1.35x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 108 ms                                                 | 73.7 ms: 1.46x faster                                             |
| nbody          | 136 ms                                                 | 96.0 ms: 1.42x faster                                             |
| pidigits       | 190 ms                                                 | 197 ms: 1.04x slower                                              |
| Geometric mean | (ref)                                                  | 1.26x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                              |
| regex_v8       | 25.0 ms                                                | 21.7 ms: 1.15x faster                                             |
| regex_dna      | 214 ms                                                 | 205 ms: 1.04x faster                                              |
| regex_effbot   | 3.21 ms                                                | 3.62 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.10x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 286 us: 1.59x faster                                              |
| unpickle_pure_python | 297 us                                                 | 199 us: 1.49x faster                                              |
| json_dumps           | 13.5 ms                                                | 9.53 ms: 1.41x faster                                             |
| xml_etree_process    | 74.5 ms                                                | 53.2 ms: 1.40x faster                                             |
| xml_etree_generate   | 93.3 ms                                                | 77.4 ms: 1.21x faster                                             |
| json_loads           | 28.9 us                                                | 24.3 us: 1.19x faster                                             |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                              |
| pickle_list          | 4.50 us                                                | 4.14 us: 1.09x faster                                             |
| unpickle             | 14.3 us                                                | 13.3 us: 1.08x faster                                             |
| xml_etree_iterparse  | 110 ms                                                 | 103 ms: 1.07x faster                                              |
| pickle               | 10.1 us                                                | 10.4 us: 1.02x slower                                             |
| pickle_dict          | 28.3 us                                                | 31.6 us: 1.11x slower                                             |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                      |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.91 ms: 1.56x faster                                             |
| python_startup_no_site | 5.76 ms                                                | 6.47 ms: 1.12x slower                                             |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.7 ms: 1.48x faster                                             |
| mako            | 14.3 ms                                                | 9.92 ms: 1.44x faster                                             |
| django_template | 46.3 ms                                                | 32.6 ms: 1.42x faster                                             |
| genshi_xml      | 63.6 ms                                                | 46.5 ms: 1.37x faster                                             |
| Geometric mean  | (ref)                                                  | 1.42x faster                                                      |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.16 ms: 2.34x faster                                             |
| logging_silent          | 173 ns                                                 | 93.3 ns: 1.86x faster                                             |
| scimark_sor             | 193 ms                                                 | 108 ms: 1.79x faster                                              |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                              |
| richards                | 71.4 ms                                                | 42.2 ms: 1.69x faster                                             |
| pyflate                 | 675 ms                                                 | 404 ms: 1.67x faster                                              |
| raytrace                | 461 ms                                                 | 283 ms: 1.63x faster                                              |
| crypto_pyaes            | 118 ms                                                 | 72.6 ms: 1.62x faster                                             |
| pickle_pure_python      | 453 us                                                 | 286 us: 1.59x faster                                              |
| scimark_monte_carlo     | 105 ms                                                 | 66.2 ms: 1.58x faster                                             |
| hexiom                  | 9.42 ms                                                | 5.96 ms: 1.58x faster                                             |
| chaos                   | 104 ms                                                 | 66.1 ms: 1.57x faster                                             |
| python_startup          | 13.9 ms                                                | 8.91 ms: 1.56x faster                                             |
| spectral_norm           | 148 ms                                                 | 95.4 ms: 1.55x faster                                             |
| unpickle_pure_python    | 297 us                                                 | 199 us: 1.49x faster                                              |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.48x faster                                              |
| genshi_text             | 30.6 ms                                                | 20.7 ms: 1.48x faster                                             |
| float                   | 108 ms                                                 | 73.7 ms: 1.46x faster                                             |
| mako                    | 14.3 ms                                                | 9.92 ms: 1.44x faster                                             |
| unpack_sequence         | 59.5 ns                                                | 41.6 ns: 1.43x faster                                             |
| deepcopy_memo           | 50.0 us                                                | 35.0 us: 1.43x faster                                             |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.43x faster                                             |
| nbody                   | 136 ms                                                 | 96.0 ms: 1.42x faster                                             |
| django_template         | 46.3 ms                                                | 32.6 ms: 1.42x faster                                             |
| json_dumps              | 13.5 ms                                                | 9.53 ms: 1.41x faster                                             |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.41x faster                                             |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                            |
| html5lib                | 85.8 ms                                                | 61.1 ms: 1.40x faster                                             |
| thrift                  | 1.03 ms                                                | 735 us: 1.40x faster                                              |
| xml_etree_process       | 74.5 ms                                                | 53.2 ms: 1.40x faster                                             |
| chameleon               | 8.86 ms                                                | 6.36 ms: 1.39x faster                                             |
| logging_format          | 8.92 us                                                | 6.48 us: 1.38x faster                                             |
| tornado_http            | 128 ms                                                 | 93.7 ms: 1.37x faster                                             |
| logging_simple          | 8.06 us                                                | 5.89 us: 1.37x faster                                             |
| pprint_safe_repr        | 943 ms                                                 | 689 ms: 1.37x faster                                              |
| async_tree_none         | 713 ms                                                 | 522 ms: 1.37x faster                                              |
| genshi_xml              | 63.6 ms                                                | 46.5 ms: 1.37x faster                                             |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                              |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.04 ms: 1.36x faster                                             |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.35x faster                                            |
| fannkuch                | 477 ms                                                 | 355 ms: 1.34x faster                                              |
| scimark_fft             | 414 ms                                                 | 309 ms: 1.34x faster                                              |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.34x faster                                             |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                             |
| 2to3                    | 332 ms                                                 | 251 ms: 1.32x faster                                              |
| async_tree_memoization  | 854 ms                                                 | 647 ms: 1.32x faster                                              |
| pycparser               | 1.51 sec                                               | 1.15 sec: 1.31x faster                                            |
| coroutines              | 31.7 ms                                                | 24.5 ms: 1.29x faster                                             |
| sqlglot_normalize       | 135 ms                                                 | 105 ms: 1.28x faster                                              |
| deepcopy                | 429 us                                                 | 336 us: 1.28x faster                                              |
| docutils                | 3.18 sec                                               | 2.50 sec: 1.27x faster                                            |
| sqlglot_optimize        | 65.3 ms                                                | 51.4 ms: 1.27x faster                                             |
| deepcopy_reduce         | 3.75 us                                                | 2.98 us: 1.26x faster                                             |
| async_tree_cpu_io_mixed | 949 ms                                                 | 757 ms: 1.25x faster                                              |
| async_generators        | 428 ms                                                 | 347 ms: 1.23x faster                                              |
| nqueens                 | 99.3 ms                                                | 81.0 ms: 1.23x faster                                             |
| sympy_integrate         | 23.9 ms                                                | 19.7 ms: 1.21x faster                                             |
| bench_thread_pool       | 943 us                                                 | 781 us: 1.21x faster                                              |
| xml_etree_generate      | 93.3 ms                                                | 77.4 ms: 1.21x faster                                             |
| sympy_str               | 324 ms                                                 | 270 ms: 1.20x faster                                              |
| dulwich_log             | 75.5 ms                                                | 63.0 ms: 1.20x faster                                             |
| sqlalchemy_declarative  | 165 ms                                                 | 138 ms: 1.20x faster                                              |
| json_loads              | 28.9 us                                                | 24.3 us: 1.19x faster                                             |
| sympy_expand            | 537 ms                                                 | 454 ms: 1.18x faster                                              |
| sympy_sum               | 183 ms                                                 | 156 ms: 1.18x faster                                              |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.9 ms: 1.18x faster                                             |
| regex_v8                | 25.0 ms                                                | 21.7 ms: 1.15x faster                                             |
| json                    | 5.35 ms                                                | 4.70 ms: 1.14x faster                                             |
| sqlite_synth            | 2.90 us                                                | 2.58 us: 1.13x faster                                             |
| pathlib                 | 20.0 ms                                                | 18.0 ms: 1.11x faster                                             |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                              |
| mdp                     | 2.82 sec                                               | 2.59 sec: 1.09x faster                                            |
| pickle_list             | 4.50 us                                                | 4.14 us: 1.09x faster                                             |
| unpickle                | 14.3 us                                                | 13.3 us: 1.08x faster                                             |
| xml_etree_iterparse     | 110 ms                                                 | 103 ms: 1.07x faster                                              |
| meteor_contest          | 114 ms                                                 | 108 ms: 1.06x faster                                              |
| regex_dna               | 214 ms                                                 | 205 ms: 1.04x faster                                              |
| telco                   | 6.68 ms                                                | 6.45 ms: 1.04x faster                                             |
| pickle                  | 10.1 us                                                | 10.4 us: 1.02x slower                                             |
| pidigits                | 190 ms                                                 | 197 ms: 1.04x slower                                              |
| pickle_dict             | 28.3 us                                                | 31.6 us: 1.11x slower                                             |
| python_startup_no_site  | 5.76 ms                                                | 6.47 ms: 1.12x slower                                             |
| regex_effbot            | 3.21 ms                                                | 3.62 ms: 1.13x slower                                             |
| coverage                | 75.3 ms                                                | 95.6 ms: 1.27x slower                                             |
| Geometric mean          | (ref)                                                  | 1.29x faster                                                      |

Benchmark hidden because not significant (3): generators, bench_mp_pool, unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (5) of public/results/bm-20230207-3.12.0a5+-9595e01/bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5+-9595e01.json: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
