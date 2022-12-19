| Benchmark               | bm-20220601-linux-amd64-python-main-3.11.0b3-eb0004c | bm-20220813-linux-amd64-python-main-3.12.0a1+-32ac98e |
|-------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 256 ms                                               | 250 ms: 1.02x faster                                  |
| chameleon               | 6.67 ms                                              | 6.30 ms: 1.06x faster                                 |
| crypto_pyaes            | 73.1 ms                                              | 74.2 ms: 1.02x slower                                 |
| deltablue               | 3.62 ms                                              | 3.20 ms: 1.13x faster                                 |
| django_template         | 32.9 ms                                              | 32.5 ms: 1.01x faster                                 |
| dulwich_log             | 63.1 ms                                              | 61.6 ms: 1.02x faster                                 |
| fannkuch                | 372 ms                                               | 375 ms: 1.01x slower                                  |
| go                      | 137 ms                                               | 134 ms: 1.02x faster                                  |
| hexiom                  | 6.32 ms                                              | 5.97 ms: 1.06x faster                                 |
| json                    | 4.75 ms                                              | 4.68 ms: 1.01x faster                                 |
| json_dumps              | 12.5 ms                                              | 9.67 ms: 1.29x faster                                 |
| json_loads              | 24.4 us                                              | 24.2 us: 1.01x faster                                 |
| logging_format          | 6.44 us                                              | 6.39 us: 1.01x faster                                 |
| logging_silent          | 101 ns                                               | 89.6 ns: 1.13x faster                                 |
| logging_simple          | 5.95 us                                              | 5.81 us: 1.03x faster                                 |
| mako                    | 9.82 ms                                              | 9.21 ms: 1.07x faster                                 |
| meteor_contest          | 104 ms                                               | 101 ms: 1.03x faster                                  |
| pickle                  | 9.55 us                                              | 10.5 us: 1.09x slower                                 |
| pickle_dict             | 25.6 us                                              | 31.4 us: 1.23x slower                                 |
| pickle_list             | 4.33 us                                              | 4.25 us: 1.02x faster                                 |
| pickle_pure_python      | 302 us                                               | 287 us: 1.05x faster                                  |
| pidigits                | 194 ms                                               | 201 ms: 1.04x slower                                  |
| pycparser               | 1.10 sec                                             | 1.05 sec: 1.05x faster                                |
| pyflate                 | 411 ms                                               | 397 ms: 1.04x faster                                  |
| python_startup          | 8.33 ms                                              | 8.17 ms: 1.02x faster                                 |
| python_startup_no_site  | 6.17 ms                                              | 6.04 ms: 1.02x faster                                 |
| regex_compile           | 135 ms                                               | 127 ms: 1.07x faster                                  |
| regex_dna               | 192 ms                                               | 205 ms: 1.07x slower                                  |
| regex_effbot            | 2.92 ms                                              | 3.42 ms: 1.17x slower                                 |
| regex_v8                | 21.2 ms                                              | 20.9 ms: 1.01x faster                                 |
| richards                | 46.5 ms                                              | 45.1 ms: 1.03x faster                                 |
| scimark_fft             | 317 ms                                               | 308 ms: 1.03x faster                                  |
| scimark_monte_carlo     | 66.0 ms                                              | 64.7 ms: 1.02x faster                                 |
| scimark_sor             | 115 ms                                               | 111 ms: 1.03x faster                                  |
| scimark_sparse_mat_mult | 4.54 ms                                              | 4.15 ms: 1.09x faster                                 |
| spectral_norm           | 97.6 ms                                              | 95.1 ms: 1.03x faster                                 |
| sqlite_synth            | 2.49 us                                              | 2.58 us: 1.04x slower                                 |
| sympy_expand            | 467 ms                                               | 457 ms: 1.02x faster                                  |
| sympy_integrate         | 20.5 ms                                              | 20.1 ms: 1.02x faster                                 |
| sympy_str               | 284 ms                                               | 278 ms: 1.02x faster                                  |
| thrift                  | 759 us                                               | 728 us: 1.04x faster                                  |
| tornado_http            | 93.8 ms                                              | 91.6 ms: 1.02x faster                                 |
| unpack_sequence         | 43.4 ns                                              | 43.0 ns: 1.01x faster                                 |
| unpickle_list           | 4.89 us                                              | 4.94 us: 1.01x slower                                 |
| unpickle_pure_python    | 228 us                                               | 201 us: 1.14x faster                                  |
| xml_etree_generate      | 76.3 ms                                              | 74.3 ms: 1.03x faster                                 |
| xml_etree_parse         | 156 ms                                               | 155 ms: 1.01x faster                                  |
| xml_etree_process       | 53.8 ms                                              | 51.3 ms: 1.05x faster                                 |
| Geometric mean          | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (12): chaos, float, html5lib, nbody, nqueens, pathlib, raytrace, scimark_lu, sympy_sum, telco, unpickle, xml_etree_iterparse
