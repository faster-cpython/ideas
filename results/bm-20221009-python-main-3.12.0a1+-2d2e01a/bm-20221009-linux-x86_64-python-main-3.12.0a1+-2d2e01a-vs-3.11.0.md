Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| chameleon      | 6.41 ms                                                | 6.61 ms: 1.03x slower                                  |
| html5lib       | 63.2 ms                                                | 59.7 ms: 1.06x faster                                  |
| tornado_http   | 96.6 ms                                                | 93.4 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.3 ms: 1.06x faster                                  |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.60 ms: 1.07x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.1 ms: 1.01x faster                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.44 ms: 1.34x faster                                  |
| json_loads           | 26.2 us                                                | 23.8 us: 1.10x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.9 us: 1.02x slower                                  |
| pickle_list          | 4.17 us                                                | 4.06 us: 1.03x faster                                  |
| pickle_pure_python   | 304 us                                                 | 293 us: 1.04x faster                                   |
| unpickle             | 13.3 us                                                | 13.0 us: 1.02x faster                                  |
| unpickle_list        | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python | 225 us                                                 | 204 us: 1.11x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 146 ms: 1.08x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 101 ms: 1.02x faster                                   |
| xml_etree_generate   | 76.2 ms                                                | 76.6 ms: 1.00x slower                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.38 ms: 1.00x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.06 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 33.3 ms: 1.03x slower                                  |
| genshi_text     | 22.1 ms                                                | 21.8 ms: 1.01x faster                                  |
| genshi_xml      | 52.1 ms                                                | 49.1 ms: 1.06x faster                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221009-linux-x86_64-python-main-3.12.0a1+-2d2e01a |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.05x faster                                  |
| async_tree_cpu_io_mixed | 752 ms                                                 | 731 ms: 1.03x faster                                   |
| async_tree_memoization  | 625 ms                                                 | 646 ms: 1.03x slower                                   |
| chameleon               | 6.41 ms                                                | 6.61 ms: 1.03x slower                                  |
| chaos                   | 68.6 ms                                                | 65.5 ms: 1.05x faster                                  |
| coroutines              | 26.1 ms                                                | 25.0 ms: 1.04x faster                                  |
| coverage                | 101 ms                                                 | 98.9 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 75.3 ms: 1.02x slower                                  |
| deepcopy                | 344 us                                                 | 331 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.90 us: 1.02x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.3 us: 1.06x faster                                  |
| deltablue               | 3.64 ms                                                | 3.40 ms: 1.07x faster                                  |
| django_template         | 32.5 ms                                                | 33.3 ms: 1.03x slower                                  |
| dulwich_log             | 63.9 ms                                                | 61.1 ms: 1.05x faster                                  |
| fannkuch                | 388 ms                                                 | 362 ms: 1.07x faster                                   |
| float                   | 76.3 ms                                                | 72.3 ms: 1.06x faster                                  |
| generators              | 72.2 ms                                                | 73.8 ms: 1.02x slower                                  |
| genshi_text             | 22.1 ms                                                | 21.8 ms: 1.01x faster                                  |
| genshi_xml              | 52.1 ms                                                | 49.1 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 138 ms: 1.04x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.02 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 59.7 ms: 1.06x faster                                  |
| json                    | 4.95 ms                                                | 4.72 ms: 1.05x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.44 ms: 1.34x faster                                  |
| json_loads              | 26.2 us                                                | 23.8 us: 1.10x faster                                  |
| logging_format          | 6.62 us                                                | 6.43 us: 1.03x faster                                  |
| logging_silent          | 98.5 ns                                                | 92.7 ns: 1.06x faster                                  |
| logging_simple          | 6.06 us                                                | 5.74 us: 1.06x faster                                  |
| mdp                     | 2.62 sec                                               | 2.59 sec: 1.01x faster                                 |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                   |
| mypy                    | 669 ms                                                 | 799 ms: 1.20x slower                                   |
| nqueens                 | 85.0 ms                                                | 79.2 ms: 1.07x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.01x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.9 us: 1.02x slower                                  |
| pickle_list             | 4.17 us                                                | 4.06 us: 1.03x faster                                  |
| pickle_pure_python      | 304 us                                                 | 293 us: 1.04x faster                                   |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 682 ms: 1.01x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                 |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.08x faster                                 |
| pyflate                 | 417 ms                                                 | 407 ms: 1.03x faster                                   |
| python_startup          | 8.36 ms                                                | 8.38 ms: 1.00x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.06 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 284 ms: 1.02x faster                                   |
| regex_compile           | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.60 ms: 1.07x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.1 ms: 1.01x faster                                  |
| richards                | 46.2 ms                                                | 44.4 ms: 1.04x faster                                  |
| scimark_fft             | 329 ms                                                 | 316 ms: 1.04x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 66.3 ms: 1.03x faster                                  |
| scimark_sor             | 115 ms                                                 | 105 ms: 1.10x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.20 ms: 1.05x faster                                  |
| spectral_norm           | 99.9 ms                                                | 96.4 ms: 1.04x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.34 ms: 1.02x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.64 ms: 1.01x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.4 ms: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.03x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.60 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 456 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| sympy_sum               | 166 ms                                                 | 164 ms: 1.01x faster                                   |
| sympy_str               | 287 ms                                                 | 280 ms: 1.03x faster                                   |
| telco                   | 6.62 ms                                                | 6.32 ms: 1.05x faster                                  |
| thrift                  | 752 us                                                 | 737 us: 1.02x faster                                   |
| tornado_http            | 96.6 ms                                                | 93.4 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 50.2 ns: 1.16x slower                                  |
| unpickle                | 13.3 us                                                | 13.0 us: 1.02x faster                                  |
| unpickle_list           | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 204 us: 1.11x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 146 ms: 1.08x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 101 ms: 1.02x faster                                   |
| xml_etree_generate      | 76.2 ms                                                | 76.6 ms: 1.00x slower                                  |
| Geometric mean          | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (8): async_tree_none, async_tree_io, mako, nbody, pylint, regex_dna, scimark_lu, xml_etree_process
Ignored benchmarks (7) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
