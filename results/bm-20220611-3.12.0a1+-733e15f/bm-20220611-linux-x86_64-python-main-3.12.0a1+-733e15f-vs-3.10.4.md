| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220611-linux-amd64-python-main-3.12.0a1+-733e15f |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 251 ms: 1.33x faster                                  |
| chameleon               | 8.76 ms                                            | 6.40 ms: 1.37x faster                                 |
| chaos                   | 107 ms                                             | 68.0 ms: 1.57x faster                                 |
| crypto_pyaes            | 116 ms                                             | 74.0 ms: 1.57x faster                                 |
| deltablue               | 7.32 ms                                            | 3.51 ms: 2.09x faster                                 |
| django_template         | 45.7 ms                                            | 31.2 ms: 1.46x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.9 ms: 1.21x faster                                 |
| fannkuch                | 483 ms                                             | 382 ms: 1.26x faster                                  |
| float                   | 107 ms                                             | 71.0 ms: 1.51x faster                                 |
| go                      | 227 ms                                             | 131 ms: 1.72x faster                                  |
| hexiom                  | 9.29 ms                                            | 6.17 ms: 1.50x faster                                 |
| html5lib                | 85.1 ms                                            | 63.4 ms: 1.34x faster                                 |
| json                    | 5.55 ms                                            | 4.78 ms: 1.16x faster                                 |
| json_dumps              | 13.2 ms                                            | 12.0 ms: 1.09x faster                                 |
| json_loads              | 31.1 us                                            | 25.1 us: 1.24x faster                                 |
| logging_format          | 8.78 us                                            | 6.36 us: 1.38x faster                                 |
| logging_silent          | 168 ns                                             | 99.2 ns: 1.69x faster                                 |
| logging_simple          | 8.07 us                                            | 5.84 us: 1.38x faster                                 |
| mako                    | 14.7 ms                                            | 9.74 ms: 1.51x faster                                 |
| meteor_contest          | 114 ms                                             | 102 ms: 1.12x faster                                  |
| nbody                   | 135 ms                                             | 91.3 ms: 1.48x faster                                 |
| nqueens                 | 98.4 ms                                            | 83.4 ms: 1.18x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.8 ms: 1.13x faster                                 |
| pickle_dict             | 27.2 us                                            | 30.6 us: 1.13x slower                                 |
| pickle_list             | 4.40 us                                            | 4.11 us: 1.07x faster                                 |
| pickle_pure_python      | 449 us                                             | 293 us: 1.53x faster                                  |
| pidigits                | 190 ms                                             | 197 ms: 1.03x slower                                  |
| pycparser               | 1.52 sec                                           | 1.07 sec: 1.43x faster                                |
| pyflate                 | 664 ms                                             | 400 ms: 1.66x faster                                  |
| python_startup          | 9.21 ms                                            | 8.26 ms: 1.12x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.11 ms: 1.02x slower                                 |
| raytrace                | 463 ms                                             | 281 ms: 1.65x faster                                  |
| regex_compile           | 178 ms                                             | 132 ms: 1.34x faster                                  |
| regex_dna               | 214 ms                                             | 198 ms: 1.08x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.01 ms: 1.08x faster                                 |
| regex_v8                | 25.7 ms                                            | 21.3 ms: 1.21x faster                                 |
| richards                | 68.9 ms                                            | 43.6 ms: 1.58x faster                                 |
| scimark_fft             | 419 ms                                             | 315 ms: 1.33x faster                                  |
| scimark_lu              | 160 ms                                             | 102 ms: 1.58x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 66.7 ms: 1.61x faster                                 |
| scimark_sor             | 196 ms                                             | 110 ms: 1.78x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.36 ms: 1.25x faster                                 |
| spectral_norm           | 144 ms                                             | 95.3 ms: 1.51x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.50 us: 1.17x faster                                 |
| sympy_expand            | 538 ms                                             | 457 ms: 1.18x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.2 ms: 1.19x faster                                 |
| sympy_str               | 325 ms                                             | 283 ms: 1.15x faster                                  |
| sympy_sum               | 184 ms                                             | 159 ms: 1.16x faster                                  |
| telco                   | 6.60 ms                                            | 6.46 ms: 1.02x faster                                 |
| thrift                  | 1.01 ms                                            | 741 us: 1.37x faster                                  |
| tornado_http            | 127 ms                                             | 91.3 ms: 1.40x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 43.6 ns: 1.29x faster                                 |
| unpickle_pure_python    | 298 us                                             | 212 us: 1.40x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.4 ms: 1.23x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 104 ms: 1.05x faster                                  |
| xml_etree_parse         | 162 ms                                             | 159 ms: 1.02x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.1 ms: 1.39x faster                                 |
| Geometric mean          | (ref)                                              | 1.30x faster                                          |

Benchmark hidden because not significant (3): pickle, unpickle, unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
