| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220405-linux-amd64-python-main-3.11.0a7-2e49bd0 |
|-------------------------|:--------------------------------------------------:|:----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 264 ms: 1.26x faster                                 |
| chameleon               | 8.76 ms                                            | 6.87 ms: 1.27x faster                                |
| chaos                   | 107 ms                                             | 70.2 ms: 1.52x faster                                |
| crypto_pyaes            | 116 ms                                             | 82.7 ms: 1.41x faster                                |
| deltablue               | 7.32 ms                                            | 3.70 ms: 1.98x faster                                |
| django_template         | 45.7 ms                                            | 34.3 ms: 1.33x faster                                |
| dulwich_log             | 75.2 ms                                            | 63.8 ms: 1.18x faster                                |
| fannkuch                | 483 ms                                             | 401 ms: 1.20x faster                                 |
| float                   | 107 ms                                             | 74.4 ms: 1.44x faster                                |
| go                      | 227 ms                                             | 143 ms: 1.59x faster                                 |
| hexiom                  | 9.29 ms                                            | 6.84 ms: 1.36x faster                                |
| html5lib                | 85.1 ms                                            | 65.3 ms: 1.30x faster                                |
| json                    | 5.55 ms                                            | 5.07 ms: 1.10x faster                                |
| json_dumps              | 13.2 ms                                            | 12.5 ms: 1.05x faster                                |
| json_loads              | 31.1 us                                            | 28.1 us: 1.11x faster                                |
| logging_format          | 8.78 us                                            | 6.35 us: 1.38x faster                                |
| logging_silent          | 168 ns                                             | 104 ns: 1.62x faster                                 |
| logging_simple          | 8.07 us                                            | 5.80 us: 1.39x faster                                |
| mako                    | 14.7 ms                                            | 10.2 ms: 1.45x faster                                |
| meteor_contest          | 114 ms                                             | 107 ms: 1.07x faster                                 |
| nbody                   | 135 ms                                             | 95.2 ms: 1.42x faster                                |
| nqueens                 | 98.4 ms                                            | 85.2 ms: 1.15x faster                                |
| pathlib                 | 20.1 ms                                            | 18.5 ms: 1.09x faster                                |
| pickle                  | 10.2 us                                            | 9.55 us: 1.07x faster                                |
| pickle_dict             | 27.2 us                                            | 27.6 us: 1.02x slower                                |
| pickle_list             | 4.40 us                                            | 4.57 us: 1.04x slower                                |
| pickle_pure_python      | 449 us                                             | 311 us: 1.44x faster                                 |
| pidigits                | 190 ms                                             | 197 ms: 1.04x slower                                 |
| pycparser               | 1.52 sec                                           | 1.24 sec: 1.23x faster                               |
| pyflate                 | 664 ms                                             | 438 ms: 1.51x faster                                 |
| python_startup          | 9.21 ms                                            | 8.07 ms: 1.14x faster                                |
| python_startup_no_site  | 5.97 ms                                            | 5.98 ms: 1.00x slower                                |
| raytrace                | 463 ms                                             | 306 ms: 1.51x faster                                 |
| regex_compile           | 178 ms                                             | 137 ms: 1.30x faster                                 |
| regex_dna               | 214 ms                                             | 231 ms: 1.08x slower                                 |
| regex_effbot            | 3.24 ms                                            | 3.34 ms: 1.03x slower                                |
| regex_v8                | 25.7 ms                                            | 25.9 ms: 1.01x slower                                |
| richards                | 68.9 ms                                            | 47.5 ms: 1.45x faster                                |
| scimark_fft             | 419 ms                                             | 335 ms: 1.25x faster                                 |
| scimark_lu              | 160 ms                                             | 108 ms: 1.48x faster                                 |
| scimark_monte_carlo     | 107 ms                                             | 70.8 ms: 1.51x faster                                |
| scimark_sor             | 196 ms                                             | 123 ms: 1.59x faster                                 |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.85 ms: 1.12x faster                                |
| spectral_norm           | 144 ms                                             | 105 ms: 1.37x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.51 us: 1.16x faster                                |
| sympy_expand            | 538 ms                                             | 476 ms: 1.13x faster                                 |
| sympy_integrate         | 24.1 ms                                            | 20.5 ms: 1.18x faster                                |
| sympy_str               | 325 ms                                             | 287 ms: 1.13x faster                                 |
| sympy_sum               | 184 ms                                             | 160 ms: 1.15x faster                                 |
| thrift                  | 1.01 ms                                            | 762 us: 1.33x faster                                 |
| tornado_http            | 127 ms                                             | 95.4 ms: 1.34x faster                                |
| unpack_sequence         | 56.1 ns                                            | 44.9 ns: 1.25x faster                                |
| unpickle_list           | 4.90 us                                            | 4.97 us: 1.01x slower                                |
| unpickle_pure_python    | 298 us                                             | 231 us: 1.29x faster                                 |
| xml_etree_generate      | 92.4 ms                                            | 78.5 ms: 1.18x faster                                |
| xml_etree_iterparse     | 110 ms                                             | 104 ms: 1.06x faster                                 |
| xml_etree_parse         | 162 ms                                             | 157 ms: 1.03x faster                                 |
| xml_etree_process       | 72.6 ms                                            | 55.2 ms: 1.31x faster                                |
| Geometric mean          | (ref)                                              | 1.23x faster                                         |

Benchmark hidden because not significant (2): telco, unpickle
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
