
# Results vs. 3.10.4

- fork: faster-cpython
- ref: pep_669
- machine: linux-x86_64
- commit hash: 662c16c
- commit date: 2023-03-25
- overall geometric mean: 1.32x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 247 ms: 1.36x faster                                                |
| chameleon      | 9.13 ms                                                             | 6.20 ms: 1.47x faster                                               |
| docutils       | 3.19 sec                                                            | 2.51 sec: 1.27x faster                                              |
| html5lib       | 86.4 ms                                                             | 60.5 ms: 1.43x faster                                               |
| tornado_http   | 129 ms                                                              | 90.0 ms: 1.43x faster                                               |
| Geometric mean | (ref)                                                               | 1.39x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 84.3 ms: 1.73x faster                                               |
| float          | 110 ms                                                              | 71.2 ms: 1.54x faster                                               |
| pidigits       | 190 ms                                                              | 188 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                               | 1.39x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 129 ms: 1.37x faster                                                |
| regex_v8       | 24.9 ms                                                             | 22.2 ms: 1.12x faster                                               |
| regex_dna      | 213 ms                                                              | 203 ms: 1.05x faster                                                |
| regex_effbot   | 3.22 ms                                                             | 3.47 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                               | 1.11x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 282 us: 1.62x faster                                                |
| unpickle_pure_python | 300 us                                                              | 197 us: 1.52x faster                                                |
| json_dumps           | 13.7 ms                                                             | 9.53 ms: 1.44x faster                                               |
| xml_etree_process    | 74.8 ms                                                             | 54.8 ms: 1.36x faster                                               |
| json_loads           | 29.3 us                                                             | 24.0 us: 1.22x faster                                               |
| xml_etree_generate   | 94.9 ms                                                             | 79.2 ms: 1.20x faster                                               |
| xml_etree_iterparse  | 111 ms                                                              | 99.1 ms: 1.12x faster                                               |
| pickle_list          | 4.73 us                                                             | 4.22 us: 1.12x faster                                               |
| xml_etree_parse      | 164 ms                                                              | 148 ms: 1.11x faster                                                |
| unpickle             | 15.0 us                                                             | 14.1 us: 1.06x faster                                               |
| pickle               | 10.2 us                                                             | 10.3 us: 1.01x slower                                               |
| pickle_dict          | 27.8 us                                                             | 30.6 us: 1.10x slower                                               |
| Geometric mean       | (ref)                                                               | 1.19x faster                                                        |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 8.86 ms: 1.60x faster                                               |
| python_startup_no_site | 5.80 ms                                                             | 6.57 ms: 1.13x slower                                               |
| Geometric mean         | (ref)                                                               | 1.19x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 9.85 ms: 1.50x faster                                               |
| genshi_text     | 30.4 ms                                                             | 20.4 ms: 1.49x faster                                               |
| django_template | 45.8 ms                                                             | 32.6 ms: 1.41x faster                                               |
| genshi_xml      | 64.3 ms                                                             | 46.0 ms: 1.40x faster                                               |
| Geometric mean  | (ref)                                                               | 1.45x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230325-linux-x86_64-faster%2dcpython-pep_669-3.12.0a6+-662c16c |
|-------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 27.5 ms: 2.75x faster                                               |
| deltablue               | 7.30 ms                                                             | 3.15 ms: 2.32x faster                                               |
| asyncio_tcp             | 922 ms                                                              | 501 ms: 1.84x faster                                                |
| scimark_sor             | 198 ms                                                              | 108 ms: 1.83x faster                                                |
| logging_silent          | 169 ns                                                              | 92.5 ns: 1.83x faster                                               |
| richards                | 74.2 ms                                                             | 42.4 ms: 1.75x faster                                               |
| nbody                   | 146 ms                                                              | 84.3 ms: 1.73x faster                                               |
| raytrace                | 470 ms                                                              | 278 ms: 1.69x faster                                                |
| spectral_norm           | 150 ms                                                              | 88.8 ms: 1.69x faster                                               |
| scimark_monte_carlo     | 109 ms                                                              | 65.2 ms: 1.66x faster                                               |
| pyflate                 | 671 ms                                                              | 406 ms: 1.65x faster                                                |
| go                      | 226 ms                                                              | 137 ms: 1.64x faster                                                |
| pickle_pure_python      | 457 us                                                              | 282 us: 1.62x faster                                                |
| hexiom                  | 9.50 ms                                                             | 5.90 ms: 1.61x faster                                               |
| crypto_pyaes            | 117 ms                                                              | 72.7 ms: 1.60x faster                                               |
| python_startup          | 14.1 ms                                                             | 8.86 ms: 1.60x faster                                               |
| chaos                   | 106 ms                                                              | 66.6 ms: 1.59x faster                                               |
| deepcopy_memo           | 51.8 us                                                             | 33.3 us: 1.56x faster                                               |
| float                   | 110 ms                                                              | 71.2 ms: 1.54x faster                                               |
| unpack_sequence         | 65.6 ns                                                             | 43.1 ns: 1.52x faster                                               |
| unpickle_pure_python    | 300 us                                                              | 197 us: 1.52x faster                                                |
| mako                    | 14.7 ms                                                             | 9.85 ms: 1.50x faster                                               |
| genshi_text             | 30.4 ms                                                             | 20.4 ms: 1.49x faster                                               |
| scimark_lu              | 160 ms                                                              | 108 ms: 1.49x faster                                                |
| sqlglot_parse           | 2.07 ms                                                             | 1.40 ms: 1.48x faster                                               |
| chameleon               | 9.13 ms                                                             | 6.20 ms: 1.47x faster                                               |
| sqlglot_transpile       | 2.45 ms                                                             | 1.68 ms: 1.46x faster                                               |
| logging_format          | 9.07 us                                                             | 6.23 us: 1.46x faster                                               |
| logging_simple          | 8.21 us                                                             | 5.68 us: 1.45x faster                                               |
| coroutines              | 31.8 ms                                                             | 22.1 ms: 1.44x faster                                               |
| json_dumps              | 13.7 ms                                                             | 9.53 ms: 1.44x faster                                               |
| pprint_pformat          | 1.98 sec                                                            | 1.38 sec: 1.44x faster                                              |
| tornado_http            | 129 ms                                                              | 90.0 ms: 1.43x faster                                               |
| html5lib                | 86.4 ms                                                             | 60.5 ms: 1.43x faster                                               |
| pprint_safe_repr        | 953 ms                                                              | 673 ms: 1.42x faster                                                |
| django_template         | 45.8 ms                                                             | 32.6 ms: 1.41x faster                                               |
| genshi_xml              | 64.3 ms                                                             | 46.0 ms: 1.40x faster                                               |
| async_tree_io           | 1.78 sec                                                            | 1.28 sec: 1.40x faster                                              |
| scimark_fft             | 425 ms                                                              | 306 ms: 1.39x faster                                                |
| async_tree_memoization  | 853 ms                                                              | 620 ms: 1.38x faster                                                |
| regex_compile           | 177 ms                                                              | 129 ms: 1.37x faster                                                |
| deepcopy                | 438 us                                                              | 319 us: 1.37x faster                                                |
| async_tree_none         | 713 ms                                                              | 520 ms: 1.37x faster                                                |
| xml_etree_process       | 74.8 ms                                                             | 54.8 ms: 1.36x faster                                               |
| aiohttp                 | 1.35 ms                                                             | 991 us: 1.36x faster                                                |
| 2to3                    | 336 ms                                                              | 247 ms: 1.36x faster                                                |
| pycparser               | 1.53 sec                                                            | 1.13 sec: 1.35x faster                                              |
| gunicorn                | 1.43 ms                                                             | 1.07 ms: 1.34x faster                                               |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.24 ms: 1.33x faster                                               |
| mypy2                   | 432 ms                                                              | 326 ms: 1.32x faster                                                |
| thrift                  | 1.04 ms                                                             | 784 us: 1.32x faster                                                |
| deepcopy_reduce         | 3.80 us                                                             | 2.90 us: 1.31x faster                                               |
| sqlglot_normalize       | 135 ms                                                              | 104 ms: 1.30x faster                                                |
| sqlglot_optimize        | 65.3 ms                                                             | 50.4 ms: 1.30x faster                                               |
| async_tree_cpu_io_mixed | 944 ms                                                              | 731 ms: 1.29x faster                                                |
| docutils                | 3.19 sec                                                            | 2.51 sec: 1.27x faster                                              |
| fannkuch                | 485 ms                                                              | 381 ms: 1.27x faster                                                |
| sqlalchemy_declarative  | 166 ms                                                              | 133 ms: 1.24x faster                                                |
| sqlalchemy_imperative   | 21.2 ms                                                             | 17.1 ms: 1.23x faster                                               |
| nqueens                 | 98.8 ms                                                             | 80.1 ms: 1.23x faster                                               |
| dulwich_log             | 76.3 ms                                                             | 62.1 ms: 1.23x faster                                               |
| bench_thread_pool       | 954 us                                                              | 779 us: 1.23x faster                                                |
| json_loads              | 29.3 us                                                             | 24.0 us: 1.22x faster                                               |
| sympy_integrate         | 24.3 ms                                                             | 20.0 ms: 1.21x faster                                               |
| sympy_expand            | 540 ms                                                              | 449 ms: 1.20x faster                                                |
| xml_etree_generate      | 94.9 ms                                                             | 79.2 ms: 1.20x faster                                               |
| sympy_str               | 328 ms                                                              | 277 ms: 1.18x faster                                                |
| json                    | 5.41 ms                                                             | 4.61 ms: 1.17x faster                                               |
| comprehensions          | 27.3 us                                                             | 23.3 us: 1.17x faster                                               |
| sympy_sum               | 185 ms                                                              | 162 ms: 1.14x faster                                                |
| sqlite_synth            | 2.97 us                                                             | 2.62 us: 1.14x faster                                               |
| pathlib                 | 19.8 ms                                                             | 17.4 ms: 1.13x faster                                               |
| djangocms               | 36.3 us                                                             | 32.1 us: 1.13x faster                                               |
| xml_etree_iterparse     | 111 ms                                                              | 99.1 ms: 1.12x faster                                               |
| regex_v8                | 24.9 ms                                                             | 22.2 ms: 1.12x faster                                               |
| pickle_list             | 4.73 us                                                             | 4.22 us: 1.12x faster                                               |
| create_gc_cycles        | 1.64 ms                                                             | 1.47 ms: 1.11x faster                                               |
| meteor_contest          | 115 ms                                                              | 103 ms: 1.11x faster                                                |
| mdp                     | 2.75 sec                                                            | 2.48 sec: 1.11x faster                                              |
| xml_etree_parse         | 164 ms                                                              | 148 ms: 1.11x faster                                                |
| unpickle                | 15.0 us                                                             | 14.1 us: 1.06x faster                                               |
| regex_dna               | 213 ms                                                              | 203 ms: 1.05x faster                                                |
| telco                   | 6.67 ms                                                             | 6.41 ms: 1.04x faster                                               |
| pidigits                | 190 ms                                                              | 188 ms: 1.01x faster                                                |
| pickle                  | 10.2 us                                                             | 10.3 us: 1.01x slower                                               |
| gc_traversal            | 3.53 ms                                                             | 3.64 ms: 1.03x slower                                               |
| regex_effbot            | 3.22 ms                                                             | 3.47 ms: 1.08x slower                                               |
| pickle_dict             | 27.8 us                                                             | 30.6 us: 1.10x slower                                               |
| dask                    | 437 ms                                                              | 490 ms: 1.12x slower                                                |
| python_startup_no_site  | 5.80 ms                                                             | 6.57 ms: 1.13x slower                                               |
| coverage                | 70.6 ms                                                             | 96.7 ms: 1.37x slower                                               |
| Geometric mean          | (ref)                                                               | 1.32x faster                                                        |

Benchmark hidden because not significant (3): bench_mp_pool, unpickle_list, async_generators
Ignored benchmarks (2) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: flaskblogging, pylint
