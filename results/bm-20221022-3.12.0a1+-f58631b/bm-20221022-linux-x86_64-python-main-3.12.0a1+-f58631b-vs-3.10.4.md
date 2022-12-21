| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221022-linux-amd64-python-main-3.12.0a1+-f58631b |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 250 ms: 1.33x faster                                  |
| chameleon               | 8.76 ms                                            | 6.60 ms: 1.33x faster                                 |
| chaos                   | 107 ms                                             | 69.7 ms: 1.54x faster                                 |
| crypto_pyaes            | 116 ms                                             | 76.4 ms: 1.52x faster                                 |
| deltablue               | 7.32 ms                                            | 3.30 ms: 2.22x faster                                 |
| django_template         | 45.7 ms                                            | 32.6 ms: 1.40x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.3 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 371 ms: 1.30x faster                                  |
| float                   | 107 ms                                             | 72.5 ms: 1.48x faster                                 |
| genshi_text             | 30.6 ms                                            | 21.0 ms: 1.46x faster                                 |
| genshi_xml              | 64.1 ms                                            | 49.7 ms: 1.29x faster                                 |
| go                      | 227 ms                                             | 134 ms: 1.69x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.07 ms: 1.53x faster                                 |
| html5lib                | 85.1 ms                                            | 59.1 ms: 1.44x faster                                 |
| json                    | 5.55 ms                                            | 4.58 ms: 1.21x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.49 ms: 1.39x faster                                 |
| json_loads              | 31.1 us                                            | 23.5 us: 1.32x faster                                 |
| logging_format          | 8.78 us                                            | 6.47 us: 1.36x faster                                 |
| logging_silent          | 168 ns                                             | 90.5 ns: 1.85x faster                                 |
| logging_simple          | 8.07 us                                            | 5.84 us: 1.38x faster                                 |
| mako                    | 14.7 ms                                            | 9.75 ms: 1.51x faster                                 |
| meteor_contest          | 114 ms                                             | 103 ms: 1.10x faster                                  |
| nbody                   | 135 ms                                             | 93.9 ms: 1.44x faster                                 |
| nqueens                 | 98.4 ms                                            | 80.3 ms: 1.23x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.8 ms: 1.13x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.0 us: 1.14x slower                                 |
| pickle_list             | 4.40 us                                            | 3.96 us: 1.11x faster                                 |
| pickle_pure_python      | 449 us                                             | 289 us: 1.55x faster                                  |
| pidigits                | 190 ms                                             | 199 ms: 1.05x slower                                  |
| pycparser               | 1.52 sec                                           | 1.09 sec: 1.40x faster                                |
| pyflate                 | 664 ms                                             | 400 ms: 1.66x faster                                  |
| pylint                  | 512 ms                                             | 455 ms: 1.12x faster                                  |
| python_startup          | 9.21 ms                                            | 8.37 ms: 1.10x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.06 ms: 1.02x slower                                 |
| raytrace                | 463 ms                                             | 287 ms: 1.61x faster                                  |
| regex_compile           | 178 ms                                             | 130 ms: 1.37x faster                                  |
| regex_dna               | 214 ms                                             | 209 ms: 1.02x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.66 ms: 1.13x slower                                 |
| regex_v8                | 25.7 ms                                            | 22.7 ms: 1.13x faster                                 |
| richards                | 68.9 ms                                            | 43.5 ms: 1.58x faster                                 |
| scimark_fft             | 419 ms                                             | 317 ms: 1.32x faster                                  |
| scimark_lu              | 160 ms                                             | 109 ms: 1.47x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 66.6 ms: 1.61x faster                                 |
| scimark_sor             | 196 ms                                             | 105 ms: 1.87x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.22 ms: 1.29x faster                                 |
| spectral_norm           | 144 ms                                             | 95.1 ms: 1.51x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.61 us: 1.12x faster                                 |
| sympy_expand            | 538 ms                                             | 454 ms: 1.19x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.3 ms: 1.18x faster                                 |
| sympy_str               | 325 ms                                             | 282 ms: 1.15x faster                                  |
| sympy_sum               | 184 ms                                             | 164 ms: 1.13x faster                                  |
| telco                   | 6.60 ms                                            | 6.54 ms: 1.01x faster                                 |
| thrift                  | 1.01 ms                                            | 739 us: 1.37x faster                                  |
| tornado_http            | 127 ms                                             | 93.1 ms: 1.37x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 48.7 ns: 1.15x faster                                 |
| unpickle                | 14.4 us                                            | 13.3 us: 1.08x faster                                 |
| unpickle_list           | 4.90 us                                            | 4.98 us: 1.02x slower                                 |
| unpickle_pure_python    | 298 us                                             | 203 us: 1.47x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.5 ms: 1.22x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 102 ms: 1.08x faster                                  |
| xml_etree_parse         | 162 ms                                             | 147 ms: 1.10x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 53.1 ms: 1.37x faster                                 |
| Geometric mean          | (ref)                                              | 1.30x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (20) of public/results/bm-20221022-python-main-3.12.0a1+-f58631b/bm-20221022-linux-amd64-python-main-3.12.0a1+-f58631b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
