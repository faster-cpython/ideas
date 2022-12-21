| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220717-linux-amd64-python-main-3.12.0a1+-c20186c |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 249 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.28 ms: 1.40x faster                                 |
| chaos                   | 107 ms                                             | 66.2 ms: 1.62x faster                                 |
| crypto_pyaes            | 116 ms                                             | 72.9 ms: 1.60x faster                                 |
| deltablue               | 7.32 ms                                            | 3.21 ms: 2.28x faster                                 |
| django_template         | 45.7 ms                                            | 32.1 ms: 1.43x faster                                 |
| dulwich_log             | 75.2 ms                                            | 60.8 ms: 1.24x faster                                 |
| fannkuch                | 483 ms                                             | 373 ms: 1.29x faster                                  |
| float                   | 107 ms                                             | 72.0 ms: 1.49x faster                                 |
| go                      | 227 ms                                             | 133 ms: 1.71x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.05 ms: 1.54x faster                                 |
| html5lib                | 85.1 ms                                            | 62.8 ms: 1.35x faster                                 |
| json                    | 5.55 ms                                            | 4.61 ms: 1.20x faster                                 |
| json_dumps              | 13.2 ms                                            | 11.9 ms: 1.11x faster                                 |
| json_loads              | 31.1 us                                            | 24.3 us: 1.28x faster                                 |
| logging_format          | 8.78 us                                            | 6.22 us: 1.41x faster                                 |
| logging_silent          | 168 ns                                             | 91.9 ns: 1.83x faster                                 |
| logging_simple          | 8.07 us                                            | 5.61 us: 1.44x faster                                 |
| mako                    | 14.7 ms                                            | 9.33 ms: 1.58x faster                                 |
| meteor_contest          | 114 ms                                             | 101 ms: 1.12x faster                                  |
| nbody                   | 135 ms                                             | 88.8 ms: 1.52x faster                                 |
| nqueens                 | 98.4 ms                                            | 78.8 ms: 1.25x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.7 ms: 1.14x faster                                 |
| pickle_dict             | 27.2 us                                            | 30.6 us: 1.13x slower                                 |
| pickle_list             | 4.40 us                                            | 4.24 us: 1.04x faster                                 |
| pickle_pure_python      | 449 us                                             | 286 us: 1.57x faster                                  |
| pidigits                | 190 ms                                             | 190 ms: 1.00x faster                                  |
| pycparser               | 1.52 sec                                           | 1.05 sec: 1.45x faster                                |
| pyflate                 | 664 ms                                             | 401 ms: 1.65x faster                                  |
| python_startup          | 9.21 ms                                            | 8.17 ms: 1.13x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.02 ms: 1.01x slower                                 |
| raytrace                | 463 ms                                             | 285 ms: 1.63x faster                                  |
| regex_compile           | 178 ms                                             | 127 ms: 1.40x faster                                  |
| regex_dna               | 214 ms                                             | 197 ms: 1.09x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.47 ms: 1.07x slower                                 |
| regex_v8                | 25.7 ms                                            | 20.9 ms: 1.23x faster                                 |
| richards                | 68.9 ms                                            | 44.7 ms: 1.54x faster                                 |
| scimark_fft             | 419 ms                                             | 313 ms: 1.34x faster                                  |
| scimark_lu              | 160 ms                                             | 105 ms: 1.52x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 65.1 ms: 1.65x faster                                 |
| scimark_sor             | 196 ms                                             | 117 ms: 1.67x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.04 ms: 1.35x faster                                 |
| spectral_norm           | 144 ms                                             | 93.4 ms: 1.54x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.60 us: 1.12x faster                                 |
| sympy_expand            | 538 ms                                             | 452 ms: 1.19x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.1 ms: 1.20x faster                                 |
| sympy_str               | 325 ms                                             | 278 ms: 1.17x faster                                  |
| sympy_sum               | 184 ms                                             | 159 ms: 1.16x faster                                  |
| telco                   | 6.60 ms                                            | 6.50 ms: 1.02x faster                                 |
| thrift                  | 1.01 ms                                            | 739 us: 1.37x faster                                  |
| tornado_http            | 127 ms                                             | 91.3 ms: 1.39x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 43.2 ns: 1.30x faster                                 |
| unpickle                | 14.4 us                                            | 13.5 us: 1.06x faster                                 |
| unpickle_list           | 4.90 us                                            | 5.08 us: 1.04x slower                                 |
| unpickle_pure_python    | 298 us                                             | 202 us: 1.48x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.2 ms: 1.23x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 106 ms: 1.04x faster                                  |
| xml_etree_parse         | 162 ms                                             | 160 ms: 1.02x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.2 ms: 1.39x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
