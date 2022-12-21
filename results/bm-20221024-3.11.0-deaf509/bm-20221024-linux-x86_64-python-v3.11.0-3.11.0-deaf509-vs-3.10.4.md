| Benchmark               | bm-20220323-linux-x86_64-python-main-3.10.4-9d38120 | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|-------------------------|:---------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                              | 257 ms: 1.29x faster                                   |
| chameleon               | 8.76 ms                                             | 6.41 ms: 1.37x faster                                  |
| chaos                   | 107 ms                                              | 68.6 ms: 1.56x faster                                  |
| crypto_pyaes            | 116 ms                                              | 73.9 ms: 1.58x faster                                  |
| deltablue               | 7.32 ms                                             | 3.64 ms: 2.01x faster                                  |
| django_template         | 45.7 ms                                             | 32.5 ms: 1.41x faster                                  |
| dulwich_log             | 75.2 ms                                             | 63.9 ms: 1.18x faster                                  |
| fannkuch                | 483 ms                                              | 388 ms: 1.24x faster                                   |
| float                   | 107 ms                                              | 76.3 ms: 1.41x faster                                  |
| genshi_text             | 30.6 ms                                             | 22.1 ms: 1.38x faster                                  |
| genshi_xml              | 64.1 ms                                             | 52.1 ms: 1.23x faster                                  |
| go                      | 227 ms                                              | 143 ms: 1.58x faster                                   |
| hexiom                  | 9.29 ms                                             | 6.35 ms: 1.46x faster                                  |
| html5lib                | 85.1 ms                                             | 63.2 ms: 1.35x faster                                  |
| json                    | 5.55 ms                                             | 4.95 ms: 1.12x faster                                  |
| json_dumps              | 13.2 ms                                             | 12.7 ms: 1.04x faster                                  |
| json_loads              | 31.1 us                                             | 26.2 us: 1.19x faster                                  |
| logging_format          | 8.78 us                                             | 6.62 us: 1.33x faster                                  |
| logging_silent          | 168 ns                                              | 98.5 ns: 1.70x faster                                  |
| logging_simple          | 8.07 us                                             | 6.06 us: 1.33x faster                                  |
| mako                    | 14.7 ms                                             | 9.85 ms: 1.50x faster                                  |
| meteor_contest          | 114 ms                                              | 105 ms: 1.09x faster                                   |
| nbody                   | 135 ms                                              | 95.0 ms: 1.42x faster                                  |
| nqueens                 | 98.4 ms                                             | 85.0 ms: 1.16x faster                                  |
| pathlib                 | 20.1 ms                                             | 18.2 ms: 1.11x faster                                  |
| pickle                  | 10.2 us                                             | 9.79 us: 1.04x faster                                  |
| pickle_dict             | 27.2 us                                             | 31.4 us: 1.16x slower                                  |
| pickle_list             | 4.40 us                                             | 4.17 us: 1.05x faster                                  |
| pickle_pure_python      | 449 us                                              | 304 us: 1.48x faster                                   |
| pidigits                | 190 ms                                              | 199 ms: 1.05x slower                                   |
| pycparser               | 1.52 sec                                            | 1.17 sec: 1.30x faster                                 |
| pyflate                 | 664 ms                                              | 417 ms: 1.59x faster                                   |
| pylint                  | 512 ms                                              | 463 ms: 1.11x faster                                   |
| python_startup          | 9.21 ms                                             | 8.36 ms: 1.10x faster                                  |
| python_startup_no_site  | 5.97 ms                                             | 5.96 ms: 1.00x faster                                  |
| raytrace                | 463 ms                                              | 290 ms: 1.59x faster                                   |
| regex_compile           | 178 ms                                              | 136 ms: 1.31x faster                                   |
| regex_dna               | 214 ms                                              | 203 ms: 1.05x faster                                   |
| regex_effbot            | 3.24 ms                                             | 3.36 ms: 1.04x slower                                  |
| regex_v8                | 25.7 ms                                             | 22.3 ms: 1.15x faster                                  |
| richards                | 68.9 ms                                             | 46.2 ms: 1.49x faster                                  |
| scimark_fft             | 419 ms                                              | 329 ms: 1.27x faster                                   |
| scimark_lu              | 160 ms                                              | 107 ms: 1.49x faster                                   |
| scimark_monte_carlo     | 107 ms                                              | 68.3 ms: 1.57x faster                                  |
| scimark_sor             | 196 ms                                              | 115 ms: 1.70x faster                                   |
| scimark_sparse_mat_mult | 5.45 ms                                             | 4.40 ms: 1.24x faster                                  |
| spectral_norm           | 144 ms                                              | 99.9 ms: 1.44x faster                                  |
| sqlite_synth            | 2.92 us                                             | 2.49 us: 1.17x faster                                  |
| sympy_expand            | 538 ms                                              | 472 ms: 1.14x faster                                   |
| sympy_integrate         | 24.1 ms                                             | 20.9 ms: 1.15x faster                                  |
| sympy_str               | 325 ms                                              | 287 ms: 1.13x faster                                   |
| sympy_sum               | 184 ms                                              | 166 ms: 1.11x faster                                   |
| thrift                  | 1.01 ms                                             | 752 us: 1.35x faster                                   |
| tornado_http            | 127 ms                                              | 96.6 ms: 1.32x faster                                  |
| unpack_sequence         | 56.1 ns                                             | 43.4 ns: 1.29x faster                                  |
| unpickle                | 14.4 us                                             | 13.3 us: 1.08x faster                                  |
| unpickle_list           | 4.90 us                                             | 4.95 us: 1.01x slower                                  |
| unpickle_pure_python    | 298 us                                              | 225 us: 1.32x faster                                   |
| xml_etree_generate      | 92.4 ms                                             | 76.2 ms: 1.21x faster                                  |
| xml_etree_iterparse     | 110 ms                                              | 103 ms: 1.07x faster                                   |
| xml_etree_parse         | 162 ms                                              | 158 ms: 1.03x faster                                   |
| xml_etree_process       | 72.6 ms                                             | 53.8 ms: 1.35x faster                                  |
| Geometric mean          | (ref)                                               | 1.26x faster                                           |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (27) of ../ideas/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
