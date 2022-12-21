| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221112-linux-amd64-python-main-3.12.0a2+-57be545 |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 246 ms: 1.35x faster                                  |
| chameleon               | 8.76 ms                                            | 6.49 ms: 1.35x faster                                 |
| chaos                   | 107 ms                                             | 67.0 ms: 1.60x faster                                 |
| crypto_pyaes            | 116 ms                                             | 75.1 ms: 1.55x faster                                 |
| deltablue               | 7.32 ms                                            | 3.22 ms: 2.27x faster                                 |
| django_template         | 45.7 ms                                            | 32.5 ms: 1.41x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.1 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 374 ms: 1.29x faster                                  |
| float                   | 107 ms                                             | 73.3 ms: 1.47x faster                                 |
| genshi_text             | 30.6 ms                                            | 21.3 ms: 1.43x faster                                 |
| genshi_xml              | 64.1 ms                                            | 46.8 ms: 1.37x faster                                 |
| go                      | 227 ms                                             | 135 ms: 1.68x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.13 ms: 1.51x faster                                 |
| html5lib                | 85.1 ms                                            | 58.9 ms: 1.45x faster                                 |
| json                    | 5.55 ms                                            | 4.71 ms: 1.18x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.44 ms: 1.39x faster                                 |
| json_loads              | 31.1 us                                            | 24.2 us: 1.29x faster                                 |
| logging_format          | 8.78 us                                            | 6.34 us: 1.39x faster                                 |
| logging_silent          | 168 ns                                             | 91.8 ns: 1.83x faster                                 |
| logging_simple          | 8.07 us                                            | 5.77 us: 1.40x faster                                 |
| mako                    | 14.7 ms                                            | 9.70 ms: 1.52x faster                                 |
| meteor_contest          | 114 ms                                             | 104 ms: 1.09x faster                                  |
| nbody                   | 135 ms                                             | 93.4 ms: 1.44x faster                                 |
| nqueens                 | 98.4 ms                                            | 81.1 ms: 1.21x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.5 ms: 1.15x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.1 us: 1.15x slower                                 |
| pickle_list             | 4.40 us                                            | 4.14 us: 1.06x faster                                 |
| pickle_pure_python      | 449 us                                             | 281 us: 1.60x faster                                  |
| pidigits                | 190 ms                                             | 197 ms: 1.04x slower                                  |
| pycparser               | 1.52 sec                                           | 1.11 sec: 1.37x faster                                |
| pyflate                 | 664 ms                                             | 402 ms: 1.65x faster                                  |
| python_startup          | 9.21 ms                                            | 8.52 ms: 1.08x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.24 ms: 1.05x slower                                 |
| raytrace                | 463 ms                                             | 281 ms: 1.65x faster                                  |
| regex_compile           | 178 ms                                             | 128 ms: 1.40x faster                                  |
| regex_dna               | 214 ms                                             | 205 ms: 1.05x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.64 ms: 1.12x slower                                 |
| regex_v8                | 25.7 ms                                            | 22.2 ms: 1.16x faster                                 |
| richards                | 68.9 ms                                            | 41.7 ms: 1.65x faster                                 |
| scimark_fft             | 419 ms                                             | 309 ms: 1.35x faster                                  |
| scimark_lu              | 160 ms                                             | 108 ms: 1.49x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 65.5 ms: 1.64x faster                                 |
| scimark_sor             | 196 ms                                             | 104 ms: 1.89x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.16 ms: 1.31x faster                                 |
| spectral_norm           | 144 ms                                             | 95.2 ms: 1.51x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.65 us: 1.10x faster                                 |
| sympy_expand            | 538 ms                                             | 458 ms: 1.17x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.3 ms: 1.18x faster                                 |
| sympy_str               | 325 ms                                             | 283 ms: 1.15x faster                                  |
| sympy_sum               | 184 ms                                             | 164 ms: 1.13x faster                                  |
| telco                   | 6.60 ms                                            | 6.32 ms: 1.04x faster                                 |
| thrift                  | 1.01 ms                                            | 745 us: 1.36x faster                                  |
| tornado_http            | 127 ms                                             | 92.5 ms: 1.38x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 44.2 ns: 1.27x faster                                 |
| unpickle                | 14.4 us                                            | 13.3 us: 1.08x faster                                 |
| unpickle_list           | 4.90 us                                            | 4.91 us: 1.00x slower                                 |
| unpickle_pure_python    | 298 us                                             | 200 us: 1.49x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 76.8 ms: 1.20x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 103 ms: 1.06x faster                                  |
| xml_etree_parse         | 162 ms                                             | 149 ms: 1.09x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 53.0 ms: 1.37x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (1) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: pylint
Ignored benchmarks (20) of public/results/bm-20221112-python-main-3.12.0a2+-57be545/bm-20221112-linux-amd64-python-main-3.12.0a2+-57be545.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
