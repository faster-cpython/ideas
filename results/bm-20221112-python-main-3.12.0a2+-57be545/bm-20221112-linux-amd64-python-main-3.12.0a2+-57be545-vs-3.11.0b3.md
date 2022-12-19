| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20221112-linux-amd64-python-main-3.12.0a2+-57be545 |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 246 ms: 1.04x faster                                  |
| chameleon               | 6.67 ms                                              | 6.49 ms: 1.03x faster                                 |
| crypto_pyaes            | 73.1 ms                                              | 75.1 ms: 1.03x slower                                 |
| deltablue               | 3.62 ms                                              | 3.22 ms: 1.12x faster                                 |
| django_template         | 32.9 ms                                              | 32.5 ms: 1.01x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.1 ms: 1.03x faster                                 |
| fannkuch                | 372 ms                                               | 374 ms: 1.00x slower                                  |
| go                      | 137 ms                                               | 135 ms: 1.01x faster                                  |
| hexiom                  | 6.32 ms                                              | 6.13 ms: 1.03x faster                                 |
| html5lib                | 62.6 ms                                              | 58.9 ms: 1.06x faster                                 |
| json                    | 4.75 ms                                              | 4.71 ms: 1.01x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.44 ms: 1.32x faster                                 |
| json_loads              | 24.4 us                                              | 24.2 us: 1.01x faster                                 |
| logging_format          | 6.44 us                                              | 6.34 us: 1.02x faster                                 |
| logging_silent          | 101 ns                                               | 91.8 ns: 1.10x faster                                 |
| logging_simple          | 5.95 us                                              | 5.77 us: 1.03x faster                                 |
| mako                    | 9.82 ms                                              | 9.70 ms: 1.01x faster                                 |
| nbody                   | 90.6 ms                                              | 93.4 ms: 1.03x slower                                 |
| nqueens                 | 80.7 ms                                              | 81.1 ms: 1.00x slower                                 |
| pathlib                 | 17.9 ms                                              | 17.5 ms: 1.02x faster                                 |
| pickle                  | 9.55 us                                              | 10.0 us: 1.05x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.1 us: 1.22x slower                                 |
| pickle_list             | 4.33 us                                              | 4.14 us: 1.05x faster                                 |
| pickle_pure_python      | 302 us                                               | 281 us: 1.07x faster                                  |
| pidigits                | 194 ms                                               | 197 ms: 1.02x slower                                  |
| pycparser               | 1.10 sec                                             | 1.11 sec: 1.01x slower                                |
| pyflate                 | 411 ms                                               | 402 ms: 1.02x faster                                  |
| python_startup          | 8.33 ms                                              | 8.52 ms: 1.02x slower                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.24 ms: 1.01x slower                                 |
| raytrace                | 292 ms                                               | 281 ms: 1.04x faster                                  |
| regex_compile           | 135 ms                                               | 128 ms: 1.06x faster                                  |
| regex_dna               | 192 ms                                               | 205 ms: 1.07x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.64 ms: 1.25x slower                                 |
| regex_v8                | 21.2 ms                                              | 22.2 ms: 1.05x slower                                 |
| richards                | 46.5 ms                                              | 41.7 ms: 1.12x faster                                 |
| scimark_fft             | 317 ms                                               | 309 ms: 1.03x faster                                  |
| scimark_lu              | 107 ms                                               | 108 ms: 1.01x slower                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 65.5 ms: 1.01x faster                                 |
| scimark_sor             | 115 ms                                               | 104 ms: 1.11x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.16 ms: 1.09x faster                                 |
| spectral_norm           | 97.6 ms                                              | 95.2 ms: 1.03x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.65 us: 1.06x slower                                 |
| sympy_expand            | 467 ms                                               | 458 ms: 1.02x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.3 ms: 1.01x faster                                 |
| sympy_str               | 284 ms                                               | 283 ms: 1.01x faster                                  |
| sympy_sum               | 159 ms                                               | 164 ms: 1.03x slower                                  |
| telco                   | 6.49 ms                                              | 6.32 ms: 1.03x faster                                 |
| thrift                  | 759 us                                               | 745 us: 1.02x faster                                  |
| tornado_http            | 93.8 ms                                              | 92.5 ms: 1.01x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 44.2 ns: 1.02x slower                                 |
| unpickle_list           | 4.89 us                                              | 4.91 us: 1.01x slower                                 |
| unpickle_pure_python    | 228 us                                               | 200 us: 1.14x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 76.8 ms: 1.01x slower                                 |
| xml_etree_iterparse     | 105 ms                                               | 103 ms: 1.01x faster                                  |
| xml_etree_parse         | 156 ms                                               | 149 ms: 1.04x faster                                  |
| xml_etree_process       | 53.8 ms                                              | 53.0 ms: 1.02x faster                                 |
| Geometric mean          | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (4): chaos, float, meteor_contest, unpickle
Ignored benchmarks (22) of public/results/bm-20221112-python-main-3.12.0a2+-57be545/bm-20221112-linux-amd64-python-main-3.12.0a2+-57be545.json: aiohttp, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
