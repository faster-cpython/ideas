| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221009-linux-amd64-python-main-3.12.0a1+-2d2e01a |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 248 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.61 ms: 1.32x faster                                 |
| chaos                   | 107 ms                                             | 65.5 ms: 1.63x faster                                 |
| crypto_pyaes            | 116 ms                                             | 75.3 ms: 1.54x faster                                 |
| deltablue               | 7.32 ms                                            | 3.40 ms: 2.15x faster                                 |
| django_template         | 45.7 ms                                            | 33.3 ms: 1.37x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.1 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 362 ms: 1.33x faster                                  |
| float                   | 107 ms                                             | 72.3 ms: 1.48x faster                                 |
| genshi_text             | 30.6 ms                                            | 21.8 ms: 1.40x faster                                 |
| genshi_xml              | 64.1 ms                                            | 49.1 ms: 1.30x faster                                 |
| go                      | 227 ms                                             | 138 ms: 1.64x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.02 ms: 1.54x faster                                 |
| html5lib                | 85.1 ms                                            | 59.7 ms: 1.42x faster                                 |
| json                    | 5.55 ms                                            | 4.72 ms: 1.17x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.44 ms: 1.39x faster                                 |
| json_loads              | 31.1 us                                            | 23.8 us: 1.31x faster                                 |
| logging_format          | 8.78 us                                            | 6.43 us: 1.37x faster                                 |
| logging_silent          | 168 ns                                             | 92.7 ns: 1.81x faster                                 |
| logging_simple          | 8.07 us                                            | 5.74 us: 1.41x faster                                 |
| mako                    | 14.7 ms                                            | 9.84 ms: 1.50x faster                                 |
| meteor_contest          | 114 ms                                             | 103 ms: 1.11x faster                                  |
| nbody                   | 135 ms                                             | 94.6 ms: 1.42x faster                                 |
| nqueens                 | 98.4 ms                                            | 79.2 ms: 1.24x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.9 ms: 1.13x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.9 us: 1.17x slower                                 |
| pickle_list             | 4.40 us                                            | 4.06 us: 1.08x faster                                 |
| pickle_pure_python      | 449 us                                             | 293 us: 1.53x faster                                  |
| pidigits                | 190 ms                                             | 189 ms: 1.01x faster                                  |
| pycparser               | 1.52 sec                                           | 1.09 sec: 1.40x faster                                |
| pyflate                 | 664 ms                                             | 407 ms: 1.63x faster                                  |
| pylint                  | 512 ms                                             | 454 ms: 1.13x faster                                  |
| python_startup          | 9.21 ms                                            | 8.38 ms: 1.10x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.06 ms: 1.02x slower                                 |
| raytrace                | 463 ms                                             | 284 ms: 1.63x faster                                  |
| regex_compile           | 178 ms                                             | 128 ms: 1.39x faster                                  |
| regex_dna               | 214 ms                                             | 203 ms: 1.06x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.60 ms: 1.11x slower                                 |
| regex_v8                | 25.7 ms                                            | 22.1 ms: 1.16x faster                                 |
| richards                | 68.9 ms                                            | 44.4 ms: 1.55x faster                                 |
| scimark_fft             | 419 ms                                             | 316 ms: 1.32x faster                                  |
| scimark_lu              | 160 ms                                             | 108 ms: 1.48x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 66.3 ms: 1.62x faster                                 |
| scimark_sor             | 196 ms                                             | 105 ms: 1.87x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.20 ms: 1.30x faster                                 |
| spectral_norm           | 144 ms                                             | 96.4 ms: 1.49x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.60 us: 1.12x faster                                 |
| sympy_expand            | 538 ms                                             | 456 ms: 1.18x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.4 ms: 1.18x faster                                 |
| sympy_str               | 325 ms                                             | 280 ms: 1.16x faster                                  |
| sympy_sum               | 184 ms                                             | 164 ms: 1.13x faster                                  |
| telco                   | 6.60 ms                                            | 6.32 ms: 1.04x faster                                 |
| thrift                  | 1.01 ms                                            | 737 us: 1.38x faster                                  |
| tornado_http            | 127 ms                                             | 93.4 ms: 1.36x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 50.2 ns: 1.12x faster                                 |
| unpickle                | 14.4 us                                            | 13.0 us: 1.10x faster                                 |
| unpickle_list           | 4.90 us                                            | 5.02 us: 1.02x slower                                 |
| unpickle_pure_python    | 298 us                                             | 204 us: 1.46x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 76.6 ms: 1.21x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 101 ms: 1.09x faster                                  |
| xml_etree_parse         | 162 ms                                             | 146 ms: 1.11x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 53.7 ms: 1.35x faster                                 |
| Geometric mean          | (ref)                                              | 1.30x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (20) of public/results/bm-20221009-python-main-3.12.0a1+-2d2e01a/bm-20221009-linux-amd64-python-main-3.12.0a1+-2d2e01a.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
