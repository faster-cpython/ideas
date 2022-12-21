| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220307-linux-amd64-python-main-3.11.0a6-3ddfa55 |
|-------------------------|:--------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 268 ms: 1.24x faster                                 |
| chameleon               | 8.76 ms                                            | 6.93 ms: 1.26x faster                                |
| chaos                   | 107 ms                                             | 73.5 ms: 1.46x faster                                |
| crypto_pyaes            | 116 ms                                             | 84.6 ms: 1.38x faster                                |
| deltablue               | 7.32 ms                                            | 4.16 ms: 1.76x faster                                |
| django_template         | 45.7 ms                                            | 36.0 ms: 1.27x faster                                |
| dulwich_log             | 75.2 ms                                            | 66.5 ms: 1.13x faster                                |
| fannkuch                | 483 ms                                             | 398 ms: 1.21x faster                                 |
| float                   | 107 ms                                             | 78.7 ms: 1.36x faster                                |
| go                      | 227 ms                                             | 148 ms: 1.54x faster                                 |
| hexiom                  | 9.29 ms                                            | 7.04 ms: 1.32x faster                                |
| html5lib                | 85.1 ms                                            | 68.6 ms: 1.24x faster                                |
| json                    | 5.55 ms                                            | 5.00 ms: 1.11x faster                                |
| json_dumps              | 13.2 ms                                            | 12.6 ms: 1.04x faster                                |
| json_loads              | 31.1 us                                            | 28.1 us: 1.11x faster                                |
| logging_format          | 8.78 us                                            | 6.08 us: 1.44x faster                                |
| logging_silent          | 168 ns                                             | 113 ns: 1.49x faster                                 |
| logging_simple          | 8.07 us                                            | 5.52 us: 1.46x faster                                |
| mako                    | 14.7 ms                                            | 10.6 ms: 1.39x faster                                |
| meteor_contest          | 114 ms                                             | 106 ms: 1.08x faster                                 |
| nbody                   | 135 ms                                             | 97.7 ms: 1.38x faster                                |
| nqueens                 | 98.4 ms                                            | 87.0 ms: 1.13x faster                                |
| pathlib                 | 20.1 ms                                            | 18.2 ms: 1.11x faster                                |
| pickle                  | 10.2 us                                            | 9.69 us: 1.06x faster                                |
| pickle_dict             | 27.2 us                                            | 28.1 us: 1.03x slower                                |
| pickle_list             | 4.40 us                                            | 4.51 us: 1.02x slower                                |
| pickle_pure_python      | 449 us                                             | 335 us: 1.34x faster                                 |
| pidigits                | 190 ms                                             | 208 ms: 1.09x slower                                 |
| pycparser               | 1.52 sec                                           | 1.21 sec: 1.26x faster                               |
| pyflate                 | 664 ms                                             | 453 ms: 1.46x faster                                 |
| python_startup          | 9.21 ms                                            | 8.20 ms: 1.12x faster                                |
| python_startup_no_site  | 5.97 ms                                            | 6.07 ms: 1.02x slower                                |
| raytrace                | 463 ms                                             | 318 ms: 1.45x faster                                 |
| regex_compile           | 178 ms                                             | 140 ms: 1.27x faster                                 |
| regex_dna               | 214 ms                                             | 221 ms: 1.03x slower                                 |
| regex_effbot            | 3.24 ms                                            | 3.49 ms: 1.08x slower                                |
| regex_v8                | 25.7 ms                                            | 23.0 ms: 1.12x faster                                |
| richards                | 68.9 ms                                            | 48.5 ms: 1.42x faster                                |
| scimark_fft             | 419 ms                                             | 336 ms: 1.24x faster                                 |
| scimark_lu              | 160 ms                                             | 115 ms: 1.39x faster                                 |
| scimark_monte_carlo     | 107 ms                                             | 72.9 ms: 1.47x faster                                |
| scimark_sor             | 196 ms                                             | 123 ms: 1.59x faster                                 |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.82 ms: 1.13x faster                                |
| spectral_norm           | 144 ms                                             | 107 ms: 1.34x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.51 us: 1.16x faster                                |
| sympy_expand            | 538 ms                                             | 481 ms: 1.12x faster                                 |
| sympy_integrate         | 24.1 ms                                            | 20.9 ms: 1.15x faster                                |
| sympy_str               | 325 ms                                             | 289 ms: 1.12x faster                                 |
| sympy_sum               | 184 ms                                             | 163 ms: 1.13x faster                                 |
| telco                   | 6.60 ms                                            | 6.92 ms: 1.05x slower                                |
| thrift                  | 1.01 ms                                            | 789 us: 1.29x faster                                 |
| tornado_http            | 127 ms                                             | 99.2 ms: 1.28x faster                                |
| unpack_sequence         | 56.1 ns                                            | 131 ns: 2.34x slower                                 |
| unpickle_list           | 4.90 us                                            | 4.92 us: 1.00x slower                                |
| unpickle_pure_python    | 298 us                                             | 246 us: 1.21x faster                                 |
| xml_etree_generate      | 92.4 ms                                            | 79.6 ms: 1.16x faster                                |
| xml_etree_iterparse     | 110 ms                                             | 105 ms: 1.05x faster                                 |
| xml_etree_parse         | 162 ms                                             | 156 ms: 1.04x faster                                 |
| xml_etree_process       | 72.6 ms                                            | 56.0 ms: 1.30x faster                                |
| Geometric mean          | (ref)                                              | 1.19x faster                                         |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
