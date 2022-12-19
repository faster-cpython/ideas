| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220806-linux-amd64-python-main-3.12.0a1+-330f1d5 |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 248 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.50 ms: 1.35x faster                                 |
| chaos                   | 107 ms                                             | 66.8 ms: 1.60x faster                                 |
| crypto_pyaes            | 116 ms                                             | 72.6 ms: 1.60x faster                                 |
| deltablue               | 7.32 ms                                            | 3.21 ms: 2.28x faster                                 |
| django_template         | 45.7 ms                                            | 32.5 ms: 1.41x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.2 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 374 ms: 1.29x faster                                  |
| float                   | 107 ms                                             | 74.1 ms: 1.45x faster                                 |
| go                      | 227 ms                                             | 131 ms: 1.73x faster                                  |
| hexiom                  | 9.29 ms                                            | 5.98 ms: 1.55x faster                                 |
| html5lib                | 85.1 ms                                            | 62.6 ms: 1.36x faster                                 |
| json                    | 5.55 ms                                            | 4.70 ms: 1.18x faster                                 |
| json_dumps              | 13.2 ms                                            | 9.51 ms: 1.38x faster                                 |
| json_loads              | 31.1 us                                            | 24.6 us: 1.26x faster                                 |
| logging_format          | 8.78 us                                            | 6.34 us: 1.38x faster                                 |
| logging_silent          | 168 ns                                             | 89.9 ns: 1.87x faster                                 |
| logging_simple          | 8.07 us                                            | 5.72 us: 1.41x faster                                 |
| mako                    | 14.7 ms                                            | 9.50 ms: 1.55x faster                                 |
| meteor_contest          | 114 ms                                             | 101 ms: 1.12x faster                                  |
| nbody                   | 135 ms                                             | 91.3 ms: 1.48x faster                                 |
| nqueens                 | 98.4 ms                                            | 79.2 ms: 1.24x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.6 ms: 1.15x faster                                 |
| pickle_dict             | 27.2 us                                            | 31.9 us: 1.17x slower                                 |
| pickle_list             | 4.40 us                                            | 4.26 us: 1.03x faster                                 |
| pickle_pure_python      | 449 us                                             | 288 us: 1.56x faster                                  |
| pidigits                | 190 ms                                             | 194 ms: 1.02x slower                                  |
| pycparser               | 1.52 sec                                           | 1.04 sec: 1.46x faster                                |
| pyflate                 | 664 ms                                             | 393 ms: 1.69x faster                                  |
| python_startup          | 9.21 ms                                            | 8.15 ms: 1.13x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.01 ms: 1.01x slower                                 |
| raytrace                | 463 ms                                             | 278 ms: 1.67x faster                                  |
| regex_compile           | 178 ms                                             | 127 ms: 1.40x faster                                  |
| regex_dna               | 214 ms                                             | 203 ms: 1.05x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.50 ms: 1.08x slower                                 |
| regex_v8                | 25.7 ms                                            | 20.8 ms: 1.24x faster                                 |
| richards                | 68.9 ms                                            | 44.5 ms: 1.55x faster                                 |
| scimark_fft             | 419 ms                                             | 311 ms: 1.35x faster                                  |
| scimark_lu              | 160 ms                                             | 106 ms: 1.51x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 64.2 ms: 1.67x faster                                 |
| scimark_sor             | 196 ms                                             | 110 ms: 1.78x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 3.91 ms: 1.39x faster                                 |
| spectral_norm           | 144 ms                                             | 93.8 ms: 1.53x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.59 us: 1.13x faster                                 |
| sympy_expand            | 538 ms                                             | 461 ms: 1.17x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.3 ms: 1.19x faster                                 |
| sympy_str               | 325 ms                                             | 282 ms: 1.15x faster                                  |
| sympy_sum               | 184 ms                                             | 160 ms: 1.15x faster                                  |
| telco                   | 6.60 ms                                            | 6.41 ms: 1.03x faster                                 |
| thrift                  | 1.01 ms                                            | 748 us: 1.36x faster                                  |
| tornado_http            | 127 ms                                             | 91.7 ms: 1.39x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 45.9 ns: 1.22x faster                                 |
| unpickle                | 14.4 us                                            | 13.3 us: 1.08x faster                                 |
| unpickle_list           | 4.90 us                                            | 5.06 us: 1.03x slower                                 |
| unpickle_pure_python    | 298 us                                             | 199 us: 1.49x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.0 ms: 1.23x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 105 ms: 1.05x faster                                  |
| xml_etree_parse         | 162 ms                                             | 156 ms: 1.04x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.2 ms: 1.39x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
