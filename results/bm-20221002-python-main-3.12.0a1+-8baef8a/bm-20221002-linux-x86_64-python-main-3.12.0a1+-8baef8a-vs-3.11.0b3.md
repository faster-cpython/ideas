| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20221002-linux-amd64-python-main-3.12.0a1+-8baef8a |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 246 ms: 1.04x faster                                  |
| chameleon               | 6.67 ms                                              | 6.38 ms: 1.05x faster                                 |
| chaos                   | 66.9 ms                                              | 66.4 ms: 1.01x faster                                 |
| deltablue               | 3.62 ms                                              | 3.26 ms: 1.11x faster                                 |
| django_template         | 32.9 ms                                              | 32.4 ms: 1.01x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.3 ms: 1.03x faster                                 |
| float                   | 72.9 ms                                              | 72.0 ms: 1.01x faster                                 |
| go                      | 137 ms                                               | 132 ms: 1.03x faster                                  |
| hexiom                  | 6.32 ms                                              | 6.00 ms: 1.05x faster                                 |
| html5lib                | 62.6 ms                                              | 59.3 ms: 1.06x faster                                 |
| json                    | 4.75 ms                                              | 4.51 ms: 1.05x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.56 ms: 1.31x faster                                 |
| json_loads              | 24.4 us                                              | 24.0 us: 1.02x faster                                 |
| logging_format          | 6.44 us                                              | 6.39 us: 1.01x faster                                 |
| logging_silent          | 101 ns                                               | 92.6 ns: 1.10x faster                                 |
| logging_simple          | 5.95 us                                              | 5.75 us: 1.03x faster                                 |
| mako                    | 9.82 ms                                              | 9.35 ms: 1.05x faster                                 |
| meteor_contest          | 104 ms                                               | 102 ms: 1.02x faster                                  |
| nbody                   | 90.6 ms                                              | 96.2 ms: 1.06x slower                                 |
| nqueens                 | 80.7 ms                                              | 79.3 ms: 1.02x faster                                 |
| pathlib                 | 17.9 ms                                              | 17.6 ms: 1.02x faster                                 |
| pickle                  | 9.55 us                                              | 10.1 us: 1.05x slower                                 |
| pickle_dict             | 25.6 us                                              | 30.9 us: 1.21x slower                                 |
| pickle_list             | 4.33 us                                              | 4.06 us: 1.07x faster                                 |
| pickle_pure_python      | 302 us                                               | 285 us: 1.06x faster                                  |
| pidigits                | 194 ms                                               | 193 ms: 1.00x faster                                  |
| pyflate                 | 411 ms                                               | 400 ms: 1.03x faster                                  |
| python_startup          | 8.33 ms                                              | 8.35 ms: 1.00x slower                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.05 ms: 1.02x faster                                 |
| raytrace                | 292 ms                                               | 278 ms: 1.05x faster                                  |
| regex_compile           | 135 ms                                               | 127 ms: 1.07x faster                                  |
| regex_dna               | 192 ms                                               | 204 ms: 1.07x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.32 ms: 1.14x slower                                 |
| regex_v8                | 21.2 ms                                              | 21.3 ms: 1.01x slower                                 |
| richards                | 46.5 ms                                              | 44.2 ms: 1.05x faster                                 |
| scimark_lu              | 107 ms                                               | 108 ms: 1.01x slower                                  |
| scimark_sor             | 115 ms                                               | 105 ms: 1.10x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.17 ms: 1.09x faster                                 |
| spectral_norm           | 97.6 ms                                              | 92.3 ms: 1.06x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.57 us: 1.03x slower                                 |
| sympy_expand            | 467 ms                                               | 453 ms: 1.03x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.3 ms: 1.01x faster                                 |
| sympy_str               | 284 ms                                               | 281 ms: 1.01x faster                                  |
| sympy_sum               | 159 ms                                               | 163 ms: 1.03x slower                                  |
| telco                   | 6.49 ms                                              | 6.33 ms: 1.03x faster                                 |
| thrift                  | 759 us                                               | 744 us: 1.02x faster                                  |
| tornado_http            | 93.8 ms                                              | 92.8 ms: 1.01x faster                                 |
| unpickle_list           | 4.89 us                                              | 4.96 us: 1.02x slower                                 |
| unpickle_pure_python    | 228 us                                               | 201 us: 1.13x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.3 ms: 1.01x faster                                 |
| xml_etree_iterparse     | 105 ms                                               | 103 ms: 1.02x faster                                  |
| xml_etree_parse         | 156 ms                                               | 157 ms: 1.01x slower                                  |
| xml_etree_process       | 53.8 ms                                              | 52.9 ms: 1.02x faster                                 |
| Geometric mean          | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (7): crypto_pyaes, fannkuch, pycparser, scimark_fft, scimark_monte_carlo, unpack_sequence, unpickle
Ignored benchmarks (23) of public/results/bm-20221002-python-main-3.12.0a1+-8baef8a/bm-20221002-linux-amd64-python-main-3.12.0a1+-8baef8a.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
