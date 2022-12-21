| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221119-linux-amd64-python-main-3.12.0a3+-b0e1f9c |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 245 ms: 1.36x faster                                  |
| chameleon               | 8.76 ms                                            | 6.49 ms: 1.35x faster                                 |
| chaos                   | 107 ms                                             | 66.0 ms: 1.62x faster                                 |
| crypto_pyaes            | 116 ms                                             | 74.3 ms: 1.57x faster                                 |
| deltablue               | 7.32 ms                                            | 3.23 ms: 2.27x faster                                 |
| django_template         | 45.7 ms                                            | 32.6 ms: 1.40x faster                                 |
| dulwich_log             | 75.2 ms                                            | 60.6 ms: 1.24x faster                                 |
| fannkuch                | 483 ms                                             | 369 ms: 1.31x faster                                  |
| float                   | 107 ms                                             | 71.6 ms: 1.50x faster                                 |
| genshi_text             | 30.6 ms                                            | 20.4 ms: 1.50x faster                                 |
| genshi_xml              | 64.1 ms                                            | 46.2 ms: 1.39x faster                                 |
| go                      | 227 ms                                             | 135 ms: 1.67x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.21 ms: 1.50x faster                                 |
| html5lib                | 85.1 ms                                            | 59.1 ms: 1.44x faster                                 |
| json                    | 5.55 ms                                            | 4.67 ms: 1.19x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.42 ms: 1.40x faster                                 |
| json_loads              | 31.1 us                                            | 24.2 us: 1.29x faster                                 |
| logging_format          | 8.78 us                                            | 6.35 us: 1.38x faster                                 |
| logging_silent          | 168 ns                                             | 91.1 ns: 1.84x faster                                 |
| logging_simple          | 8.07 us                                            | 5.77 us: 1.40x faster                                 |
| mako                    | 14.7 ms                                            | 9.94 ms: 1.48x faster                                 |
| meteor_contest          | 114 ms                                             | 104 ms: 1.10x faster                                  |
| nbody                   | 135 ms                                             | 94.1 ms: 1.43x faster                                 |
| nqueens                 | 98.4 ms                                            | 81.5 ms: 1.21x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.5 ms: 1.15x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.0 us: 1.14x slower                                 |
| pickle_list             | 4.40 us                                            | 4.11 us: 1.07x faster                                 |
| pickle_pure_python      | 449 us                                             | 283 us: 1.58x faster                                  |
| pidigits                | 190 ms                                             | 192 ms: 1.01x slower                                  |
| pycparser               | 1.52 sec                                           | 1.12 sec: 1.36x faster                                |
| pyflate                 | 664 ms                                             | 403 ms: 1.65x faster                                  |
| python_startup          | 9.21 ms                                            | 8.51 ms: 1.08x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.25 ms: 1.05x slower                                 |
| raytrace                | 463 ms                                             | 278 ms: 1.66x faster                                  |
| regex_compile           | 178 ms                                             | 127 ms: 1.40x faster                                  |
| regex_dna               | 214 ms                                             | 213 ms: 1.01x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.77 ms: 1.16x slower                                 |
| regex_v8                | 25.7 ms                                            | 22.2 ms: 1.16x faster                                 |
| richards                | 68.9 ms                                            | 41.6 ms: 1.66x faster                                 |
| scimark_fft             | 419 ms                                             | 303 ms: 1.38x faster                                  |
| scimark_lu              | 160 ms                                             | 104 ms: 1.54x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 64.0 ms: 1.67x faster                                 |
| scimark_sor             | 196 ms                                             | 104 ms: 1.88x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 3.96 ms: 1.37x faster                                 |
| spectral_norm           | 144 ms                                             | 97.6 ms: 1.47x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.64 us: 1.11x faster                                 |
| sympy_expand            | 538 ms                                             | 457 ms: 1.18x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.4 ms: 1.18x faster                                 |
| sympy_str               | 325 ms                                             | 283 ms: 1.15x faster                                  |
| sympy_sum               | 184 ms                                             | 165 ms: 1.12x faster                                  |
| telco                   | 6.60 ms                                            | 6.27 ms: 1.05x faster                                 |
| thrift                  | 1.01 ms                                            | 746 us: 1.36x faster                                  |
| tornado_http            | 127 ms                                             | 92.7 ms: 1.37x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 42.9 ns: 1.31x faster                                 |
| unpickle                | 14.4 us                                            | 13.6 us: 1.06x faster                                 |
| unpickle_list           | 4.90 us                                            | 5.10 us: 1.04x slower                                 |
| unpickle_pure_python    | 298 us                                             | 201 us: 1.48x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 76.4 ms: 1.21x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 103 ms: 1.07x faster                                  |
| xml_etree_parse         | 162 ms                                             | 148 ms: 1.09x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.9 ms: 1.37x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (1) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: pylint
Ignored benchmarks (20) of public/results/bm-20221119-python-main-3.12.0a3+-b0e1f9c/bm-20221119-linux-amd64-python-main-3.12.0a3+-b0e1f9c.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
