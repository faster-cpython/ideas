| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20221022-linux-amd64-python-main-3.12.0a1+-f58631b |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 250 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.60 ms: 1.01x faster                                 |
| chaos                   | 66.9 ms                                              | 69.7 ms: 1.04x slower                                 |
| crypto_pyaes            | 73.1 ms                                              | 76.4 ms: 1.05x slower                                 |
| deltablue               | 3.62 ms                                              | 3.30 ms: 1.10x faster                                 |
| django_template         | 32.9 ms                                              | 32.6 ms: 1.01x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.3 ms: 1.03x faster                                 |
| go                      | 137 ms                                               | 134 ms: 1.02x faster                                  |
| hexiom                  | 6.32 ms                                              | 6.07 ms: 1.04x faster                                 |
| html5lib                | 62.6 ms                                              | 59.1 ms: 1.06x faster                                 |
| json                    | 4.75 ms                                              | 4.58 ms: 1.04x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.49 ms: 1.32x faster                                 |
| json_loads              | 24.4 us                                              | 23.5 us: 1.04x faster                                 |
| logging_silent          | 101 ns                                               | 90.5 ns: 1.12x faster                                 |
| logging_simple          | 5.95 us                                              | 5.84 us: 1.02x faster                                 |
| mako                    | 9.82 ms                                              | 9.75 ms: 1.01x faster                                 |
| meteor_contest          | 104 ms                                               | 103 ms: 1.01x faster                                  |
| nbody                   | 90.6 ms                                              | 93.9 ms: 1.04x slower                                 |
| nqueens                 | 80.7 ms                                              | 80.3 ms: 1.00x faster                                 |
| pathlib                 | 17.9 ms                                              | 17.8 ms: 1.01x faster                                 |
| pickle                  | 9.55 us                                              | 10.3 us: 1.08x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.0 us: 1.21x slower                                 |
| pickle_list             | 4.33 us                                              | 3.96 us: 1.09x faster                                 |
| pickle_pure_python      | 302 us                                               | 289 us: 1.04x faster                                  |
| pidigits                | 194 ms                                               | 199 ms: 1.03x slower                                  |
| pycparser               | 1.10 sec                                             | 1.09 sec: 1.02x faster                                |
| pyflate                 | 411 ms                                               | 400 ms: 1.03x faster                                  |
| python_startup          | 8.33 ms                                              | 8.37 ms: 1.00x slower                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.06 ms: 1.02x faster                                 |
| raytrace                | 292 ms                                               | 287 ms: 1.02x faster                                  |
| regex_compile           | 135 ms                                               | 130 ms: 1.04x faster                                  |
| regex_dna               | 192 ms                                               | 209 ms: 1.09x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.66 ms: 1.26x slower                                 |
| regex_v8                | 21.2 ms                                              | 22.7 ms: 1.07x slower                                 |
| richards                | 46.5 ms                                              | 43.5 ms: 1.07x faster                                 |
| scimark_fft             | 317 ms                                               | 317 ms: 1.00x faster                                  |
| scimark_lu              | 107 ms                                               | 109 ms: 1.02x slower                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 66.6 ms: 1.01x slower                                 |
| scimark_sor             | 115 ms                                               | 105 ms: 1.10x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.22 ms: 1.08x faster                                 |
| spectral_norm           | 97.6 ms                                              | 95.1 ms: 1.03x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.61 us: 1.05x slower                                 |
| sympy_expand            | 467 ms                                               | 454 ms: 1.03x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.3 ms: 1.01x faster                                 |
| sympy_str               | 284 ms                                               | 282 ms: 1.01x faster                                  |
| sympy_sum               | 159 ms                                               | 164 ms: 1.03x slower                                  |
| telco                   | 6.49 ms                                              | 6.54 ms: 1.01x slower                                 |
| thrift                  | 759 us                                               | 739 us: 1.03x faster                                  |
| tornado_http            | 93.8 ms                                              | 93.1 ms: 1.01x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 48.7 ns: 1.12x slower                                 |
| unpickle_list           | 4.89 us                                              | 4.98 us: 1.02x slower                                 |
| unpickle_pure_python    | 228 us                                               | 203 us: 1.12x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.5 ms: 1.01x faster                                 |
| xml_etree_iterparse     | 105 ms                                               | 102 ms: 1.03x faster                                  |
| xml_etree_parse         | 156 ms                                               | 147 ms: 1.06x faster                                  |
| xml_etree_process       | 53.8 ms                                              | 53.1 ms: 1.01x faster                                 |
| Geometric mean          | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (4): fannkuch, float, logging_format, unpickle
Ignored benchmarks (23) of public/results/bm-20221022-python-main-3.12.0a1+-f58631b/bm-20221022-linux-amd64-python-main-3.12.0a1+-f58631b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
