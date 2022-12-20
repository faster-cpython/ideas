| Benchmark               | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:---------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 332 ms                                              | 274 ms: 1.21x faster                                                  |
| chameleon               | 8.76 ms                                             | 7.46 ms: 1.18x faster                                                 |
| chaos                   | 107 ms                                              | 77.1 ms: 1.39x faster                                                 |
| crypto_pyaes            | 116 ms                                              | 90.2 ms: 1.29x faster                                                 |
| deltablue               | 7.32 ms                                             | 4.86 ms: 1.51x faster                                                 |
| django_template         | 45.7 ms                                             | 37.9 ms: 1.21x faster                                                 |
| dulwich_log             | 75.2 ms                                             | 68.3 ms: 1.10x faster                                                 |
| fannkuch                | 483 ms                                              | 427 ms: 1.13x faster                                                  |
| float                   | 107 ms                                              | 83.3 ms: 1.29x faster                                                 |
| genshi_text             | 30.6 ms                                             | 24.6 ms: 1.24x faster                                                 |
| genshi_xml              | 64.1 ms                                             | 56.1 ms: 1.14x faster                                                 |
| go                      | 227 ms                                              | 167 ms: 1.35x faster                                                  |
| hexiom                  | 9.29 ms                                             | 7.42 ms: 1.25x faster                                                 |
| html5lib                | 85.1 ms                                             | 71.5 ms: 1.19x faster                                                 |
| json                    | 5.55 ms                                             | 4.91 ms: 1.13x faster                                                 |
| json_dumps              | 13.2 ms                                             | 12.4 ms: 1.06x faster                                                 |
| json_loads              | 31.1 us                                             | 25.9 us: 1.20x faster                                                 |
| logging_format          | 8.78 us                                             | 6.71 us: 1.31x faster                                                 |
| logging_silent          | 168 ns                                              | 117 ns: 1.44x faster                                                  |
| logging_simple          | 8.07 us                                             | 6.07 us: 1.33x faster                                                 |
| mako                    | 14.7 ms                                             | 12.1 ms: 1.22x faster                                                 |
| meteor_contest          | 114 ms                                              | 106 ms: 1.07x faster                                                  |
| nbody                   | 135 ms                                              | 112 ms: 1.20x faster                                                  |
| nqueens                 | 98.4 ms                                             | 91.4 ms: 1.08x faster                                                 |
| pathlib                 | 20.1 ms                                             | 19.1 ms: 1.05x faster                                                 |
| pickle_dict             | 27.2 us                                             | 28.6 us: 1.05x slower                                                 |
| pickle_list             | 4.40 us                                             | 4.68 us: 1.06x slower                                                 |
| pickle_pure_python      | 449 us                                              | 364 us: 1.23x faster                                                  |
| pidigits                | 190 ms                                              | 188 ms: 1.01x faster                                                  |
| pycparser               | 1.52 sec                                            | 1.26 sec: 1.21x faster                                                |
| pyflate                 | 664 ms                                              | 541 ms: 1.23x faster                                                  |
| pylint                  | 512 ms                                              | 469 ms: 1.09x faster                                                  |
| python_startup          | 9.21 ms                                             | 14.6 ms: 1.58x slower                                                 |
| python_startup_no_site  | 5.97 ms                                             | 5.77 ms: 1.04x faster                                                 |
| raytrace                | 463 ms                                              | 326 ms: 1.42x faster                                                  |
| regex_compile           | 178 ms                                              | 145 ms: 1.23x faster                                                  |
| regex_dna               | 214 ms                                              | 219 ms: 1.02x slower                                                  |
| regex_v8                | 25.7 ms                                             | 23.7 ms: 1.08x faster                                                 |
| richards                | 68.9 ms                                             | 55.7 ms: 1.24x faster                                                 |
| scimark_fft             | 419 ms                                              | 355 ms: 1.18x faster                                                  |
| scimark_lu              | 160 ms                                              | 136 ms: 1.18x faster                                                  |
| scimark_monte_carlo     | 107 ms                                              | 78.4 ms: 1.37x faster                                                 |
| scimark_sor             | 196 ms                                              | 156 ms: 1.25x faster                                                  |
| scimark_sparse_mat_mult | 5.45 ms                                             | 4.86 ms: 1.12x faster                                                 |
| spectral_norm           | 144 ms                                              | 106 ms: 1.36x faster                                                  |
| sqlite_synth            | 2.92 us                                             | 2.76 us: 1.06x faster                                                 |
| sympy_expand            | 538 ms                                              | 505 ms: 1.06x faster                                                  |
| sympy_integrate         | 24.1 ms                                             | 22.2 ms: 1.08x faster                                                 |
| sympy_str               | 325 ms                                              | 306 ms: 1.06x faster                                                  |
| sympy_sum               | 184 ms                                              | 170 ms: 1.08x faster                                                  |
| telco                   | 6.60 ms                                             | 6.50 ms: 1.02x faster                                                 |
| thrift                  | 1.01 ms                                             | 821 us: 1.24x faster                                                  |
| tornado_http            | 127 ms                                              | 111 ms: 1.15x faster                                                  |
| unpack_sequence         | 56.1 ns                                             | 43.6 ns: 1.29x faster                                                 |
| unpickle                | 14.4 us                                             | 13.7 us: 1.05x faster                                                 |
| unpickle_list           | 4.90 us                                             | 5.13 us: 1.05x slower                                                 |
| unpickle_pure_python    | 298 us                                              | 271 us: 1.10x faster                                                  |
| xml_etree_generate      | 92.4 ms                                             | 81.6 ms: 1.13x faster                                                 |
| xml_etree_iterparse     | 110 ms                                              | 110 ms: 1.00x slower                                                  |
| xml_etree_parse         | 162 ms                                              | 158 ms: 1.03x faster                                                  |
| xml_etree_process       | 72.6 ms                                             | 59.6 ms: 1.22x faster                                                 |
| Geometric mean          | (ref)                                               | 1.15x faster                                                          |

Benchmark hidden because not significant (2): pickle, regex_effbot
Ignored benchmarks (25) of public/results/bm-20211105-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b/bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b.json: async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, gunicorn, mdp, pprint_pformat, pprint_safe_repr, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
