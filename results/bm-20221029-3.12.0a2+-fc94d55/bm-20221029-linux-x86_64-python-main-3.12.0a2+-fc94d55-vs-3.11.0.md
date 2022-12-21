Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| chameleon      | 6.41 ms                                                | 6.37 ms: 1.01x faster                                  |
| html5lib       | 63.2 ms                                                | 59.5 ms: 1.06x faster                                  |
| tornado_http   | 96.6 ms                                                | 93.1 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.9 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 98.1 ms: 1.03x slower                                  |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 130 ms: 1.05x faster                                   |
| regex_dna      | 203 ms                                                 | 210 ms: 1.03x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.69 ms: 1.10x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.9 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.31 ms: 1.36x faster                                  |
| json_loads           | 26.2 us                                                | 23.5 us: 1.12x faster                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.07x slower                                  |
| pickle_dict          | 31.4 us                                                | 31.6 us: 1.01x slower                                  |
| pickle_pure_python   | 304 us                                                 | 287 us: 1.06x faster                                   |
| unpickle             | 13.3 us                                                | 12.9 us: 1.02x faster                                  |
| unpickle_pure_python | 225 us                                                 | 205 us: 1.10x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.07x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_process    | 53.8 ms                                                | 53.1 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                           |

Benchmark hidden because not significant (3): pickle_list, unpickle_list, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.37 ms: 1.00x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.08 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.0 ms: 1.01x faster                                  |
| genshi_text     | 22.1 ms                                                | 21.1 ms: 1.05x faster                                  |
| genshi_xml      | 52.1 ms                                                | 49.2 ms: 1.06x faster                                  |
| mako            | 9.85 ms                                                | 9.72 ms: 1.01x faster                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221029-linux-x86_64-python-main-3.12.0a2+-fc94d55 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 248 ms: 1.04x faster                                   |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                  |
| async_tree_none         | 529 ms                                                 | 536 ms: 1.01x slower                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 737 ms: 1.02x faster                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 638 ms: 1.02x slower                                   |
| chameleon               | 6.41 ms                                                | 6.37 ms: 1.01x faster                                  |
| chaos                   | 68.6 ms                                                | 67.4 ms: 1.02x faster                                  |
| coroutines              | 26.1 ms                                                | 24.4 ms: 1.07x faster                                  |
| coverage                | 101 ms                                                 | 97.3 ms: 1.03x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.7 ms: 1.01x slower                                  |
| deepcopy                | 344 us                                                 | 328 us: 1.05x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.91 us: 1.02x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.3 us: 1.06x faster                                  |
| deltablue               | 3.64 ms                                                | 3.30 ms: 1.10x faster                                  |
| django_template         | 32.5 ms                                                | 32.0 ms: 1.01x faster                                  |
| dulwich_log             | 63.9 ms                                                | 61.6 ms: 1.04x faster                                  |
| fannkuch                | 388 ms                                                 | 373 ms: 1.04x faster                                   |
| float                   | 76.3 ms                                                | 72.9 ms: 1.05x faster                                  |
| generators              | 72.2 ms                                                | 72.6 ms: 1.01x slower                                  |
| genshi_text             | 22.1 ms                                                | 21.1 ms: 1.05x faster                                  |
| genshi_xml              | 52.1 ms                                                | 49.2 ms: 1.06x faster                                  |
| go                      | 143 ms                                                 | 137 ms: 1.05x faster                                   |
| gunicorn                | 1.12 ms                                                | 1.08 ms: 1.04x faster                                  |
| hexiom                  | 6.35 ms                                                | 6.22 ms: 1.02x faster                                  |
| html5lib                | 63.2 ms                                                | 59.5 ms: 1.06x faster                                  |
| json                    | 4.95 ms                                                | 4.67 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.31 ms: 1.36x faster                                  |
| json_loads              | 26.2 us                                                | 23.5 us: 1.12x faster                                  |
| logging_format          | 6.62 us                                                | 6.41 us: 1.03x faster                                  |
| logging_silent          | 98.5 ns                                                | 94.4 ns: 1.04x faster                                  |
| logging_simple          | 6.06 us                                                | 5.78 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.72 ms: 1.01x faster                                  |
| mdp                     | 2.62 sec                                               | 2.54 sec: 1.03x faster                                 |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                   |
| mypy                    | 669 ms                                                 | 802 ms: 1.20x slower                                   |
| nbody                   | 95.0 ms                                                | 98.1 ms: 1.03x slower                                  |
| nqueens                 | 85.0 ms                                                | 80.7 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.6 ms: 1.03x faster                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.07x slower                                  |
| pickle_dict             | 31.4 us                                                | 31.6 us: 1.01x slower                                  |
| pickle_pure_python      | 304 us                                                 | 287 us: 1.06x faster                                   |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 670 ms: 1.03x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.37 sec: 1.05x faster                                 |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.07x faster                                 |
| pyflate                 | 417 ms                                                 | 399 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.37 ms: 1.00x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.08 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 285 ms: 1.02x faster                                   |
| regex_compile           | 136 ms                                                 | 130 ms: 1.05x faster                                   |
| regex_dna               | 203 ms                                                 | 210 ms: 1.03x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.69 ms: 1.10x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.9 ms: 1.03x slower                                  |
| richards                | 46.2 ms                                                | 43.4 ms: 1.06x faster                                  |
| scimark_fft             | 329 ms                                                 | 318 ms: 1.04x faster                                   |
| scimark_lu              | 107 ms                                                 | 110 ms: 1.03x slower                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.6 ms: 1.04x faster                                  |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.27 ms: 1.03x faster                                  |
| spectral_norm           | 99.9 ms                                                | 94.1 ms: 1.06x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.34 ms: 1.03x faster                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.63 ms: 1.02x faster                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.5 ms: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 106 ms: 1.02x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.64 us: 1.06x slower                                  |
| sympy_expand            | 472 ms                                                 | 457 ms: 1.03x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.5 ms: 1.02x faster                                  |
| sympy_sum               | 166 ms                                                 | 164 ms: 1.01x faster                                   |
| sympy_str               | 287 ms                                                 | 282 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.31 ms: 1.05x faster                                  |
| thrift                  | 752 us                                                 | 736 us: 1.02x faster                                   |
| tornado_http            | 96.6 ms                                                | 93.1 ms: 1.04x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 46.0 ns: 1.06x slower                                  |
| unpickle                | 13.3 us                                                | 12.9 us: 1.02x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 205 us: 1.10x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.07x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                   |
| xml_etree_process       | 53.8 ms                                                | 53.1 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (4): pickle_list, pylint, unpickle_list, xml_etree_generate
Ignored benchmarks (7) of public/results/bm-20221024-python-v3.11.0-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
