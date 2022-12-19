| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20221029-linux-amd64-python-main-3.12.0a2+-fc94d55 |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 248 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.37 ms: 1.05x faster                                 |
| chaos                   | 66.9 ms                                              | 67.4 ms: 1.01x slower                                 |
| crypto_pyaes            | 73.1 ms                                              | 74.7 ms: 1.02x slower                                 |
| deltablue               | 3.62 ms                                              | 3.30 ms: 1.10x faster                                 |
| django_template         | 32.9 ms                                              | 32.0 ms: 1.03x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.6 ms: 1.02x faster                                 |
| go                      | 137 ms                                               | 137 ms: 1.00x slower                                  |
| hexiom                  | 6.32 ms                                              | 6.22 ms: 1.01x faster                                 |
| html5lib                | 62.6 ms                                              | 59.5 ms: 1.05x faster                                 |
| json                    | 4.75 ms                                              | 4.67 ms: 1.02x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.31 ms: 1.34x faster                                 |
| json_loads              | 24.4 us                                              | 23.5 us: 1.04x faster                                 |
| logging_silent          | 101 ns                                               | 94.4 ns: 1.07x faster                                 |
| logging_simple          | 5.95 us                                              | 5.78 us: 1.03x faster                                 |
| mako                    | 9.82 ms                                              | 9.72 ms: 1.01x faster                                 |
| meteor_contest          | 104 ms                                               | 103 ms: 1.01x faster                                  |
| nbody                   | 90.6 ms                                              | 98.1 ms: 1.08x slower                                 |
| pathlib                 | 17.9 ms                                              | 17.6 ms: 1.01x faster                                 |
| pickle                  | 9.55 us                                              | 10.4 us: 1.09x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.6 us: 1.24x slower                                 |
| pickle_list             | 4.33 us                                              | 4.16 us: 1.04x faster                                 |
| pickle_pure_python      | 302 us                                               | 287 us: 1.05x faster                                  |
| pidigits                | 194 ms                                               | 190 ms: 1.02x faster                                  |
| pycparser               | 1.10 sec                                             | 1.09 sec: 1.01x faster                                |
| pyflate                 | 411 ms                                               | 399 ms: 1.03x faster                                  |
| python_startup          | 8.33 ms                                              | 8.37 ms: 1.01x slower                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.08 ms: 1.02x faster                                 |
| raytrace                | 292 ms                                               | 285 ms: 1.03x faster                                  |
| regex_compile           | 135 ms                                               | 130 ms: 1.04x faster                                  |
| regex_dna               | 192 ms                                               | 210 ms: 1.10x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.69 ms: 1.27x slower                                 |
| regex_v8                | 21.2 ms                                              | 22.9 ms: 1.08x slower                                 |
| richards                | 46.5 ms                                              | 43.4 ms: 1.07x faster                                 |
| scimark_lu              | 107 ms                                               | 110 ms: 1.03x slower                                  |
| scimark_sor             | 115 ms                                               | 107 ms: 1.07x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.27 ms: 1.06x faster                                 |
| spectral_norm           | 97.6 ms                                              | 94.1 ms: 1.04x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.64 us: 1.06x slower                                 |
| sympy_expand            | 467 ms                                               | 457 ms: 1.02x faster                                  |
| sympy_str               | 284 ms                                               | 282 ms: 1.01x faster                                  |
| sympy_sum               | 159 ms                                               | 164 ms: 1.03x slower                                  |
| telco                   | 6.49 ms                                              | 6.31 ms: 1.03x faster                                 |
| thrift                  | 759 us                                               | 736 us: 1.03x faster                                  |
| tornado_http            | 93.8 ms                                              | 93.1 ms: 1.01x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 46.0 ns: 1.06x slower                                 |
| unpickle                | 13.3 us                                              | 12.9 us: 1.03x faster                                 |
| unpickle_list           | 4.89 us                                              | 4.97 us: 1.02x slower                                 |
| unpickle_pure_python    | 228 us                                               | 205 us: 1.11x faster                                  |
| xml_etree_iterparse     | 105 ms                                               | 102 ms: 1.02x faster                                  |
| xml_etree_parse         | 156 ms                                               | 147 ms: 1.06x faster                                  |
| xml_etree_process       | 53.8 ms                                              | 53.1 ms: 1.01x faster                                 |
| Geometric mean          | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (8): fannkuch, float, logging_format, nqueens, scimark_fft, scimark_monte_carlo, sympy_integrate, xml_etree_generate
Ignored benchmarks (23) of public/results/bm-20221029-python-main-3.12.0a2+-fc94d55/bm-20221029-linux-amd64-python-main-3.12.0a2+-fc94d55.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
