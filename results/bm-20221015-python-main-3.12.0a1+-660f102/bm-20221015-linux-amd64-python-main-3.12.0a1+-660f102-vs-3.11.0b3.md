| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20221015-linux-amd64-python-main-3.12.0a1+-660f102 |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 249 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.71 ms: 1.01x slower                                 |
| chaos                   | 66.9 ms                                              | 66.1 ms: 1.01x faster                                 |
| crypto_pyaes            | 73.1 ms                                              | 75.2 ms: 1.03x slower                                 |
| deltablue               | 3.62 ms                                              | 3.31 ms: 1.09x faster                                 |
| django_template         | 32.9 ms                                              | 32.6 ms: 1.01x faster                                 |
| dulwich_log             | 63.1 ms                                              | 60.9 ms: 1.04x faster                                 |
| fannkuch                | 372 ms                                               | 368 ms: 1.01x faster                                  |
| float                   | 72.9 ms                                              | 72.2 ms: 1.01x faster                                 |
| go                      | 137 ms                                               | 134 ms: 1.02x faster                                  |
| hexiom                  | 6.32 ms                                              | 6.05 ms: 1.04x faster                                 |
| html5lib                | 62.6 ms                                              | 59.2 ms: 1.06x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.60 ms: 1.30x faster                                 |
| json_loads              | 24.4 us                                              | 23.9 us: 1.02x faster                                 |
| logging_format          | 6.44 us                                              | 6.38 us: 1.01x faster                                 |
| logging_silent          | 101 ns                                               | 92.9 ns: 1.09x faster                                 |
| logging_simple          | 5.95 us                                              | 5.73 us: 1.04x faster                                 |
| nbody                   | 90.6 ms                                              | 94.2 ms: 1.04x slower                                 |
| nqueens                 | 80.7 ms                                              | 79.5 ms: 1.02x faster                                 |
| pathlib                 | 17.9 ms                                              | 17.7 ms: 1.01x faster                                 |
| pickle                  | 9.55 us                                              | 10.3 us: 1.08x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.1 us: 1.21x slower                                 |
| pickle_list             | 4.33 us                                              | 4.14 us: 1.05x faster                                 |
| pickle_pure_python      | 302 us                                               | 293 us: 1.03x faster                                  |
| pidigits                | 194 ms                                               | 199 ms: 1.03x slower                                  |
| pycparser               | 1.10 sec                                             | 1.10 sec: 1.01x faster                                |
| pyflate                 | 411 ms                                               | 402 ms: 1.02x faster                                  |
| python_startup          | 8.33 ms                                              | 8.41 ms: 1.01x slower                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.09 ms: 1.01x faster                                 |
| raytrace                | 292 ms                                               | 285 ms: 1.02x faster                                  |
| regex_compile           | 135 ms                                               | 129 ms: 1.05x faster                                  |
| regex_dna               | 192 ms                                               | 200 ms: 1.05x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.60 ms: 1.23x slower                                 |
| regex_v8                | 21.2 ms                                              | 22.2 ms: 1.05x slower                                 |
| richards                | 46.5 ms                                              | 43.0 ms: 1.08x faster                                 |
| scimark_fft             | 317 ms                                               | 315 ms: 1.01x faster                                  |
| scimark_lu              | 107 ms                                               | 108 ms: 1.01x slower                                  |
| scimark_sor             | 115 ms                                               | 104 ms: 1.11x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.16 ms: 1.09x faster                                 |
| spectral_norm           | 97.6 ms                                              | 96.7 ms: 1.01x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.62 us: 1.05x slower                                 |
| sympy_expand            | 467 ms                                               | 458 ms: 1.02x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.4 ms: 1.00x faster                                 |
| sympy_str               | 284 ms                                               | 281 ms: 1.01x faster                                  |
| sympy_sum               | 159 ms                                               | 163 ms: 1.03x slower                                  |
| thrift                  | 759 us                                               | 742 us: 1.02x faster                                  |
| tornado_http            | 93.8 ms                                              | 92.6 ms: 1.01x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 44.1 ns: 1.02x slower                                 |
| unpickle                | 13.3 us                                              | 12.9 us: 1.03x faster                                 |
| unpickle_list           | 4.89 us                                              | 4.96 us: 1.01x slower                                 |
| unpickle_pure_python    | 228 us                                               | 202 us: 1.13x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 76.9 ms: 1.01x slower                                 |
| xml_etree_iterparse     | 105 ms                                               | 103 ms: 1.02x faster                                  |
| xml_etree_parse         | 156 ms                                               | 145 ms: 1.07x faster                                  |
| Geometric mean          | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (6): json, mako, meteor_contest, scimark_monte_carlo, telco, xml_etree_process
Ignored benchmarks (23) of public/results/bm-20221015-python-main-3.12.0a1+-660f102/bm-20221015-linux-amd64-python-main-3.12.0a1+-660f102.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
