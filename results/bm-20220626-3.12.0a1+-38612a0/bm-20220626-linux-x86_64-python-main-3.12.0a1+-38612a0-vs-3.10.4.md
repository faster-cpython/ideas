| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220626-linux-amd64-python-main-3.12.0a1+-38612a0 |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 249 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.45 ms: 1.36x faster                                 |
| chaos                   | 107 ms                                             | 63.8 ms: 1.68x faster                                 |
| crypto_pyaes            | 116 ms                                             | 73.7 ms: 1.58x faster                                 |
| deltablue               | 7.32 ms                                            | 3.24 ms: 2.26x faster                                 |
| django_template         | 45.7 ms                                            | 31.6 ms: 1.45x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.7 ms: 1.22x faster                                 |
| fannkuch                | 483 ms                                             | 376 ms: 1.28x faster                                  |
| float                   | 107 ms                                             | 71.1 ms: 1.51x faster                                 |
| go                      | 227 ms                                             | 128 ms: 1.76x faster                                  |
| hexiom                  | 9.29 ms                                            | 5.94 ms: 1.56x faster                                 |
| html5lib                | 85.1 ms                                            | 62.0 ms: 1.37x faster                                 |
| json                    | 5.55 ms                                            | 4.72 ms: 1.18x faster                                 |
| json_dumps              | 13.2 ms                                            | 12.0 ms: 1.09x faster                                 |
| json_loads              | 31.1 us                                            | 24.5 us: 1.27x faster                                 |
| logging_format          | 8.78 us                                            | 6.40 us: 1.37x faster                                 |
| logging_silent          | 168 ns                                             | 89.6 ns: 1.87x faster                                 |
| logging_simple          | 8.07 us                                            | 5.77 us: 1.40x faster                                 |
| mako                    | 14.7 ms                                            | 9.46 ms: 1.56x faster                                 |
| meteor_contest          | 114 ms                                             | 102 ms: 1.12x faster                                  |
| nbody                   | 135 ms                                             | 94.8 ms: 1.42x faster                                 |
| nqueens                 | 98.4 ms                                            | 82.2 ms: 1.20x faster                                 |
| pathlib                 | 20.1 ms                                            | 18.1 ms: 1.11x faster                                 |
| pickle_dict             | 27.2 us                                            | 30.1 us: 1.11x slower                                 |
| pickle_list             | 4.40 us                                            | 4.15 us: 1.06x faster                                 |
| pickle_pure_python      | 449 us                                             | 294 us: 1.53x faster                                  |
| pidigits                | 190 ms                                             | 194 ms: 1.02x slower                                  |
| pycparser               | 1.52 sec                                           | 1.05 sec: 1.45x faster                                |
| pyflate                 | 664 ms                                             | 400 ms: 1.66x faster                                  |
| python_startup          | 9.21 ms                                            | 8.26 ms: 1.12x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.10 ms: 1.02x slower                                 |
| raytrace                | 463 ms                                             | 279 ms: 1.66x faster                                  |
| regex_compile           | 178 ms                                             | 128 ms: 1.39x faster                                  |
| regex_dna               | 214 ms                                             | 208 ms: 1.03x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.61 ms: 1.11x slower                                 |
| regex_v8                | 25.7 ms                                            | 21.3 ms: 1.21x faster                                 |
| richards                | 68.9 ms                                            | 45.4 ms: 1.52x faster                                 |
| scimark_fft             | 419 ms                                             | 304 ms: 1.38x faster                                  |
| scimark_lu              | 160 ms                                             | 104 ms: 1.54x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 62.4 ms: 1.72x faster                                 |
| scimark_sor             | 196 ms                                             | 110 ms: 1.78x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 3.89 ms: 1.40x faster                                 |
| spectral_norm           | 144 ms                                             | 92.8 ms: 1.55x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.57 us: 1.14x faster                                 |
| sympy_expand            | 538 ms                                             | 451 ms: 1.19x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.2 ms: 1.19x faster                                 |
| sympy_str               | 325 ms                                             | 277 ms: 1.17x faster                                  |
| sympy_sum               | 184 ms                                             | 159 ms: 1.16x faster                                  |
| telco                   | 6.60 ms                                            | 6.44 ms: 1.02x faster                                 |
| thrift                  | 1.01 ms                                            | 745 us: 1.36x faster                                  |
| tornado_http            | 127 ms                                             | 92.1 ms: 1.38x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 42.8 ns: 1.31x faster                                 |
| unpickle                | 14.4 us                                            | 13.4 us: 1.07x faster                                 |
| unpickle_pure_python    | 298 us                                             | 198 us: 1.50x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.0 ms: 1.23x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 103 ms: 1.07x faster                                  |
| xml_etree_parse         | 162 ms                                             | 155 ms: 1.05x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.0 ms: 1.40x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (2): pickle, unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
