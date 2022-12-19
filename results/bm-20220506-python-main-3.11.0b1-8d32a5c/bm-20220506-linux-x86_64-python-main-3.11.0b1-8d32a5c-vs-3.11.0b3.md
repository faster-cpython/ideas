| Benchmark              | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220506-linux-amd64-python-main-3.11.0b1-8d32a5c |
|------------------------|:----------------------------------------------------:|:----------------------------------------------------:|
| chameleon              | 6.67 ms                                              | 6.57 ms: 1.02x faster                                |
| chaos                  | 66.9 ms                                              | 68.6 ms: 1.02x slower                                |
| crypto_pyaes           | 73.1 ms                                              | 74.3 ms: 1.02x slower                                |
| dulwich_log            | 63.1 ms                                              | 62.8 ms: 1.00x faster                                |
| fannkuch               | 372 ms                                               | 385 ms: 1.03x slower                                 |
| hexiom                 | 6.32 ms                                              | 6.29 ms: 1.00x faster                                |
| html5lib               | 62.6 ms                                              | 60.1 ms: 1.04x faster                                |
| json                   | 4.75 ms                                              | 4.91 ms: 1.03x slower                                |
| json_dumps             | 12.5 ms                                              | 12.4 ms: 1.01x faster                                |
| json_loads             | 24.4 us                                              | 25.4 us: 1.04x slower                                |
| logging_silent         | 101 ns                                               | 98.2 ns: 1.03x faster                                |
| logging_simple         | 5.95 us                                              | 5.89 us: 1.01x faster                                |
| mako                   | 9.82 ms                                              | 9.88 ms: 1.01x slower                                |
| meteor_contest         | 104 ms                                               | 105 ms: 1.01x slower                                 |
| nbody                  | 90.6 ms                                              | 93.1 ms: 1.03x slower                                |
| nqueens                | 80.7 ms                                              | 84.7 ms: 1.05x slower                                |
| pickle_list            | 4.33 us                                              | 4.26 us: 1.02x faster                                |
| pickle_pure_python     | 302 us                                               | 305 us: 1.01x slower                                 |
| pidigits               | 194 ms                                               | 190 ms: 1.02x faster                                 |
| pycparser              | 1.10 sec                                             | 1.18 sec: 1.07x slower                               |
| python_startup         | 8.33 ms                                              | 8.25 ms: 1.01x faster                                |
| python_startup_no_site | 6.17 ms                                              | 6.16 ms: 1.00x faster                                |
| raytrace               | 292 ms                                               | 294 ms: 1.01x slower                                 |
| regex_compile          | 135 ms                                               | 135 ms: 1.01x faster                                 |
| regex_dna              | 192 ms                                               | 204 ms: 1.06x slower                                 |
| regex_effbot           | 2.92 ms                                              | 2.93 ms: 1.01x slower                                |
| regex_v8               | 21.2 ms                                              | 21.6 ms: 1.02x slower                                |
| scimark_fft            | 317 ms                                               | 325 ms: 1.02x slower                                 |
| scimark_lu             | 107 ms                                               | 109 ms: 1.02x slower                                 |
| scimark_monte_carlo    | 66.0 ms                                              | 66.5 ms: 1.01x slower                                |
| scimark_sor            | 115 ms                                               | 115 ms: 1.00x faster                                 |
| sqlite_synth           | 2.49 us                                              | 2.53 us: 1.01x slower                                |
| sympy_sum              | 159 ms                                               | 161 ms: 1.01x slower                                 |
| telco                  | 6.49 ms                                              | 6.84 ms: 1.05x slower                                |
| thrift                 | 759 us                                               | 741 us: 1.02x faster                                 |
| tornado_http           | 93.8 ms                                              | 94.6 ms: 1.01x slower                                |
| unpack_sequence        | 43.4 ns                                              | 44.3 ns: 1.02x slower                                |
| unpickle_list          | 4.89 us                                              | 5.05 us: 1.03x slower                                |
| unpickle_pure_python   | 228 us                                               | 229 us: 1.00x slower                                 |
| xml_etree_generate     | 76.3 ms                                              | 76.5 ms: 1.00x slower                                |
| xml_etree_parse        | 156 ms                                               | 157 ms: 1.01x slower                                 |
| Geometric mean         | (ref)                                                | 1.01x slower                                         |

Benchmark hidden because not significant (19): 2to3, deltablue, django_template, float, go, logging_format, pathlib, pickle, pickle_dict, pyflate, richards, scimark_sparse_mat_mult, spectral_norm, sympy_expand, sympy_integrate, sympy_str, unpickle, xml_etree_iterparse, xml_etree_process
