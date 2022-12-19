| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220611-linux-amd64-python-main-3.12.0a1+-733e15f |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 251 ms: 1.02x faster                                  |
| chameleon               | 6.67 ms                                              | 6.40 ms: 1.04x faster                                 |
| chaos                   | 66.9 ms                                              | 68.0 ms: 1.02x slower                                 |
| crypto_pyaes            | 73.1 ms                                              | 74.0 ms: 1.01x slower                                 |
| deltablue               | 3.62 ms                                              | 3.51 ms: 1.03x faster                                 |
| django_template         | 32.9 ms                                              | 31.2 ms: 1.05x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.9 ms: 1.02x faster                                 |
| fannkuch                | 372 ms                                               | 382 ms: 1.03x slower                                  |
| float                   | 72.9 ms                                              | 71.0 ms: 1.03x faster                                 |
| go                      | 137 ms                                               | 131 ms: 1.04x faster                                  |
| hexiom                  | 6.32 ms                                              | 6.17 ms: 1.02x faster                                 |
| json_dumps              | 12.5 ms                                              | 12.0 ms: 1.04x faster                                 |
| json_loads              | 24.4 us                                              | 25.1 us: 1.03x slower                                 |
| logging_format          | 6.44 us                                              | 6.36 us: 1.01x faster                                 |
| logging_silent          | 101 ns                                               | 99.2 ns: 1.02x faster                                 |
| logging_simple          | 5.95 us                                              | 5.84 us: 1.02x faster                                 |
| mako                    | 9.82 ms                                              | 9.74 ms: 1.01x faster                                 |
| meteor_contest          | 104 ms                                               | 102 ms: 1.02x faster                                  |
| nqueens                 | 80.7 ms                                              | 83.4 ms: 1.03x slower                                 |
| pickle                  | 9.55 us                                              | 10.3 us: 1.07x slower                                 |
| pickle_dict             | 25.6 us                                              | 30.6 us: 1.19x slower                                 |
| pickle_list             | 4.33 us                                              | 4.11 us: 1.05x faster                                 |
| pickle_pure_python      | 302 us                                               | 293 us: 1.03x faster                                  |
| pidigits                | 194 ms                                               | 197 ms: 1.02x slower                                  |
| pycparser               | 1.10 sec                                             | 1.07 sec: 1.03x faster                                |
| pyflate                 | 411 ms                                               | 400 ms: 1.03x faster                                  |
| python_startup          | 8.33 ms                                              | 8.26 ms: 1.01x faster                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.11 ms: 1.01x faster                                 |
| raytrace                | 292 ms                                               | 281 ms: 1.04x faster                                  |
| regex_compile           | 135 ms                                               | 132 ms: 1.02x faster                                  |
| regex_dna               | 192 ms                                               | 198 ms: 1.03x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.01 ms: 1.03x slower                                 |
| regex_v8                | 21.2 ms                                              | 21.3 ms: 1.00x slower                                 |
| richards                | 46.5 ms                                              | 43.6 ms: 1.07x faster                                 |
| scimark_fft             | 317 ms                                               | 315 ms: 1.01x faster                                  |
| scimark_lu              | 107 ms                                               | 102 ms: 1.05x faster                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 66.7 ms: 1.01x slower                                 |
| scimark_sor             | 115 ms                                               | 110 ms: 1.04x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.36 ms: 1.04x faster                                 |
| spectral_norm           | 97.6 ms                                              | 95.3 ms: 1.02x faster                                 |
| sympy_expand            | 467 ms                                               | 457 ms: 1.02x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.2 ms: 1.01x faster                                 |
| sympy_str               | 284 ms                                               | 283 ms: 1.01x faster                                  |
| thrift                  | 759 us                                               | 741 us: 1.02x faster                                  |
| tornado_http            | 93.8 ms                                              | 91.3 ms: 1.03x faster                                 |
| unpickle                | 13.3 us                                              | 14.1 us: 1.06x slower                                 |
| unpickle_pure_python    | 228 us                                               | 212 us: 1.07x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.4 ms: 1.01x faster                                 |
| xml_etree_parse         | 156 ms                                               | 159 ms: 1.02x slower                                  |
| xml_etree_process       | 53.8 ms                                              | 52.1 ms: 1.03x faster                                 |
| Geometric mean          | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (10): html5lib, json, nbody, pathlib, sqlite_synth, sympy_sum, telco, unpack_sequence, unpickle_list, xml_etree_iterparse
