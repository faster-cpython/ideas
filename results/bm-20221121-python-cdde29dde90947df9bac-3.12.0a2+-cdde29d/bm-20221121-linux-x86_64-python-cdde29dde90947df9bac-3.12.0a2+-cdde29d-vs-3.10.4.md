| Benchmark               | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:---------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 332 ms                                              | 244 ms: 1.36x faster                                                   |
| chameleon               | 8.76 ms                                             | 6.31 ms: 1.39x faster                                                  |
| chaos                   | 107 ms                                              | 65.6 ms: 1.63x faster                                                  |
| crypto_pyaes            | 116 ms                                              | 75.1 ms: 1.55x faster                                                  |
| deltablue               | 7.32 ms                                             | 3.17 ms: 2.31x faster                                                  |
| django_template         | 45.7 ms                                             | 32.1 ms: 1.42x faster                                                  |
| dulwich_log             | 75.2 ms                                             | 61.5 ms: 1.22x faster                                                  |
| fannkuch                | 483 ms                                              | 373 ms: 1.30x faster                                                   |
| float                   | 107 ms                                              | 73.1 ms: 1.47x faster                                                  |
| genshi_text             | 30.6 ms                                             | 20.2 ms: 1.52x faster                                                  |
| genshi_xml              | 64.1 ms                                             | 46.6 ms: 1.38x faster                                                  |
| go                      | 227 ms                                              | 133 ms: 1.70x faster                                                   |
| hexiom                  | 9.29 ms                                             | 6.18 ms: 1.50x faster                                                  |
| html5lib                | 85.1 ms                                             | 59.1 ms: 1.44x faster                                                  |
| json                    | 5.55 ms                                             | 4.61 ms: 1.20x faster                                                  |
| json_dumps              | 13.2 ms                                             | 9.51 ms: 1.38x faster                                                  |
| json_loads              | 31.1 us                                             | 23.8 us: 1.31x faster                                                  |
| logging_format          | 8.78 us                                             | 6.29 us: 1.40x faster                                                  |
| logging_silent          | 168 ns                                              | 94.1 ns: 1.78x faster                                                  |
| logging_simple          | 8.07 us                                             | 5.62 us: 1.44x faster                                                  |
| mako                    | 14.7 ms                                             | 9.56 ms: 1.54x faster                                                  |
| meteor_contest          | 114 ms                                              | 102 ms: 1.12x faster                                                   |
| nbody                   | 135 ms                                              | 93.7 ms: 1.44x faster                                                  |
| nqueens                 | 98.4 ms                                             | 82.0 ms: 1.20x faster                                                  |
| pathlib                 | 20.1 ms                                             | 17.8 ms: 1.13x faster                                                  |
| pickle_dict             | 27.2 us                                             | 31.3 us: 1.15x slower                                                  |
| pickle_list             | 4.40 us                                             | 3.97 us: 1.11x faster                                                  |
| pickle_pure_python      | 449 us                                              | 281 us: 1.60x faster                                                   |
| pidigits                | 190 ms                                              | 189 ms: 1.01x faster                                                   |
| pycparser               | 1.52 sec                                            | 1.07 sec: 1.43x faster                                                 |
| pyflate                 | 664 ms                                              | 397 ms: 1.67x faster                                                   |
| python_startup          | 9.21 ms                                             | 8.48 ms: 1.09x faster                                                  |
| python_startup_no_site  | 5.97 ms                                             | 6.12 ms: 1.03x slower                                                  |
| raytrace                | 463 ms                                              | 280 ms: 1.65x faster                                                   |
| regex_compile           | 178 ms                                              | 127 ms: 1.40x faster                                                   |
| regex_dna               | 214 ms                                              | 209 ms: 1.02x faster                                                   |
| regex_effbot            | 3.24 ms                                             | 3.55 ms: 1.09x slower                                                  |
| regex_v8                | 25.7 ms                                             | 21.0 ms: 1.22x faster                                                  |
| richards                | 68.9 ms                                             | 41.3 ms: 1.67x faster                                                  |
| scimark_fft             | 419 ms                                              | 307 ms: 1.36x faster                                                   |
| scimark_lu              | 160 ms                                              | 106 ms: 1.51x faster                                                   |
| scimark_monte_carlo     | 107 ms                                              | 65.0 ms: 1.65x faster                                                  |
| scimark_sor             | 196 ms                                              | 107 ms: 1.83x faster                                                   |
| scimark_sparse_mat_mult | 5.45 ms                                             | 4.08 ms: 1.33x faster                                                  |
| spectral_norm           | 144 ms                                              | 95.6 ms: 1.50x faster                                                  |
| sqlite_synth            | 2.92 us                                             | 2.59 us: 1.13x faster                                                  |
| sympy_expand            | 538 ms                                              | 454 ms: 1.18x faster                                                   |
| sympy_integrate         | 24.1 ms                                             | 20.3 ms: 1.18x faster                                                  |
| sympy_str               | 325 ms                                              | 280 ms: 1.16x faster                                                   |
| sympy_sum               | 184 ms                                              | 163 ms: 1.13x faster                                                   |
| telco                   | 6.60 ms                                             | 6.44 ms: 1.02x faster                                                  |
| thrift                  | 1.01 ms                                             | 748 us: 1.36x faster                                                   |
| tornado_http            | 127 ms                                              | 92.8 ms: 1.37x faster                                                  |
| unpack_sequence         | 56.1 ns                                             | 45.1 ns: 1.24x faster                                                  |
| unpickle                | 14.4 us                                             | 13.6 us: 1.06x faster                                                  |
| unpickle_list           | 4.90 us                                             | 5.13 us: 1.05x slower                                                  |
| unpickle_pure_python    | 298 us                                              | 198 us: 1.50x faster                                                   |
| xml_etree_generate      | 92.4 ms                                             | 76.3 ms: 1.21x faster                                                  |
| xml_etree_iterparse     | 110 ms                                              | 102 ms: 1.08x faster                                                   |
| xml_etree_parse         | 162 ms                                              | 147 ms: 1.10x faster                                                   |
| xml_etree_process       | 72.6 ms                                             | 52.8 ms: 1.38x faster                                                  |
| Geometric mean          | (ref)                                               | 1.31x faster                                                           |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (1) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-x86_64-python-main-3.10.4-9d38120.json: pylint
Ignored benchmarks (24) of public/results/bm-20221121-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d/bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
