| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220113-linux-amd64-python-main-3.11.0a4-9471106 |
|-------------------------|:--------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 264 ms: 1.26x faster                                 |
| chameleon               | 8.76 ms                                            | 7.55 ms: 1.16x faster                                |
| chaos                   | 107 ms                                             | 72.7 ms: 1.47x faster                                |
| crypto_pyaes            | 116 ms                                             | 83.8 ms: 1.39x faster                                |
| deltablue               | 7.32 ms                                            | 4.16 ms: 1.76x faster                                |
| django_template         | 45.7 ms                                            | 35.2 ms: 1.30x faster                                |
| dulwich_log             | 75.2 ms                                            | 65.8 ms: 1.14x faster                                |
| fannkuch                | 483 ms                                             | 392 ms: 1.23x faster                                 |
| float                   | 107 ms                                             | 78.0 ms: 1.38x faster                                |
| go                      | 227 ms                                             | 148 ms: 1.53x faster                                 |
| hexiom                  | 9.29 ms                                            | 6.63 ms: 1.40x faster                                |
| html5lib                | 85.1 ms                                            | 68.1 ms: 1.25x faster                                |
| json                    | 5.55 ms                                            | 4.74 ms: 1.17x faster                                |
| json_dumps              | 13.2 ms                                            | 12.4 ms: 1.06x faster                                |
| json_loads              | 31.1 us                                            | 25.1 us: 1.24x faster                                |
| logging_format          | 8.78 us                                            | 6.51 us: 1.35x faster                                |
| logging_silent          | 168 ns                                             | 113 ns: 1.48x faster                                 |
| logging_simple          | 8.07 us                                            | 5.95 us: 1.36x faster                                |
| mako                    | 14.7 ms                                            | 11.5 ms: 1.28x faster                                |
| meteor_contest          | 114 ms                                             | 103 ms: 1.11x faster                                 |
| nbody                   | 135 ms                                             | 95.1 ms: 1.42x faster                                |
| nqueens                 | 98.4 ms                                            | 84.0 ms: 1.17x faster                                |
| pathlib                 | 20.1 ms                                            | 19.1 ms: 1.05x faster                                |
| pickle                  | 10.2 us                                            | 9.95 us: 1.03x faster                                |
| pickle_dict             | 27.2 us                                            | 26.8 us: 1.01x faster                                |
| pickle_list             | 4.40 us                                            | 4.37 us: 1.01x faster                                |
| pickle_pure_python      | 449 us                                             | 329 us: 1.36x faster                                 |
| pidigits                | 190 ms                                             | 194 ms: 1.02x slower                                 |
| pycparser               | 1.52 sec                                           | 1.17 sec: 1.31x faster                               |
| pyflate                 | 664 ms                                             | 444 ms: 1.50x faster                                 |
| python_startup          | 9.21 ms                                            | 8.07 ms: 1.14x faster                                |
| python_startup_no_site  | 5.97 ms                                            | 5.85 ms: 1.02x faster                                |
| raytrace                | 463 ms                                             | 320 ms: 1.44x faster                                 |
| regex_compile           | 178 ms                                             | 138 ms: 1.29x faster                                 |
| regex_dna               | 214 ms                                             | 212 ms: 1.01x faster                                 |
| regex_v8                | 25.7 ms                                            | 24.8 ms: 1.03x faster                                |
| richards                | 68.9 ms                                            | 51.5 ms: 1.34x faster                                |
| scimark_fft             | 419 ms                                             | 330 ms: 1.27x faster                                 |
| scimark_lu              | 160 ms                                             | 114 ms: 1.41x faster                                 |
| scimark_monte_carlo     | 107 ms                                             | 72.7 ms: 1.48x faster                                |
| scimark_sor             | 196 ms                                             | 124 ms: 1.57x faster                                 |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.69 ms: 1.16x faster                                |
| spectral_norm           | 144 ms                                             | 99.0 ms: 1.45x faster                                |
| sqlite_synth            | 2.92 us                                            | 2.73 us: 1.07x faster                                |
| sympy_expand            | 538 ms                                             | 506 ms: 1.06x faster                                 |
| sympy_integrate         | 24.1 ms                                            | 21.4 ms: 1.13x faster                                |
| sympy_str               | 325 ms                                             | 302 ms: 1.08x faster                                 |
| sympy_sum               | 184 ms                                             | 170 ms: 1.09x faster                                 |
| telco                   | 6.60 ms                                            | 6.69 ms: 1.01x slower                                |
| thrift                  | 1.01 ms                                            | 812 us: 1.25x faster                                 |
| tornado_http            | 127 ms                                             | 107 ms: 1.19x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 44.8 ns: 1.25x faster                                |
| unpickle_list           | 4.90 us                                            | 5.20 us: 1.06x slower                                |
| unpickle_pure_python    | 298 us                                             | 254 us: 1.17x faster                                 |
| xml_etree_generate      | 92.4 ms                                            | 80.2 ms: 1.15x faster                                |
| xml_etree_iterparse     | 110 ms                                             | 107 ms: 1.02x faster                                 |
| xml_etree_parse         | 162 ms                                             | 155 ms: 1.05x faster                                 |
| xml_etree_process       | 72.6 ms                                            | 56.9 ms: 1.28x faster                                |
| Geometric mean          | (ref)                                              | 1.21x faster                                         |

Benchmark hidden because not significant (2): regex_effbot, unpickle
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
