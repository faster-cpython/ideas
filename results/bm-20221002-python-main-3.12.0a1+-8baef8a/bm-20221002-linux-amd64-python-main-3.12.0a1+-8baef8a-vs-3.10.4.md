| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20221002-linux-amd64-python-main-3.12.0a1+-8baef8a |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 246 ms: 1.35x faster                                  |
| chameleon               | 8.76 ms                                            | 6.38 ms: 1.37x faster                                 |
| chaos                   | 107 ms                                             | 66.4 ms: 1.61x faster                                 |
| crypto_pyaes            | 116 ms                                             | 72.8 ms: 1.60x faster                                 |
| deltablue               | 7.32 ms                                            | 3.26 ms: 2.25x faster                                 |
| django_template         | 45.7 ms                                            | 32.4 ms: 1.41x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.3 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 371 ms: 1.30x faster                                  |
| float                   | 107 ms                                             | 72.0 ms: 1.49x faster                                 |
| genshi_text             | 30.6 ms                                            | 20.7 ms: 1.48x faster                                 |
| genshi_xml              | 64.1 ms                                            | 48.4 ms: 1.33x faster                                 |
| go                      | 227 ms                                             | 132 ms: 1.72x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.00 ms: 1.55x faster                                 |
| html5lib                | 85.1 ms                                            | 59.3 ms: 1.44x faster                                 |
| json                    | 5.55 ms                                            | 4.51 ms: 1.23x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.56 ms: 1.38x faster                                 |
| json_loads              | 31.1 us                                            | 24.0 us: 1.30x faster                                 |
| logging_format          | 8.78 us                                            | 6.39 us: 1.38x faster                                 |
| logging_silent          | 168 ns                                             | 92.6 ns: 1.81x faster                                 |
| logging_simple          | 8.07 us                                            | 5.75 us: 1.40x faster                                 |
| mako                    | 14.7 ms                                            | 9.35 ms: 1.58x faster                                 |
| meteor_contest          | 114 ms                                             | 102 ms: 1.12x faster                                  |
| nbody                   | 135 ms                                             | 96.2 ms: 1.40x faster                                 |
| nqueens                 | 98.4 ms                                            | 79.3 ms: 1.24x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.6 ms: 1.14x faster                                 |
| pickle_dict             | 27.2 us                                            | 30.9 us: 1.14x slower                                 |
| pickle_list             | 4.40 us                                            | 4.06 us: 1.08x faster                                 |
| pickle_pure_python      | 449 us                                             | 285 us: 1.58x faster                                  |
| pidigits                | 190 ms                                             | 193 ms: 1.02x slower                                  |
| pycparser               | 1.52 sec                                           | 1.10 sec: 1.38x faster                                |
| pyflate                 | 664 ms                                             | 400 ms: 1.66x faster                                  |
| pylint                  | 512 ms                                             | 447 ms: 1.15x faster                                  |
| python_startup          | 9.21 ms                                            | 8.35 ms: 1.10x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.05 ms: 1.01x slower                                 |
| raytrace                | 463 ms                                             | 278 ms: 1.66x faster                                  |
| regex_compile           | 178 ms                                             | 127 ms: 1.40x faster                                  |
| regex_dna               | 214 ms                                             | 204 ms: 1.05x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.32 ms: 1.02x slower                                 |
| regex_v8                | 25.7 ms                                            | 21.3 ms: 1.20x faster                                 |
| richards                | 68.9 ms                                            | 44.2 ms: 1.56x faster                                 |
| scimark_fft             | 419 ms                                             | 317 ms: 1.32x faster                                  |
| scimark_lu              | 160 ms                                             | 108 ms: 1.48x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 65.6 ms: 1.64x faster                                 |
| scimark_sor             | 196 ms                                             | 105 ms: 1.87x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.17 ms: 1.31x faster                                 |
| spectral_norm           | 144 ms                                             | 92.3 ms: 1.56x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.57 us: 1.14x faster                                 |
| sympy_expand            | 538 ms                                             | 453 ms: 1.19x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.3 ms: 1.18x faster                                 |
| sympy_str               | 325 ms                                             | 281 ms: 1.16x faster                                  |
| sympy_sum               | 184 ms                                             | 163 ms: 1.13x faster                                  |
| telco                   | 6.60 ms                                            | 6.33 ms: 1.04x faster                                 |
| thrift                  | 1.01 ms                                            | 744 us: 1.36x faster                                  |
| tornado_http            | 127 ms                                             | 92.8 ms: 1.37x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 43.5 ns: 1.29x faster                                 |
| unpickle                | 14.4 us                                            | 13.5 us: 1.06x faster                                 |
| unpickle_list           | 4.90 us                                            | 4.96 us: 1.01x slower                                 |
| unpickle_pure_python    | 298 us                                             | 201 us: 1.48x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.3 ms: 1.23x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 103 ms: 1.07x faster                                  |
| xml_etree_parse         | 162 ms                                             | 157 ms: 1.04x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.9 ms: 1.37x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (20) of public/results/bm-20221002-python-main-3.12.0a1+-8baef8a/bm-20221002-linux-amd64-python-main-3.12.0a1+-8baef8a.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
