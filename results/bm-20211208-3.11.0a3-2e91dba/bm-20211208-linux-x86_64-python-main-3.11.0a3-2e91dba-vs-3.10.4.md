| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20211208-linux-amd64-python-main-3.11.0a3-2e91dba |
|-------------------------|:--------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 264 ms: 1.26x faster                                 |
| chameleon               | 8.76 ms                                            | 7.44 ms: 1.18x faster                                |
| chaos                   | 107 ms                                             | 73.9 ms: 1.45x faster                                |
| crypto_pyaes            | 116 ms                                             | 88.1 ms: 1.32x faster                                |
| deltablue               | 7.32 ms                                            | 4.54 ms: 1.61x faster                                |
| django_template         | 45.7 ms                                            | 36.5 ms: 1.25x faster                                |
| dulwich_log             | 75.2 ms                                            | 67.2 ms: 1.12x faster                                |
| fannkuch                | 483 ms                                             | 386 ms: 1.25x faster                                 |
| float                   | 107 ms                                             | 79.2 ms: 1.36x faster                                |
| go                      | 227 ms                                             | 158 ms: 1.44x faster                                 |
| hexiom                  | 9.29 ms                                            | 6.77 ms: 1.37x faster                                |
| html5lib                | 85.1 ms                                            | 68.5 ms: 1.24x faster                                |
| json                    | 5.55 ms                                            | 4.83 ms: 1.15x faster                                |
| json_dumps              | 13.2 ms                                            | 12.6 ms: 1.04x faster                                |
| json_loads              | 31.1 us                                            | 25.6 us: 1.21x faster                                |
| logging_format          | 8.78 us                                            | 6.49 us: 1.35x faster                                |
| logging_silent          | 168 ns                                             | 110 ns: 1.52x faster                                 |
| logging_simple          | 8.07 us                                            | 5.97 us: 1.35x faster                                |
| mako                    | 14.7 ms                                            | 11.9 ms: 1.24x faster                                |
| meteor_contest          | 114 ms                                             | 104 ms: 1.09x faster                                 |
| nbody                   | 135 ms                                             | 96.1 ms: 1.40x faster                                |
| nqueens                 | 98.4 ms                                            | 84.6 ms: 1.16x faster                                |
| pathlib                 | 20.1 ms                                            | 19.4 ms: 1.04x faster                                |
| pickle                  | 10.2 us                                            | 9.95 us: 1.03x faster                                |
| pickle_dict             | 27.2 us                                            | 27.7 us: 1.02x slower                                |
| pickle_list             | 4.40 us                                            | 4.68 us: 1.06x slower                                |
| pickle_pure_python      | 449 us                                             | 347 us: 1.29x faster                                 |
| pidigits                | 190 ms                                             | 198 ms: 1.04x slower                                 |
| pycparser               | 1.52 sec                                           | 1.24 sec: 1.23x faster                               |
| pyflate                 | 664 ms                                             | 477 ms: 1.39x faster                                 |
| python_startup          | 9.21 ms                                            | 8.00 ms: 1.15x faster                                |
| python_startup_no_site  | 5.97 ms                                            | 5.78 ms: 1.03x faster                                |
| raytrace                | 463 ms                                             | 333 ms: 1.39x faster                                 |
| regex_compile           | 178 ms                                             | 139 ms: 1.28x faster                                 |
| regex_dna               | 214 ms                                             | 212 ms: 1.01x faster                                 |
| regex_effbot            | 3.24 ms                                            | 3.21 ms: 1.01x faster                                |
| regex_v8                | 25.7 ms                                            | 24.5 ms: 1.05x faster                                |
| richards                | 68.9 ms                                            | 54.5 ms: 1.26x faster                                |
| scimark_fft             | 419 ms                                             | 332 ms: 1.26x faster                                 |
| scimark_lu              | 160 ms                                             | 112 ms: 1.43x faster                                 |
| scimark_monte_carlo     | 107 ms                                             | 74.0 ms: 1.45x faster                                |
| scimark_sor             | 196 ms                                             | 130 ms: 1.50x faster                                 |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.77 ms: 1.14x faster                                |
| spectral_norm           | 144 ms                                             | 104 ms: 1.39x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.74 us: 1.07x faster                                |
| sympy_expand            | 538 ms                                             | 509 ms: 1.06x faster                                 |
| sympy_integrate         | 24.1 ms                                            | 21.7 ms: 1.11x faster                                |
| sympy_str               | 325 ms                                             | 308 ms: 1.06x faster                                 |
| sympy_sum               | 184 ms                                             | 172 ms: 1.07x faster                                 |
| thrift                  | 1.01 ms                                            | 814 us: 1.25x faster                                 |
| tornado_http            | 127 ms                                             | 108 ms: 1.18x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 49.2 ns: 1.14x faster                                |
| unpickle_list           | 4.90 us                                            | 5.21 us: 1.06x slower                                |
| unpickle_pure_python    | 298 us                                             | 251 us: 1.19x faster                                 |
| xml_etree_generate      | 92.4 ms                                            | 80.8 ms: 1.14x faster                                |
| xml_etree_iterparse     | 110 ms                                             | 105 ms: 1.04x faster                                 |
| xml_etree_parse         | 162 ms                                             | 156 ms: 1.04x faster                                 |
| xml_etree_process       | 72.6 ms                                            | 57.8 ms: 1.26x faster                                |
| Geometric mean          | (ref)                                              | 1.19x faster                                         |

Benchmark hidden because not significant (2): telco, unpickle
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
