| Benchmark               | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 | bm-20220702-linux-amd64-python-main-3.12.0a1+-7db1d2e |
|-------------------------|:--------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                             | 248 ms: 1.34x faster                                  |
| chameleon               | 8.76 ms                                            | 6.39 ms: 1.37x faster                                 |
| chaos                   | 107 ms                                             | 65.2 ms: 1.64x faster                                 |
| crypto_pyaes            | 116 ms                                             | 73.3 ms: 1.59x faster                                 |
| deltablue               | 7.32 ms                                            | 3.20 ms: 2.29x faster                                 |
| django_template         | 45.7 ms                                            | 32.0 ms: 1.43x faster                                 |
| dulwich_log             | 75.2 ms                                            | 61.2 ms: 1.23x faster                                 |
| fannkuch                | 483 ms                                             | 373 ms: 1.29x faster                                  |
| float                   | 107 ms                                             | 69.9 ms: 1.54x faster                                 |
| go                      | 227 ms                                             | 130 ms: 1.74x faster                                  |
| hexiom                  | 9.29 ms                                            | 5.88 ms: 1.58x faster                                 |
| html5lib                | 85.1 ms                                            | 62.0 ms: 1.37x faster                                 |
| json                    | 5.55 ms                                            | 4.70 ms: 1.18x faster                                 |
| json_dumps              | 13.2 ms                                            | 11.9 ms: 1.10x faster                                 |
| json_loads              | 31.1 us                                            | 24.3 us: 1.28x faster                                 |
| logging_format          | 8.78 us                                            | 6.26 us: 1.40x faster                                 |
| logging_silent          | 168 ns                                             | 91.7 ns: 1.83x faster                                 |
| logging_simple          | 8.07 us                                            | 5.74 us: 1.41x faster                                 |
| mako                    | 14.7 ms                                            | 9.55 ms: 1.54x faster                                 |
| meteor_contest          | 114 ms                                             | 101 ms: 1.13x faster                                  |
| nbody                   | 135 ms                                             | 89.9 ms: 1.50x faster                                 |
| nqueens                 | 98.4 ms                                            | 81.0 ms: 1.22x faster                                 |
| pathlib                 | 20.1 ms                                            | 17.8 ms: 1.13x faster                                 |
| pickle                  | 10.2 us                                            | 10.5 us: 1.02x slower                                 |
| pickle_dict             | 27.2 us                                            | 30.7 us: 1.13x slower                                 |
| pickle_list             | 4.40 us                                            | 4.28 us: 1.03x faster                                 |
| pickle_pure_python      | 449 us                                             | 282 us: 1.59x faster                                  |
| pidigits                | 190 ms                                             | 189 ms: 1.00x faster                                  |
| pycparser               | 1.52 sec                                           | 1.08 sec: 1.41x faster                                |
| pyflate                 | 664 ms                                             | 389 ms: 1.71x faster                                  |
| python_startup          | 9.21 ms                                            | 8.22 ms: 1.12x faster                                 |
| python_startup_no_site  | 5.97 ms                                            | 6.07 ms: 1.02x slower                                 |
| raytrace                | 463 ms                                             | 282 ms: 1.64x faster                                  |
| regex_compile           | 178 ms                                             | 125 ms: 1.43x faster                                  |
| regex_dna               | 214 ms                                             | 197 ms: 1.09x faster                                  |
| regex_effbot            | 3.24 ms                                            | 3.49 ms: 1.08x slower                                 |
| regex_v8                | 25.7 ms                                            | 22.0 ms: 1.17x faster                                 |
| richards                | 68.9 ms                                            | 44.6 ms: 1.54x faster                                 |
| scimark_fft             | 419 ms                                             | 309 ms: 1.35x faster                                  |
| scimark_lu              | 160 ms                                             | 105 ms: 1.53x faster                                  |
| scimark_monte_carlo     | 107 ms                                             | 62.8 ms: 1.71x faster                                 |
| scimark_sor             | 196 ms                                             | 111 ms: 1.76x faster                                  |
| scimark_sparse_mat_mult | 5.45 ms                                            | 4.21 ms: 1.29x faster                                 |
| spectral_norm           | 144 ms                                             | 94.3 ms: 1.52x faster                                 |
| sqlite_synth            | 2.92 us                                            | 2.59 us: 1.13x faster                                 |
| sympy_expand            | 538 ms                                             | 450 ms: 1.20x faster                                  |
| sympy_integrate         | 24.1 ms                                            | 20.1 ms: 1.20x faster                                 |
| sympy_str               | 325 ms                                             | 276 ms: 1.18x faster                                  |
| sympy_sum               | 184 ms                                             | 158 ms: 1.16x faster                                  |
| thrift                  | 1.01 ms                                            | 744 us: 1.36x faster                                  |
| tornado_http            | 127 ms                                             | 91.4 ms: 1.39x faster                                 |
| unpack_sequence         | 56.1 ns                                            | 45.5 ns: 1.23x faster                                 |
| unpickle                | 14.4 us                                            | 13.4 us: 1.07x faster                                 |
| unpickle_list           | 4.90 us                                            | 4.93 us: 1.01x slower                                 |
| unpickle_pure_python    | 298 us                                             | 198 us: 1.50x faster                                  |
| xml_etree_generate      | 92.4 ms                                            | 75.0 ms: 1.23x faster                                 |
| xml_etree_iterparse     | 110 ms                                             | 102 ms: 1.07x faster                                  |
| xml_etree_parse         | 162 ms                                             | 156 ms: 1.04x faster                                  |
| xml_etree_process       | 72.6 ms                                            | 52.0 ms: 1.40x faster                                 |
| Geometric mean          | (ref)                                              | 1.31x faster                                          |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
