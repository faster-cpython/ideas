| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221019-linux-amd64-python-main-3.12.0a1+-5055300 |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 249 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.46 ms: 1.36x faster                                 |
| chaos                   | 107 ms                                             | 67.8 ms: 1.58x faster                                 |
| crypto_pyaes            | 116 ms                                             | 75.4 ms: 1.54x faster                                 |
| deltablue               | 7.32 ms                                            | 3.36 ms: 2.18x faster                                 |
| django_template         | 45.7 ms                                            | 32.7 ms: 1.40x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.2 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 363 ms: 1.33x faster                                  |
| float                   | 107 ms                                             | 71.1 ms: 1.51x faster                                 |
| genshi_text             | 30.6 ms                                            | 20.9 ms: 1.46x faster                                 |
| genshi_xml              | 64.1 ms                                            | 49.3 ms: 1.30x faster                                 |
| go                      | 227 ms                                             | 136 ms: 1.67x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.11 ms: 1.52x faster                                 |
| html5lib                | 85.1 ms                                            | 60.2 ms: 1.41x faster                                 |
| json                    | 5.55 ms                                            | 4.77 ms: 1.16x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.42 ms: 1.40x faster                                 |
| json_loads              | 31.1 us                                            | 24.0 us: 1.30x faster                                 |
| logging_format          | 8.78 us                                            | 6.49 us: 1.35x faster                                 |
| logging_silent          | 168 ns                                             | 93.3 ns: 1.80x faster                                 |
| logging_simple          | 8.07 us                                            | 5.83 us: 1.39x faster                                 |
| mako                    | 14.7 ms                                            | 9.79 ms: 1.50x faster                                 |
| meteor_contest          | 114 ms                                             | 102 ms: 1.12x faster                                  |
| nbody                   | 135 ms                                             | 94.8 ms: 1.42x faster                                 |
| nqueens                 | 98.4 ms                                            | 80.9 ms: 1.22x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.6 ms: 1.15x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.1 us: 1.14x slower                                 |
| pickle_list             | 4.40 us                                            | 3.99 us: 1.10x faster                                 |
| pickle_pure_python      | 449 us                                             | 285 us: 1.58x faster                                  |
| pidigits                | 190 ms                                             | 193 ms: 1.01x slower                                  |
| pycparser               | 1.52 sec                                           | 1.08 sec: 1.40x faster                                |
| pyflate                 | 664 ms                                             | 409 ms: 1.62x faster                                  |
| pylint                  | 512 ms                                             | 454 ms: 1.13x faster                                  |
| python_startup          | 9.21 ms                                            | 8.32 ms: 1.11x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.03 ms: 1.01x slower                                 |
| raytrace                | 463 ms                                             | 289 ms: 1.60x faster                                  |
| regex_compile           | 178 ms                                             | 128 ms: 1.39x faster                                  |
| regex_dna               | 214 ms                                             | 205 ms: 1.04x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.40 ms: 1.05x slower                                 |
| regex_v8                | 25.7 ms                                            | 21.4 ms: 1.20x faster                                 |
| richards                | 68.9 ms                                            | 45.2 ms: 1.52x faster                                 |
| scimark_fft             | 419 ms                                             | 311 ms: 1.35x faster                                  |
| scimark_lu              | 160 ms                                             | 108 ms: 1.49x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 67.0 ms: 1.60x faster                                 |
| scimark_sor             | 196 ms                                             | 104 ms: 1.88x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.04 ms: 1.35x faster                                 |
| spectral_norm           | 144 ms                                             | 95.4 ms: 1.51x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.60 us: 1.12x faster                                 |
| sympy_expand            | 538 ms                                             | 456 ms: 1.18x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.3 ms: 1.19x faster                                 |
| sympy_str               | 325 ms                                             | 280 ms: 1.16x faster                                  |
| sympy_sum               | 184 ms                                             | 163 ms: 1.13x faster                                  |
| telco                   | 6.60 ms                                            | 6.43 ms: 1.03x faster                                 |
| thrift                  | 1.01 ms                                            | 742 us: 1.37x faster                                  |
| tornado_http            | 127 ms                                             | 93.0 ms: 1.37x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 45.7 ns: 1.23x faster                                 |
| unpickle                | 14.4 us                                            | 13.3 us: 1.08x faster                                 |
| unpickle_list           | 4.90 us                                            | 5.02 us: 1.02x slower                                 |
| unpickle_pure_python    | 298 us                                             | 202 us: 1.47x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 76.9 ms: 1.20x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 106 ms: 1.04x faster                                  |
| xml_etree_parse         | 162 ms                                             | 144 ms: 1.12x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 53.3 ms: 1.36x faster                                 |
| Geometric mean          | (ref)                                              | 1.30x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (20) of public/results/bm-20221019-python-main-3.12.0a1+-5055300/bm-20221019-linux-amd64-python-main-3.12.0a1+-5055300.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
