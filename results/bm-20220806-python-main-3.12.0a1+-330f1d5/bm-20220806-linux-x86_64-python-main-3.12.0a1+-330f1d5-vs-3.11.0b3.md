| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220806-linux-amd64-python-main-3.12.0a1+-330f1d5 |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 248 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.50 ms: 1.03x faster                                 |
| crypto_pyaes            | 73.1 ms                                              | 72.6 ms: 1.01x faster                                 |
| deltablue               | 3.62 ms                                              | 3.21 ms: 1.13x faster                                 |
| django_template         | 32.9 ms                                              | 32.5 ms: 1.01x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.2 ms: 1.03x faster                                 |
| fannkuch                | 372 ms                                               | 374 ms: 1.01x slower                                  |
| float                   | 72.9 ms                                              | 74.1 ms: 1.02x slower                                 |
| go                      | 137 ms                                               | 131 ms: 1.04x faster                                  |
| hexiom                  | 6.32 ms                                              | 5.98 ms: 1.06x faster                                 |
| json                    | 4.75 ms                                              | 4.70 ms: 1.01x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.51 ms: 1.31x faster                                 |
| logging_format          | 6.44 us                                              | 6.34 us: 1.01x faster                                 |
| logging_silent          | 101 ns                                               | 89.9 ns: 1.13x faster                                 |
| logging_simple          | 5.95 us                                              | 5.72 us: 1.04x faster                                 |
| mako                    | 9.82 ms                                              | 9.50 ms: 1.03x faster                                 |
| meteor_contest          | 104 ms                                               | 101 ms: 1.02x faster                                  |
| nbody                   | 90.6 ms                                              | 91.3 ms: 1.01x slower                                 |
| nqueens                 | 80.7 ms                                              | 79.2 ms: 1.02x faster                                 |
| pathlib                 | 17.9 ms                                              | 17.6 ms: 1.02x faster                                 |
| pickle                  | 9.55 us                                              | 10.4 us: 1.08x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.9 us: 1.25x slower                                 |
| pickle_list             | 4.33 us                                              | 4.26 us: 1.01x faster                                 |
| pickle_pure_python      | 302 us                                               | 288 us: 1.05x faster                                  |
| pidigits                | 194 ms                                               | 194 ms: 1.00x faster                                  |
| pycparser               | 1.10 sec                                             | 1.04 sec: 1.06x faster                                |
| pyflate                 | 411 ms                                               | 393 ms: 1.05x faster                                  |
| python_startup          | 8.33 ms                                              | 8.15 ms: 1.02x faster                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.01 ms: 1.03x faster                                 |
| raytrace                | 292 ms                                               | 278 ms: 1.05x faster                                  |
| regex_compile           | 135 ms                                               | 127 ms: 1.07x faster                                  |
| regex_dna               | 192 ms                                               | 203 ms: 1.06x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.50 ms: 1.20x slower                                 |
| regex_v8                | 21.2 ms                                              | 20.8 ms: 1.02x faster                                 |
| richards                | 46.5 ms                                              | 44.5 ms: 1.05x faster                                 |
| scimark_fft             | 317 ms                                               | 311 ms: 1.02x faster                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 64.2 ms: 1.03x faster                                 |
| scimark_sor             | 115 ms                                               | 110 ms: 1.04x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 3.91 ms: 1.16x faster                                 |
| spectral_norm           | 97.6 ms                                              | 93.8 ms: 1.04x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.59 us: 1.04x slower                                 |
| sympy_expand            | 467 ms                                               | 461 ms: 1.01x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.3 ms: 1.01x faster                                 |
| sympy_str               | 284 ms                                               | 282 ms: 1.01x faster                                  |
| sympy_sum               | 159 ms                                               | 160 ms: 1.01x slower                                  |
| telco                   | 6.49 ms                                              | 6.41 ms: 1.01x faster                                 |
| thrift                  | 759 us                                               | 748 us: 1.01x faster                                  |
| tornado_http            | 93.8 ms                                              | 91.7 ms: 1.02x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 45.9 ns: 1.06x slower                                 |
| unpickle_list           | 4.89 us                                              | 5.06 us: 1.04x slower                                 |
| unpickle_pure_python    | 228 us                                               | 199 us: 1.14x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.0 ms: 1.02x faster                                 |
| xml_etree_process       | 53.8 ms                                              | 52.2 ms: 1.03x faster                                 |
| Geometric mean          | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (7): chaos, html5lib, json_loads, scimark_lu, unpickle, xml_etree_iterparse, xml_etree_parse
