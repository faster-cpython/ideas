| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221015-linux-amd64-python-main-3.12.0a1+-660f102 |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 249 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.71 ms: 1.31x faster                                 |
| chaos                   | 107 ms                                             | 66.1 ms: 1.62x faster                                 |
| crypto_pyaes            | 116 ms                                             | 75.2 ms: 1.55x faster                                 |
| deltablue               | 7.32 ms                                            | 3.31 ms: 2.21x faster                                 |
| django_template         | 45.7 ms                                            | 32.6 ms: 1.40x faster                                 |
| dulwich_log             | 75.2 ms                                            | 60.9 ms: 1.24x faster                                 |
| fannkuch                | 483 ms                                             | 368 ms: 1.31x faster                                  |
| float                   | 107 ms                                             | 72.2 ms: 1.49x faster                                 |
| genshi_text             | 30.6 ms                                            | 21.0 ms: 1.46x faster                                 |
| genshi_xml              | 64.1 ms                                            | 49.2 ms: 1.30x faster                                 |
| go                      | 227 ms                                             | 134 ms: 1.69x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.05 ms: 1.54x faster                                 |
| html5lib                | 85.1 ms                                            | 59.2 ms: 1.44x faster                                 |
| json                    | 5.55 ms                                            | 4.78 ms: 1.16x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.60 ms: 1.37x faster                                 |
| json_loads              | 31.1 us                                            | 23.9 us: 1.30x faster                                 |
| logging_format          | 8.78 us                                            | 6.38 us: 1.38x faster                                 |
| logging_silent          | 168 ns                                             | 92.9 ns: 1.81x faster                                 |
| logging_simple          | 8.07 us                                            | 5.73 us: 1.41x faster                                 |
| mako                    | 14.7 ms                                            | 9.82 ms: 1.50x faster                                 |
| meteor_contest          | 114 ms                                             | 103 ms: 1.10x faster                                  |
| nbody                   | 135 ms                                             | 94.2 ms: 1.43x faster                                 |
| nqueens                 | 98.4 ms                                            | 79.5 ms: 1.24x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.7 ms: 1.14x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.1 us: 1.14x slower                                 |
| pickle_list             | 4.40 us                                            | 4.14 us: 1.06x faster                                 |
| pickle_pure_python      | 449 us                                             | 293 us: 1.53x faster                                  |
| pidigits                | 190 ms                                             | 199 ms: 1.05x slower                                  |
| pycparser               | 1.52 sec                                           | 1.10 sec: 1.39x faster                                |
| pyflate                 | 664 ms                                             | 402 ms: 1.65x faster                                  |
| pylint                  | 512 ms                                             | 455 ms: 1.13x faster                                  |
| python_startup          | 9.21 ms                                            | 8.41 ms: 1.10x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.09 ms: 1.02x slower                                 |
| raytrace                | 463 ms                                             | 285 ms: 1.62x faster                                  |
| regex_compile           | 178 ms                                             | 129 ms: 1.38x faster                                  |
| regex_dna               | 214 ms                                             | 200 ms: 1.07x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.60 ms: 1.11x slower                                 |
| regex_v8                | 25.7 ms                                            | 22.2 ms: 1.15x faster                                 |
| richards                | 68.9 ms                                            | 43.0 ms: 1.60x faster                                 |
| scimark_fft             | 419 ms                                             | 315 ms: 1.33x faster                                  |
| scimark_lu              | 160 ms                                             | 108 ms: 1.48x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 65.6 ms: 1.63x faster                                 |
| scimark_sor             | 196 ms                                             | 104 ms: 1.88x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.16 ms: 1.31x faster                                 |
| spectral_norm           | 144 ms                                             | 96.7 ms: 1.49x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.62 us: 1.12x faster                                 |
| sympy_expand            | 538 ms                                             | 458 ms: 1.17x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.4 ms: 1.18x faster                                 |
| sympy_str               | 325 ms                                             | 281 ms: 1.16x faster                                  |
| sympy_sum               | 184 ms                                             | 163 ms: 1.13x faster                                  |
| telco                   | 6.60 ms                                            | 6.46 ms: 1.02x faster                                 |
| thrift                  | 1.01 ms                                            | 742 us: 1.37x faster                                  |
| tornado_http            | 127 ms                                             | 92.6 ms: 1.37x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 44.1 ns: 1.27x faster                                 |
| unpickle                | 14.4 us                                            | 12.9 us: 1.11x faster                                 |
| unpickle_list           | 4.90 us                                            | 4.96 us: 1.01x slower                                 |
| unpickle_pure_python    | 298 us                                             | 202 us: 1.47x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 76.9 ms: 1.20x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 103 ms: 1.07x faster                                  |
| xml_etree_parse         | 162 ms                                             | 145 ms: 1.12x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 53.7 ms: 1.35x faster                                 |
| Geometric mean          | (ref)                                              | 1.30x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (20) of public/results/bm-20221015-python-main-3.12.0a1+-660f102/bm-20221015-linux-amd64-python-main-3.12.0a1+-660f102.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
