| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220710-linux-amd64-python-main-3.12.0a1+-264b3dd |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 249 ms: 1.03x faster                                  |
| chameleon               | 6.67 ms                                              | 6.30 ms: 1.06x faster                                 |
| chaos                   | 66.9 ms                                              | 65.0 ms: 1.03x faster                                 |
| crypto_pyaes            | 73.1 ms                                              | 74.3 ms: 1.02x slower                                 |
| deltablue               | 3.62 ms                                              | 3.24 ms: 1.12x faster                                 |
| django_template         | 32.9 ms                                              | 31.5 ms: 1.04x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.2 ms: 1.03x faster                                 |
| fannkuch                | 372 ms                                               | 378 ms: 1.02x slower                                  |
| float                   | 72.9 ms                                              | 72.4 ms: 1.01x faster                                 |
| go                      | 137 ms                                               | 130 ms: 1.05x faster                                  |
| hexiom                  | 6.32 ms                                              | 5.92 ms: 1.07x faster                                 |
| json                    | 4.75 ms                                              | 4.69 ms: 1.01x faster                                 |
| json_dumps              | 12.5 ms                                              | 11.8 ms: 1.06x faster                                 |
| json_loads              | 24.4 us                                              | 24.2 us: 1.01x faster                                 |
| logging_format          | 6.44 us                                              | 6.35 us: 1.01x faster                                 |
| logging_silent          | 101 ns                                               | 92.5 ns: 1.10x faster                                 |
| logging_simple          | 5.95 us                                              | 5.67 us: 1.05x faster                                 |
| mako                    | 9.82 ms                                              | 9.45 ms: 1.04x faster                                 |
| meteor_contest          | 104 ms                                               | 101 ms: 1.03x faster                                  |
| pickle                  | 9.55 us                                              | 10.5 us: 1.09x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.6 us: 1.23x slower                                 |
| pickle_list             | 4.33 us                                              | 4.12 us: 1.05x faster                                 |
| pickle_pure_python      | 302 us                                               | 286 us: 1.06x faster                                  |
| pidigits                | 194 ms                                               | 193 ms: 1.00x faster                                  |
| pycparser               | 1.10 sec                                             | 1.06 sec: 1.04x faster                                |
| pyflate                 | 411 ms                                               | 398 ms: 1.03x faster                                  |
| python_startup          | 8.33 ms                                              | 8.16 ms: 1.02x faster                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.01 ms: 1.03x faster                                 |
| raytrace                | 292 ms                                               | 286 ms: 1.02x faster                                  |
| regex_compile           | 135 ms                                               | 126 ms: 1.08x faster                                  |
| regex_dna               | 192 ms                                               | 207 ms: 1.08x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.54 ms: 1.21x slower                                 |
| regex_v8                | 21.2 ms                                              | 22.1 ms: 1.04x slower                                 |
| richards                | 46.5 ms                                              | 45.0 ms: 1.03x faster                                 |
| scimark_fft             | 317 ms                                               | 313 ms: 1.01x faster                                  |
| scimark_lu              | 107 ms                                               | 104 ms: 1.02x faster                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 64.6 ms: 1.02x faster                                 |
| scimark_sor             | 115 ms                                               | 111 ms: 1.04x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.18 ms: 1.09x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.62 us: 1.05x slower                                 |
| sympy_expand            | 467 ms                                               | 450 ms: 1.04x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.1 ms: 1.02x faster                                 |
| sympy_str               | 284 ms                                               | 279 ms: 1.02x faster                                  |
| thrift                  | 759 us                                               | 720 us: 1.05x faster                                  |
| tornado_http            | 93.8 ms                                              | 91.3 ms: 1.03x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 46.4 ns: 1.07x slower                                 |
| unpickle                | 13.3 us                                              | 13.1 us: 1.01x faster                                 |
| unpickle_list           | 4.89 us                                              | 5.04 us: 1.03x slower                                 |
| unpickle_pure_python    | 228 us                                               | 201 us: 1.13x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 75.9 ms: 1.00x faster                                 |
| xml_etree_iterparse     | 105 ms                                               | 104 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                              | 53.3 ms: 1.01x faster                                 |
| Geometric mean          | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (8): html5lib, nbody, nqueens, pathlib, spectral_norm, sympy_sum, telco, xml_etree_parse
