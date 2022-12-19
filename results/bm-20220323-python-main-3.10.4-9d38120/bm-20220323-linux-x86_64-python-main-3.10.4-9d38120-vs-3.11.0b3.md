| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220323-linux-amd64-python-main-3.10.4-9d38120 |
|-------------------------|:----------------------------------------------------:|:--------------------------------------------------:|
| 2to3                    | 256 ms                                               | 332 ms: 1.30x slower                               |
| chameleon               | 6.67 ms                                              | 8.76 ms: 1.31x slower                              |
| chaos                   | 66.9 ms                                              | 107 ms: 1.60x slower                               |
| crypto_pyaes            | 73.1 ms                                              | 116 ms: 1.59x slower                               |
| deltablue               | 3.62 ms                                              | 7.32 ms: 2.02x slower                              |
| django_template         | 32.9 ms                                              | 45.7 ms: 1.39x slower                              |
| dulwich_log             | 63.1 ms                                              | 75.2 ms: 1.19x slower                              |
| fannkuch                | 372 ms                                               | 483 ms: 1.30x slower                               |
| float                   | 72.9 ms                                              | 107 ms: 1.47x slower                               |
| go                      | 137 ms                                               | 227 ms: 1.66x slower                               |
| hexiom                  | 6.32 ms                                              | 9.29 ms: 1.47x slower                              |
| html5lib                | 62.6 ms                                              | 85.1 ms: 1.36x slower                              |
| json                    | 4.75 ms                                              | 5.55 ms: 1.17x slower                              |
| json_dumps              | 12.5 ms                                              | 13.2 ms: 1.05x slower                              |
| json_loads              | 24.4 us                                              | 31.1 us: 1.28x slower                              |
| logging_format          | 6.44 us                                              | 8.78 us: 1.36x slower                              |
| logging_silent          | 101 ns                                               | 168 ns: 1.65x slower                               |
| logging_simple          | 5.95 us                                              | 8.07 us: 1.36x slower                              |
| mako                    | 9.82 ms                                              | 14.7 ms: 1.50x slower                              |
| meteor_contest          | 104 ms                                               | 114 ms: 1.10x slower                               |
| nbody                   | 90.6 ms                                              | 135 ms: 1.49x slower                               |
| nqueens                 | 80.7 ms                                              | 98.4 ms: 1.22x slower                              |
| pathlib                 | 17.9 ms                                              | 20.1 ms: 1.13x slower                              |
| pickle                  | 9.55 us                                              | 10.2 us: 1.07x slower                              |
| pickle_dict             | 25.6 us                                              | 27.2 us: 1.06x slower                              |
| pickle_list             | 4.33 us                                              | 4.40 us: 1.02x slower                              |
| pickle_pure_python      | 302 us                                               | 449 us: 1.49x slower                               |
| pidigits                | 194 ms                                               | 190 ms: 1.02x faster                               |
| pycparser               | 1.10 sec                                             | 1.52 sec: 1.38x slower                             |
| pyflate                 | 411 ms                                               | 664 ms: 1.61x slower                               |
| python_startup          | 8.33 ms                                              | 9.21 ms: 1.11x slower                              |
| python_startup_no_site  | 6.17 ms                                              | 5.97 ms: 1.03x faster                              |
| raytrace                | 292 ms                                               | 463 ms: 1.58x slower                               |
| regex_compile           | 135 ms                                               | 178 ms: 1.32x slower                               |
| regex_dna               | 192 ms                                               | 214 ms: 1.12x slower                               |
| regex_effbot            | 2.92 ms                                              | 3.24 ms: 1.11x slower                              |
| regex_v8                | 21.2 ms                                              | 25.7 ms: 1.21x slower                              |
| richards                | 46.5 ms                                              | 68.9 ms: 1.48x slower                              |
| scimark_fft             | 317 ms                                               | 419 ms: 1.32x slower                               |
| scimark_lu              | 107 ms                                               | 160 ms: 1.50x slower                               |
| scimark_monte_carlo     | 66.0 ms                                              | 107 ms: 1.63x slower                               |
| scimark_sor             | 115 ms                                               | 196 ms: 1.70x slower                               |
| scimark_sparse_mat_mult | 4.54 ms                                              | 5.45 ms: 1.20x slower                              |
| spectral_norm           | 97.6 ms                                              | 144 ms: 1.47x slower                               |
| sqlite_synth            | 2.49 us                                              | 2.92 us: 1.17x slower                              |
| sympy_expand            | 467 ms                                               | 538 ms: 1.15x slower                               |
| sympy_integrate         | 20.5 ms                                              | 24.1 ms: 1.18x slower                              |
| sympy_str               | 284 ms                                               | 325 ms: 1.14x slower                               |
| sympy_sum               | 159 ms                                               | 184 ms: 1.16x slower                               |
| telco                   | 6.49 ms                                              | 6.60 ms: 1.02x slower                              |
| thrift                  | 759 us                                               | 1.01 ms: 1.34x slower                              |
| tornado_http            | 93.8 ms                                              | 127 ms: 1.36x slower                               |
| unpack_sequence         | 43.4 ns                                              | 56.1 ns: 1.29x slower                              |
| unpickle                | 13.3 us                                              | 14.4 us: 1.08x slower                              |
| unpickle_pure_python    | 228 us                                               | 298 us: 1.31x slower                               |
| xml_etree_generate      | 76.3 ms                                              | 92.4 ms: 1.21x slower                              |
| xml_etree_iterparse     | 105 ms                                               | 110 ms: 1.05x slower                               |
| xml_etree_parse         | 156 ms                                               | 162 ms: 1.04x slower                               |
| xml_etree_process       | 53.8 ms                                              | 72.6 ms: 1.35x slower                              |
| Geometric mean          | (ref)                                                | 1.29x slower                                       |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (3) of public/results/bm-20220323-python-main-3.10.4-9d38120/bm-20220323-linux-amd64-python-main-3.10.4-9d38120.json: genshi_text, genshi_xml, pylint
