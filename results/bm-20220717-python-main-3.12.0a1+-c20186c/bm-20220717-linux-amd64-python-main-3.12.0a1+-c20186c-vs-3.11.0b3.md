| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220717-linux-amd64-python-main-3.12.0a1+-c20186c |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 249 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.28 ms: 1.06x faster                                 |
| chaos                   | 66.9 ms                                              | 66.2 ms: 1.01x faster                                 |
| deltablue               | 3.62 ms                                              | 3.21 ms: 1.13x faster                                 |
| django_template         | 32.9 ms                                              | 32.1 ms: 1.03x faster                                 |
| dulwich_log             | 63.1 ms                                              | 60.8 ms: 1.04x faster                                 |
| float                   | 72.9 ms                                              | 72.0 ms: 1.01x faster                                 |
| go                      | 137 ms                                               | 133 ms: 1.03x faster                                  |
| hexiom                  | 6.32 ms                                              | 6.05 ms: 1.04x faster                                 |
| json                    | 4.75 ms                                              | 4.61 ms: 1.03x faster                                 |
| json_dumps              | 12.5 ms                                              | 11.9 ms: 1.05x faster                                 |
| json_loads              | 24.4 us                                              | 24.3 us: 1.00x faster                                 |
| logging_format          | 6.44 us                                              | 6.22 us: 1.04x faster                                 |
| logging_silent          | 101 ns                                               | 91.9 ns: 1.10x faster                                 |
| logging_simple          | 5.95 us                                              | 5.61 us: 1.06x faster                                 |
| mako                    | 9.82 ms                                              | 9.33 ms: 1.05x faster                                 |
| meteor_contest          | 104 ms                                               | 101 ms: 1.02x faster                                  |
| nbody                   | 90.6 ms                                              | 88.8 ms: 1.02x faster                                 |
| nqueens                 | 80.7 ms                                              | 78.8 ms: 1.02x faster                                 |
| pathlib                 | 17.9 ms                                              | 17.7 ms: 1.01x faster                                 |
| pickle                  | 9.55 us                                              | 10.3 us: 1.08x slower                                 |
| pickle_dict             | 25.6 us                                              | 30.6 us: 1.20x slower                                 |
| pickle_list             | 4.33 us                                              | 4.24 us: 1.02x faster                                 |
| pickle_pure_python      | 302 us                                               | 286 us: 1.05x faster                                  |
| pidigits                | 194 ms                                               | 190 ms: 1.02x faster                                  |
| pycparser               | 1.10 sec                                             | 1.05 sec: 1.05x faster                                |
| pyflate                 | 411 ms                                               | 401 ms: 1.03x faster                                  |
| python_startup          | 8.33 ms                                              | 8.17 ms: 1.02x faster                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.02 ms: 1.03x faster                                 |
| raytrace                | 292 ms                                               | 285 ms: 1.03x faster                                  |
| regex_compile           | 135 ms                                               | 127 ms: 1.06x faster                                  |
| regex_dna               | 192 ms                                               | 197 ms: 1.03x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.47 ms: 1.19x slower                                 |
| regex_v8                | 21.2 ms                                              | 20.9 ms: 1.01x faster                                 |
| richards                | 46.5 ms                                              | 44.7 ms: 1.04x faster                                 |
| scimark_fft             | 317 ms                                               | 313 ms: 1.01x faster                                  |
| scimark_lu              | 107 ms                                               | 105 ms: 1.01x faster                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 65.1 ms: 1.01x faster                                 |
| scimark_sor             | 115 ms                                               | 117 ms: 1.02x slower                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.04 ms: 1.12x faster                                 |
| spectral_norm           | 97.6 ms                                              | 93.4 ms: 1.05x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.60 us: 1.04x slower                                 |
| sympy_expand            | 467 ms                                               | 452 ms: 1.03x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.1 ms: 1.02x faster                                 |
| sympy_str               | 284 ms                                               | 278 ms: 1.02x faster                                  |
| thrift                  | 759 us                                               | 739 us: 1.03x faster                                  |
| tornado_http            | 93.8 ms                                              | 91.3 ms: 1.03x faster                                 |
| unpickle_list           | 4.89 us                                              | 5.08 us: 1.04x slower                                 |
| unpickle_pure_python    | 228 us                                               | 202 us: 1.13x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.2 ms: 1.01x faster                                 |
| xml_etree_iterparse     | 105 ms                                               | 106 ms: 1.01x slower                                  |
| xml_etree_parse         | 156 ms                                               | 160 ms: 1.03x slower                                  |
| xml_etree_process       | 53.8 ms                                              | 52.2 ms: 1.03x faster                                 |
| Geometric mean          | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (7): crypto_pyaes, fannkuch, html5lib, sympy_sum, telco, unpack_sequence, unpickle
