| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220530-linux-amd64-python-main-3.11.0b2-72f00f4 |
|-------------------------|:--------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 256 ms: 1.30x faster                                 |
| chameleon               | 8.76 ms                                            | 6.59 ms: 1.33x faster                                |
| chaos                   | 107 ms                                             | 67.8 ms: 1.58x faster                                |
| crypto_pyaes            | 116 ms                                             | 73.8 ms: 1.58x faster                                |
| deltablue               | 7.32 ms                                            | 3.60 ms: 2.03x faster                                |
| django_template         | 45.7 ms                                            | 32.4 ms: 1.41x faster                                |
| dulwich_log             | 75.2 ms                                            | 62.6 ms: 1.20x faster                                |
| fannkuch                | 483 ms                                             | 394 ms: 1.22x faster                                 |
| float                   | 107 ms                                             | 72.8 ms: 1.47x faster                                |
| go                      | 227 ms                                             | 136 ms: 1.66x faster                                 |
| hexiom                  | 9.29 ms                                            | 6.32 ms: 1.47x faster                                |
| html5lib                | 85.1 ms                                            | 63.8 ms: 1.33x faster                                |
| json                    | 5.55 ms                                            | 4.72 ms: 1.18x faster                                |
| json_dumps              | 13.2 ms                                            | 12.6 ms: 1.05x faster                                |
| json_loads              | 31.1 us                                            | 24.3 us: 1.28x faster                                |
| logging_format          | 8.78 us                                            | 6.42 us: 1.37x faster                                |
| logging_silent          | 168 ns                                             | 98.1 ns: 1.71x faster                                |
| logging_simple          | 8.07 us                                            | 5.82 us: 1.39x faster                                |
| mako                    | 14.7 ms                                            | 9.71 ms: 1.52x faster                                |
| meteor_contest          | 114 ms                                             | 104 ms: 1.09x faster                                 |
| nbody                   | 135 ms                                             | 90.9 ms: 1.48x faster                                |
| nqueens                 | 98.4 ms                                            | 82.4 ms: 1.19x faster                                |
| pathlib                 | 20.1 ms                                            | 18.2 ms: 1.10x faster                                |
| pickle                  | 10.2 us                                            | 9.61 us: 1.06x faster                                |
| pickle_dict             | 27.2 us                                            | 25.9 us: 1.05x faster                                |
| pickle_list             | 4.40 us                                            | 4.30 us: 1.02x faster                                |
| pickle_pure_python      | 449 us                                             | 302 us: 1.49x faster                                 |
| pidigits                | 190 ms                                             | 190 ms: 1.00x faster                                 |
| pycparser               | 1.52 sec                                           | 1.10 sec: 1.38x faster                               |
| pyflate                 | 664 ms                                             | 410 ms: 1.62x faster                                 |
| python_startup          | 9.21 ms                                            | 8.33 ms: 1.11x faster                                |
| python_startup_no_site  | 5.97 ms                                            | 6.17 ms: 1.03x slower                                |
| raytrace                | 463 ms                                             | 291 ms: 1.59x faster                                 |
| regex_compile           | 178 ms                                             | 136 ms: 1.31x faster                                 |
| regex_dna               | 214 ms                                             | 196 ms: 1.09x faster                                 |
| regex_effbot            | 3.24 ms                                            | 3.02 ms: 1.08x faster                                |
| regex_v8                | 25.7 ms                                            | 21.5 ms: 1.19x faster                                |
| richards                | 68.9 ms                                            | 45.3 ms: 1.52x faster                                |
| scimark_fft             | 419 ms                                             | 324 ms: 1.29x faster                                 |
| scimark_lu              | 160 ms                                             | 107 ms: 1.49x faster                                 |
| scimark_monte_carlo     | 107 ms                                             | 66.5 ms: 1.61x faster                                |
| scimark_sor             | 196 ms                                             | 115 ms: 1.70x faster                                 |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.79 ms: 1.14x faster                                |
| spectral_norm           | 144 ms                                             | 96.3 ms: 1.49x faster                                |
| sqlite_synth            | 2.92 us                                            | 2.50 us: 1.17x faster                                |
| sympy_expand            | 538 ms                                             | 465 ms: 1.16x faster                                 |
| sympy_integrate         | 24.1 ms                                            | 20.5 ms: 1.18x faster                                |
| sympy_str               | 325 ms                                             | 284 ms: 1.14x faster                                 |
| sympy_sum               | 184 ms                                             | 159 ms: 1.16x faster                                 |
| thrift                  | 1.01 ms                                            | 756 us: 1.34x faster                                 |
| tornado_http            | 127 ms                                             | 93.8 ms: 1.36x faster                                |
| unpack_sequence         | 56.1 ns                                            | 43.2 ns: 1.30x faster                                |
| unpickle                | 14.4 us                                            | 13.3 us: 1.08x faster                                |
| unpickle_list           | 4.90 us                                            | 4.98 us: 1.02x slower                                |
| unpickle_pure_python    | 298 us                                             | 227 us: 1.31x faster                                 |
| xml_etree_generate      | 92.4 ms                                            | 75.8 ms: 1.22x faster                                |
| xml_etree_iterparse     | 110 ms                                             | 104 ms: 1.06x faster                                 |
| xml_etree_parse         | 162 ms                                             | 157 ms: 1.03x faster                                 |
| xml_etree_process       | 72.6 ms                                            | 53.3 ms: 1.36x faster                                |
| Geometric mean          | (ref)                                              | 1.28x faster                                         |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
