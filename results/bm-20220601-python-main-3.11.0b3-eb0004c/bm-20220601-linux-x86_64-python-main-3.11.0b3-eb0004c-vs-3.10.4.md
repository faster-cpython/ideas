| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c |
|-------------------------|:--------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 256 ms: 1.30x faster                                 |
| chameleon               | 8.76 ms                                            | 6.67 ms: 1.31x faster                                |
| chaos                   | 107 ms                                             | 66.9 ms: 1.60x faster                                |
| crypto_pyaes            | 116 ms                                             | 73.1 ms: 1.59x faster                                |
| deltablue               | 7.32 ms                                            | 3.62 ms: 2.02x faster                                |
| django_template         | 45.7 ms                                            | 32.9 ms: 1.39x faster                                |
| dulwich_log             | 75.2 ms                                            | 63.1 ms: 1.19x faster                                |
| fannkuch                | 483 ms                                             | 372 ms: 1.30x faster                                 |
| float                   | 107 ms                                             | 72.9 ms: 1.47x faster                                |
| go                      | 227 ms                                             | 137 ms: 1.66x faster                                 |
| hexiom                  | 9.29 ms                                            | 6.32 ms: 1.47x faster                                |
| html5lib                | 85.1 ms                                            | 62.6 ms: 1.36x faster                                |
| json                    | 5.55 ms                                            | 4.75 ms: 1.17x faster                                |
| json_dumps              | 13.2 ms                                            | 12.5 ms: 1.05x faster                                |
| json_loads              | 31.1 us                                            | 24.4 us: 1.28x faster                                |
| logging_format          | 8.78 us                                            | 6.44 us: 1.36x faster                                |
| logging_silent          | 168 ns                                             | 101 ns: 1.65x faster                                 |
| logging_simple          | 8.07 us                                            | 5.95 us: 1.36x faster                                |
| mako                    | 14.7 ms                                            | 9.82 ms: 1.50x faster                                |
| meteor_contest          | 114 ms                                             | 104 ms: 1.10x faster                                 |
| nbody                   | 135 ms                                             | 90.6 ms: 1.49x faster                                |
| nqueens                 | 98.4 ms                                            | 80.7 ms: 1.22x faster                                |
| pathlib                 | 20.1 ms                                            | 17.9 ms: 1.13x faster                                |
| pickle                  | 10.2 us                                            | 9.55 us: 1.07x faster                                |
| pickle_dict             | 27.2 us                                            | 25.6 us: 1.06x faster                                |
| pickle_list             | 4.40 us                                            | 4.33 us: 1.02x faster                                |
| pickle_pure_python      | 449 us                                             | 302 us: 1.49x faster                                 |
| pidigits                | 190 ms                                             | 194 ms: 1.02x slower                                 |
| pycparser               | 1.52 sec                                           | 1.10 sec: 1.38x faster                               |
| pyflate                 | 664 ms                                             | 411 ms: 1.61x faster                                 |
| python_startup          | 9.21 ms                                            | 8.33 ms: 1.11x faster                                |
| python_startup_no_site  | 5.97 ms                                            | 6.17 ms: 1.03x slower                                |
| raytrace                | 463 ms                                             | 292 ms: 1.58x faster                                 |
| regex_compile           | 178 ms                                             | 135 ms: 1.32x faster                                 |
| regex_dna               | 214 ms                                             | 192 ms: 1.12x faster                                 |
| regex_effbot            | 3.24 ms                                            | 2.92 ms: 1.11x faster                                |
| regex_v8                | 25.7 ms                                            | 21.2 ms: 1.21x faster                                |
| richards                | 68.9 ms                                            | 46.5 ms: 1.48x faster                                |
| scimark_fft             | 419 ms                                             | 317 ms: 1.32x faster                                 |
| scimark_lu              | 160 ms                                             | 107 ms: 1.50x faster                                 |
| scimark_monte_carlo     | 107 ms                                             | 66.0 ms: 1.63x faster                                |
| scimark_sor             | 196 ms                                             | 115 ms: 1.70x faster                                 |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.54 ms: 1.20x faster                                |
| spectral_norm           | 144 ms                                             | 97.6 ms: 1.47x faster                                |
| sqlite_synth            | 2.92 us                                            | 2.49 us: 1.17x faster                                |
| sympy_expand            | 538 ms                                             | 467 ms: 1.15x faster                                 |
| sympy_integrate         | 24.1 ms                                            | 20.5 ms: 1.18x faster                                |
| sympy_str               | 325 ms                                             | 284 ms: 1.14x faster                                 |
| sympy_sum               | 184 ms                                             | 159 ms: 1.16x faster                                 |
| telco                   | 6.60 ms                                            | 6.49 ms: 1.02x faster                                |
| thrift                  | 1.01 ms                                            | 759 us: 1.34x faster                                 |
| tornado_http            | 127 ms                                             | 93.8 ms: 1.36x faster                                |
| unpack_sequence         | 56.1 ns                                            | 43.4 ns: 1.29x faster                                |
| unpickle                | 14.4 us                                            | 13.3 us: 1.08x faster                                |
| unpickle_pure_python    | 298 us                                             | 228 us: 1.31x faster                                 |
| xml_etree_generate      | 92.4 ms                                            | 76.3 ms: 1.21x faster                                |
| xml_etree_iterparse     | 110 ms                                             | 105 ms: 1.05x faster                                 |
| xml_etree_parse         | 162 ms                                             | 156 ms: 1.04x faster                                 |
| xml_etree_process       | 72.6 ms                                            | 53.8 ms: 1.35x faster                                |
| Geometric mean          | (ref)                                              | 1.29x faster                                         |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
