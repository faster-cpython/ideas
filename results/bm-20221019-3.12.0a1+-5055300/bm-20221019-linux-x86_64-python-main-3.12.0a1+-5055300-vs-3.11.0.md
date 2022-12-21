Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 249 ms: 1.04x faster                                   |
| chameleon      | 6.41 ms                                                | 6.46 ms: 1.01x slower                                  |
| html5lib       | 63.2 ms                                                | 60.2 ms: 1.05x faster                                  |
| tornado_http   | 96.6 ms                                                | 93.0 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.1 ms: 1.07x faster                                  |
| pidigits       | 199 ms                                                 | 193 ms: 1.03x faster                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_dna      | 203 ms                                                 | 205 ms: 1.01x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.40 ms: 1.01x slower                                  |
| regex_v8       | 22.3 ms                                                | 21.4 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.42 ms: 1.34x faster                                  |
| json_loads           | 26.2 us                                                | 24.0 us: 1.09x faster                                  |
| pickle               | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.1 us: 1.01x faster                                  |
| pickle_list          | 4.17 us                                                | 3.99 us: 1.05x faster                                  |
| pickle_pure_python   | 304 us                                                 | 285 us: 1.07x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python | 225 us                                                 | 202 us: 1.12x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 144 ms: 1.10x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 106 ms: 1.03x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 76.9 ms: 1.01x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.32 ms: 1.00x faster                                  |
| python_startup_no_site | 5.96 ms                                                | 6.03 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.00x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.7 ms: 1.01x slower                                  |
| genshi_text     | 22.1 ms                                                | 20.9 ms: 1.06x faster                                  |
| genshi_xml      | 52.1 ms                                                | 49.3 ms: 1.06x faster                                  |
| mako            | 9.85 ms                                                | 9.79 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 249 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.00 ms: 1.05x faster                                  |
| async_tree_cpu_io_mixed | 752 ms                                                 | 732 ms: 1.03x faster                                   |
| async_tree_memoization  | 625 ms                                                 | 657 ms: 1.05x slower                                   |
| chameleon               | 6.41 ms                                                | 6.46 ms: 1.01x slower                                  |
| chaos                   | 68.6 ms                                                | 67.8 ms: 1.01x faster                                  |
| coroutines              | 26.1 ms                                                | 24.5 ms: 1.06x faster                                  |
| coverage                | 101 ms                                                 | 97.7 ms: 1.03x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 75.4 ms: 1.02x slower                                  |
| deepcopy                | 344 us                                                 | 333 us: 1.03x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.89 us: 1.03x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.5 us: 1.06x faster                                  |
| deltablue               | 3.64 ms                                                | 3.36 ms: 1.08x faster                                  |
| django_template         | 32.5 ms                                                | 32.7 ms: 1.01x slower                                  |
| dulwich_log             | 63.9 ms                                                | 61.2 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 363 ms: 1.07x faster                                   |
| float                   | 76.3 ms                                                | 71.1 ms: 1.07x faster                                  |
| generators              | 72.2 ms                                                | 71.4 ms: 1.01x faster                                  |
| genshi_text             | 22.1 ms                                                | 20.9 ms: 1.06x faster                                  |
| genshi_xml              | 52.1 ms                                                | 49.3 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 136 ms: 1.05x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.11 ms: 1.04x faster                                  |
| html5lib                | 63.2 ms                                                | 60.2 ms: 1.05x faster                                  |
| json                    | 4.95 ms                                                | 4.77 ms: 1.04x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.42 ms: 1.34x faster                                  |
| json_loads              | 26.2 us                                                | 24.0 us: 1.09x faster                                  |
| logging_format          | 6.62 us                                                | 6.49 us: 1.02x faster                                  |
| logging_silent          | 98.5 ns                                                | 93.3 ns: 1.06x faster                                  |
| logging_simple          | 6.06 us                                                | 5.83 us: 1.04x faster                                  |
| mako                    | 9.85 ms                                                | 9.79 ms: 1.01x faster                                  |
| mdp                     | 2.62 sec                                               | 2.69 sec: 1.03x slower                                 |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.03x faster                                   |
| mypy                    | 669 ms                                                 | 799 ms: 1.20x slower                                   |
| nqueens                 | 85.0 ms                                                | 80.9 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.6 ms: 1.03x faster                                  |
| pickle                  | 9.79 us                                                | 10.3 us: 1.05x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.1 us: 1.01x faster                                  |
| pickle_list             | 4.17 us                                                | 3.99 us: 1.05x faster                                  |
| pickle_pure_python      | 304 us                                                 | 285 us: 1.07x faster                                   |
| pidigits                | 199 ms                                                 | 193 ms: 1.03x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 669 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.08 sec: 1.08x faster                                 |
| pyflate                 | 417 ms                                                 | 409 ms: 1.02x faster                                   |
| python_startup          | 8.36 ms                                                | 8.32 ms: 1.00x faster                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.03 ms: 1.01x slower                                  |
| regex_compile           | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_dna               | 203 ms                                                 | 205 ms: 1.01x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.40 ms: 1.01x slower                                  |
| regex_v8                | 22.3 ms                                                | 21.4 ms: 1.04x faster                                  |
| richards                | 46.2 ms                                                | 45.2 ms: 1.02x faster                                  |
| scimark_fft             | 329 ms                                                 | 311 ms: 1.06x faster                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 67.0 ms: 1.02x faster                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.11x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.04 ms: 1.09x faster                                  |
| spectral_norm           | 99.9 ms                                                | 95.4 ms: 1.05x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.33 ms: 1.03x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.63 ms: 1.02x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.0 ms: 1.04x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.60 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 456 ms: 1.04x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                  |
| sympy_sum               | 166 ms                                                 | 163 ms: 1.02x faster                                   |
| sympy_str               | 287 ms                                                 | 280 ms: 1.03x faster                                   |
| telco                   | 6.62 ms                                                | 6.43 ms: 1.03x faster                                  |
| thrift                  | 752 us                                                 | 742 us: 1.01x faster                                   |
| tornado_http            | 96.6 ms                                                | 93.0 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 45.7 ns: 1.05x slower                                  |
| unpickle_list           | 4.95 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 202 us: 1.12x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 144 ms: 1.10x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 106 ms: 1.03x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 76.9 ms: 1.01x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io, nbody, pylint, raytrace, scimark_lu, unpickle
Ignored benchmarks (7) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
