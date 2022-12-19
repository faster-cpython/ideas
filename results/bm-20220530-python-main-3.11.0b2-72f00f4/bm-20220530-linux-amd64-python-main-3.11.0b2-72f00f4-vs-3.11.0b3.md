| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220530-linux-amd64-python-main-3.11.0b2-72f00f4 |
|-------------------------|:----------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 256 ms: 1.00x slower                                 |
| chameleon               | 6.67 ms                                              | 6.59 ms: 1.01x faster                                |
| chaos                   | 66.9 ms                                              | 67.8 ms: 1.01x slower                                |
| crypto_pyaes            | 73.1 ms                                              | 73.8 ms: 1.01x slower                                |
| django_template         | 32.9 ms                                              | 32.4 ms: 1.02x faster                                |
| dulwich_log             | 63.1 ms                                              | 62.6 ms: 1.01x faster                                |
| fannkuch                | 372 ms                                               | 394 ms: 1.06x slower                                 |
| html5lib                | 62.6 ms                                              | 63.8 ms: 1.02x slower                                |
| json_dumps              | 12.5 ms                                              | 12.6 ms: 1.00x slower                                |
| json_loads              | 24.4 us                                              | 24.3 us: 1.00x faster                                |
| logging_silent          | 101 ns                                               | 98.1 ns: 1.03x faster                                |
| logging_simple          | 5.95 us                                              | 5.82 us: 1.02x faster                                |
| mako                    | 9.82 ms                                              | 9.71 ms: 1.01x faster                                |
| nqueens                 | 80.7 ms                                              | 82.4 ms: 1.02x slower                                |
| pathlib                 | 17.9 ms                                              | 18.2 ms: 1.02x slower                                |
| pickle                  | 9.55 us                                              | 9.61 us: 1.01x slower                                |
| pickle_dict             | 25.6 us                                              | 25.9 us: 1.01x slower                                |
| pickle_list             | 4.33 us                                              | 4.30 us: 1.01x faster                                |
| pidigits                | 194 ms                                               | 190 ms: 1.02x faster                                 |
| python_startup          | 8.33 ms                                              | 8.33 ms: 1.00x faster                                |
| python_startup_no_site  | 6.17 ms                                              | 6.17 ms: 1.00x faster                                |
| regex_compile           | 135 ms                                               | 136 ms: 1.01x slower                                 |
| regex_dna               | 192 ms                                               | 196 ms: 1.03x slower                                 |
| regex_effbot            | 2.92 ms                                              | 3.02 ms: 1.03x slower                                |
| regex_v8                | 21.2 ms                                              | 21.5 ms: 1.02x slower                                |
| richards                | 46.5 ms                                              | 45.3 ms: 1.03x faster                                |
| scimark_fft             | 317 ms                                               | 324 ms: 1.02x slower                                 |
| scimark_lu              | 107 ms                                               | 107 ms: 1.01x slower                                 |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.79 ms: 1.06x slower                                |
| spectral_norm           | 97.6 ms                                              | 96.3 ms: 1.01x faster                                |
| sympy_expand            | 467 ms                                               | 465 ms: 1.01x faster                                 |
| telco                   | 6.49 ms                                              | 6.64 ms: 1.02x slower                                |
| unpack_sequence         | 43.4 ns                                              | 43.2 ns: 1.01x faster                                |
| unpickle_list           | 4.89 us                                              | 4.98 us: 1.02x slower                                |
| xml_etree_generate      | 76.3 ms                                              | 75.8 ms: 1.01x faster                                |
| xml_etree_iterparse     | 105 ms                                               | 104 ms: 1.01x faster                                 |
| xml_etree_parse         | 156 ms                                               | 157 ms: 1.01x slower                                 |
| xml_etree_process       | 53.8 ms                                              | 53.3 ms: 1.01x faster                                |
| Geometric mean          | (ref)                                                | 1.00x slower                                         |

Benchmark hidden because not significant (22): deltablue, float, go, hexiom, json, logging_format, meteor_contest, nbody, pickle_pure_python, pycparser, pyflate, raytrace, scimark_monte_carlo, scimark_sor, sqlite_synth, sympy_integrate, sympy_str, sympy_sum, thrift, tornado_http, unpickle, unpickle_pure_python
