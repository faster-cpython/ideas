| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220702-linux-amd64-python-main-3.12.0a1+-7db1d2e |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 248 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.39 ms: 1.04x faster                                 |
| chaos                   | 66.9 ms                                              | 65.2 ms: 1.03x faster                                 |
| deltablue               | 3.62 ms                                              | 3.20 ms: 1.13x faster                                 |
| django_template         | 32.9 ms                                              | 32.0 ms: 1.03x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.2 ms: 1.03x faster                                 |
| float                   | 72.9 ms                                              | 69.9 ms: 1.04x faster                                 |
| go                      | 137 ms                                               | 130 ms: 1.05x faster                                  |
| hexiom                  | 6.32 ms                                              | 5.88 ms: 1.07x faster                                 |
| json                    | 4.75 ms                                              | 4.70 ms: 1.01x faster                                 |
| json_dumps              | 12.5 ms                                              | 11.9 ms: 1.05x faster                                 |
| logging_format          | 6.44 us                                              | 6.26 us: 1.03x faster                                 |
| logging_silent          | 101 ns                                               | 91.7 ns: 1.11x faster                                 |
| logging_simple          | 5.95 us                                              | 5.74 us: 1.04x faster                                 |
| mako                    | 9.82 ms                                              | 9.55 ms: 1.03x faster                                 |
| meteor_contest          | 104 ms                                               | 101 ms: 1.03x faster                                  |
| nbody                   | 90.6 ms                                              | 89.9 ms: 1.01x faster                                 |
| nqueens                 | 80.7 ms                                              | 81.0 ms: 1.00x slower                                 |
| pickle                  | 9.55 us                                              | 10.5 us: 1.10x slower                                 |
| pickle_dict             | 25.6 us                                              | 30.7 us: 1.20x slower                                 |
| pickle_list             | 4.33 us                                              | 4.28 us: 1.01x faster                                 |
| pickle_pure_python      | 302 us                                               | 282 us: 1.07x faster                                  |
| pidigits                | 194 ms                                               | 189 ms: 1.02x faster                                  |
| pycparser               | 1.10 sec                                             | 1.08 sec: 1.02x faster                                |
| pyflate                 | 411 ms                                               | 389 ms: 1.06x faster                                  |
| python_startup          | 8.33 ms                                              | 8.22 ms: 1.01x faster                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.07 ms: 1.02x faster                                 |
| raytrace                | 292 ms                                               | 282 ms: 1.04x faster                                  |
| regex_compile           | 135 ms                                               | 125 ms: 1.09x faster                                  |
| regex_dna               | 192 ms                                               | 197 ms: 1.03x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.49 ms: 1.20x slower                                 |
| regex_v8                | 21.2 ms                                              | 22.0 ms: 1.04x slower                                 |
| richards                | 46.5 ms                                              | 44.6 ms: 1.04x faster                                 |
| scimark_fft             | 317 ms                                               | 309 ms: 1.03x faster                                  |
| scimark_lu              | 107 ms                                               | 105 ms: 1.02x faster                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 62.8 ms: 1.05x faster                                 |
| scimark_sor             | 115 ms                                               | 111 ms: 1.04x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.21 ms: 1.08x faster                                 |
| spectral_norm           | 97.6 ms                                              | 94.3 ms: 1.04x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.59 us: 1.04x slower                                 |
| sympy_expand            | 467 ms                                               | 450 ms: 1.04x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.1 ms: 1.02x faster                                 |
| sympy_str               | 284 ms                                               | 276 ms: 1.03x faster                                  |
| telco                   | 6.49 ms                                              | 6.59 ms: 1.02x slower                                 |
| thrift                  | 759 us                                               | 744 us: 1.02x faster                                  |
| tornado_http            | 93.8 ms                                              | 91.4 ms: 1.03x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 45.5 ns: 1.05x slower                                 |
| unpickle_list           | 4.89 us                                              | 4.93 us: 1.01x slower                                 |
| unpickle_pure_python    | 228 us                                               | 198 us: 1.15x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.0 ms: 1.02x faster                                 |
| xml_etree_iterparse     | 105 ms                                               | 102 ms: 1.02x faster                                  |
| xml_etree_process       | 53.8 ms                                              | 52.0 ms: 1.03x faster                                 |
| Geometric mean          | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (8): crypto_pyaes, fannkuch, html5lib, json_loads, pathlib, sympy_sum, unpickle, xml_etree_parse
