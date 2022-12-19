| Benchmark               | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 |
|-------------------------|:-----------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 256 ms                                                | 257 ms: 1.01x slower                                   |
| chameleon               | 6.67 ms                                               | 6.41 ms: 1.04x faster                                  |
| chaos                   | 66.9 ms                                               | 68.6 ms: 1.03x slower                                  |
| crypto_pyaes            | 73.1 ms                                               | 73.9 ms: 1.01x slower                                  |
| django_template         | 32.9 ms                                               | 32.5 ms: 1.01x faster                                  |
| dulwich_log             | 63.1 ms                                               | 63.9 ms: 1.01x slower                                  |
| fannkuch                | 372 ms                                                | 388 ms: 1.04x slower                                   |
| float                   | 72.9 ms                                               | 76.3 ms: 1.05x slower                                  |
| go                      | 137 ms                                                | 143 ms: 1.05x slower                                   |
| hexiom                  | 6.32 ms                                               | 6.35 ms: 1.01x slower                                  |
| json                    | 4.75 ms                                               | 4.95 ms: 1.04x slower                                  |
| json_dumps              | 12.5 ms                                               | 12.7 ms: 1.01x slower                                  |
| json_loads              | 24.4 us                                               | 26.2 us: 1.08x slower                                  |
| logging_format          | 6.44 us                                               | 6.62 us: 1.03x slower                                  |
| logging_silent          | 101 ns                                                | 98.5 ns: 1.03x faster                                  |
| logging_simple          | 5.95 us                                               | 6.06 us: 1.02x slower                                  |
| mako                    | 9.82 ms                                               | 9.85 ms: 1.00x slower                                  |
| meteor_contest          | 104 ms                                                | 105 ms: 1.01x slower                                   |
| nbody                   | 90.6 ms                                               | 95.0 ms: 1.05x slower                                  |
| nqueens                 | 80.7 ms                                               | 85.0 ms: 1.05x slower                                  |
| pathlib                 | 17.9 ms                                               | 18.2 ms: 1.02x slower                                  |
| pickle                  | 9.55 us                                               | 9.79 us: 1.02x slower                                  |
| pickle_dict             | 25.6 us                                               | 31.4 us: 1.23x slower                                  |
| pickle_list             | 4.33 us                                               | 4.17 us: 1.04x faster                                  |
| pickle_pure_python      | 302 us                                                | 304 us: 1.01x slower                                   |
| pidigits                | 194 ms                                                | 199 ms: 1.03x slower                                   |
| pycparser               | 1.10 sec                                              | 1.17 sec: 1.06x slower                                 |
| pyflate                 | 411 ms                                                | 417 ms: 1.01x slower                                   |
| python_startup          | 8.33 ms                                               | 8.36 ms: 1.00x slower                                  |
| python_startup_no_site  | 6.17 ms                                               | 5.96 ms: 1.04x faster                                  |
| raytrace                | 292 ms                                                | 290 ms: 1.01x faster                                   |
| regex_compile           | 135 ms                                                | 136 ms: 1.01x slower                                   |
| regex_dna               | 192 ms                                                | 203 ms: 1.06x slower                                   |
| regex_effbot            | 2.92 ms                                               | 3.36 ms: 1.15x slower                                  |
| regex_v8                | 21.2 ms                                               | 22.3 ms: 1.05x slower                                  |
| richards                | 46.5 ms                                               | 46.2 ms: 1.01x faster                                  |
| scimark_fft             | 317 ms                                                | 329 ms: 1.04x slower                                   |
| scimark_lu              | 107 ms                                                | 107 ms: 1.01x slower                                   |
| scimark_monte_carlo     | 66.0 ms                                               | 68.3 ms: 1.04x slower                                  |
| scimark_sparse_mat_mult | 4.54 ms                                               | 4.40 ms: 1.03x faster                                  |
| spectral_norm           | 97.6 ms                                               | 99.9 ms: 1.02x slower                                  |
| sympy_expand            | 467 ms                                                | 472 ms: 1.01x slower                                   |
| sympy_integrate         | 20.5 ms                                               | 20.9 ms: 1.02x slower                                  |
| sympy_str               | 284 ms                                                | 287 ms: 1.01x slower                                   |
| sympy_sum               | 159 ms                                                | 166 ms: 1.04x slower                                   |
| telco                   | 6.49 ms                                               | 6.62 ms: 1.02x slower                                  |
| thrift                  | 759 us                                                | 752 us: 1.01x faster                                   |
| tornado_http            | 93.8 ms                                               | 96.6 ms: 1.03x slower                                  |
| unpickle_list           | 4.89 us                                               | 4.95 us: 1.01x slower                                  |
| unpickle_pure_python    | 228 us                                                | 225 us: 1.01x faster                                   |
| xml_etree_iterparse     | 105 ms                                                | 103 ms: 1.02x faster                                   |
| xml_etree_parse         | 156 ms                                                | 158 ms: 1.02x slower                                   |
| Geometric mean          | (ref)                                                 | 1.02x slower                                           |

Benchmark hidden because not significant (8): deltablue, html5lib, scimark_sor, sqlite_synth, unpack_sequence, unpickle, xml_etree_generate, xml_etree_process
Ignored benchmarks (30) of ../ideas/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
