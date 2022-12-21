Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 181 ms                                                              | 185 ms: 1.02x slower                                                   |
| chameleon      | 4.61 ms                                                             | 4.50 ms: 1.02x faster                                                  |
| html5lib       | 34.7 ms                                                             | 36.1 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                               | 1.00x slower                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 51.7 ms                                                             | 57.0 ms: 1.10x slower                                                  |
| nbody          | 65.2 ms                                                             | 64.4 ms: 1.01x faster                                                  |
| pidigits       | 282 ms                                                              | 283 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                               | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 76.3 ms                                                             | 75.7 ms: 1.01x faster                                                  |
| regex_dna      | 151 ms                                                              | 149 ms: 1.02x faster                                                   |
| regex_effbot   | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                                  |
| regex_v8       | 16.5 ms                                                             | 16.1 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                               | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 7.67 ms                                                             | 6.07 ms: 1.27x faster                                                  |
| json_loads           | 16.1 us                                                             | 16.4 us: 1.01x slower                                                  |
| pickle               | 7.21 us                                                             | 7.61 us: 1.06x slower                                                  |
| pickle_dict          | 17.9 us                                                             | 18.0 us: 1.01x slower                                                  |
| pickle_pure_python   | 200 us                                                              | 209 us: 1.05x slower                                                   |
| unpickle             | 9.68 us                                                             | 9.79 us: 1.01x slower                                                  |
| unpickle_list        | 2.64 us                                                             | 2.62 us: 1.01x faster                                                  |
| unpickle_pure_python | 159 us                                                              | 161 us: 1.01x slower                                                   |
| xml_etree_parse      | 99.6 ms                                                             | 92.9 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 65.6 ms                                                             | 66.3 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                               | 1.01x faster                                                           |

Benchmark hidden because not significant (3): pickle_list, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.19 ms                                                             | 9.49 ms: 1.03x slower                                                  |
| python_startup_no_site | 7.24 ms                                                             | 7.54 ms: 1.04x slower                                                  |
| Geometric mean         | (ref)                                                               | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 21.1 ms                                                             | 21.4 ms: 1.02x slower                                                  |
| genshi_text     | 15.3 ms                                                             | 14.6 ms: 1.05x faster                                                  |
| genshi_xml      | 30.5 ms                                                             | 29.5 ms: 1.03x faster                                                  |
| mako            | 8.40 ms                                                             | 7.29 ms: 1.15x faster                                                  |
| Geometric mean  | (ref)                                                               | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 181 ms                                                              | 185 ms: 1.02x slower                                                   |
| async_generators        | 195 ms                                                              | 204 ms: 1.05x slower                                                   |
| async_tree_none         | 281 ms                                                              | 285 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed | 528 ms                                                              | 543 ms: 1.03x slower                                                   |
| async_tree_io           | 696 ms                                                              | 733 ms: 1.05x slower                                                   |
| async_tree_memoization  | 317 ms                                                              | 322 ms: 1.02x slower                                                   |
| chameleon               | 4.61 ms                                                             | 4.50 ms: 1.02x faster                                                  |
| chaos                   | 49.3 ms                                                             | 50.5 ms: 1.02x slower                                                  |
| bench_thread_pool       | 457 us                                                              | 454 us: 1.01x faster                                                   |
| coroutines              | 17.8 ms                                                             | 19.9 ms: 1.12x slower                                                  |
| coverage                | 58.4 ms                                                             | 57.4 ms: 1.02x faster                                                  |
| crypto_pyaes            | 51.7 ms                                                             | 53.3 ms: 1.03x slower                                                  |
| deepcopy                | 222 us                                                              | 243 us: 1.09x slower                                                   |
| deepcopy_reduce         | 1.90 us                                                             | 2.07 us: 1.09x slower                                                  |
| deepcopy_memo           | 26.2 us                                                             | 30.1 us: 1.15x slower                                                  |
| deltablue               | 2.82 ms                                                             | 2.79 ms: 1.01x faster                                                  |
| django_template         | 21.1 ms                                                             | 21.4 ms: 1.02x slower                                                  |
| dulwich_log             | 29.1 ms                                                             | 29.2 ms: 1.00x slower                                                  |
| fannkuch                | 262 ms                                                              | 270 ms: 1.03x slower                                                   |
| float                   | 51.7 ms                                                             | 57.0 ms: 1.10x slower                                                  |
| generators              | 28.4 ms                                                             | 33.8 ms: 1.19x slower                                                  |
| genshi_text             | 15.3 ms                                                             | 14.6 ms: 1.05x faster                                                  |
| genshi_xml              | 30.5 ms                                                             | 29.5 ms: 1.03x faster                                                  |
| go                      | 109 ms                                                              | 118 ms: 1.08x slower                                                   |
| hexiom                  | 4.73 ms                                                             | 4.92 ms: 1.04x slower                                                  |
| html5lib                | 34.7 ms                                                             | 36.1 ms: 1.04x slower                                                  |
| json                    | 2.83 ms                                                             | 2.88 ms: 1.02x slower                                                  |
| json_dumps              | 7.67 ms                                                             | 6.07 ms: 1.27x faster                                                  |
| json_loads              | 16.1 us                                                             | 16.4 us: 1.01x slower                                                  |
| logging_format          | 3.73 us                                                             | 3.93 us: 1.05x slower                                                  |
| logging_silent          | 67.4 ns                                                             | 64.2 ns: 1.05x faster                                                  |
| logging_simple          | 3.47 us                                                             | 3.64 us: 1.05x slower                                                  |
| mako                    | 8.40 ms                                                             | 7.29 ms: 1.15x faster                                                  |
| meteor_contest          | 73.9 ms                                                             | 77.6 ms: 1.05x slower                                                  |
| nbody                   | 65.2 ms                                                             | 64.4 ms: 1.01x faster                                                  |
| nqueens                 | 59.5 ms                                                             | 61.7 ms: 1.04x slower                                                  |
| pathlib                 | 20.6 ms                                                             | 20.4 ms: 1.01x faster                                                  |
| pickle                  | 7.21 us                                                             | 7.61 us: 1.06x slower                                                  |
| pickle_dict             | 17.9 us                                                             | 18.0 us: 1.01x slower                                                  |
| pickle_pure_python      | 200 us                                                              | 209 us: 1.05x slower                                                   |
| pidigits                | 282 ms                                                              | 283 ms: 1.00x slower                                                   |
| pprint_safe_repr        | 467 ms                                                              | 496 ms: 1.06x slower                                                   |
| pprint_pformat          | 953 ms                                                              | 1.01 sec: 1.06x slower                                                 |
| pyflate                 | 313 ms                                                              | 351 ms: 1.12x slower                                                   |
| python_startup          | 9.19 ms                                                             | 9.49 ms: 1.03x slower                                                  |
| python_startup_no_site  | 7.24 ms                                                             | 7.54 ms: 1.04x slower                                                  |
| raytrace                | 207 ms                                                              | 219 ms: 1.06x slower                                                   |
| regex_compile           | 76.3 ms                                                             | 75.7 ms: 1.01x faster                                                  |
| regex_dna               | 151 ms                                                              | 149 ms: 1.02x faster                                                   |
| regex_effbot            | 2.63 ms                                                             | 2.60 ms: 1.01x faster                                                  |
| regex_v8                | 16.5 ms                                                             | 16.1 ms: 1.03x faster                                                  |
| richards                | 32.7 ms                                                             | 31.0 ms: 1.06x faster                                                  |
| scimark_fft             | 201 ms                                                              | 197 ms: 1.02x faster                                                   |
| scimark_lu              | 72.2 ms                                                             | 71.2 ms: 1.01x faster                                                  |
| scimark_monte_carlo     | 46.9 ms                                                             | 55.5 ms: 1.18x slower                                                  |
| scimark_sor             | 83.3 ms                                                             | 98.4 ms: 1.18x slower                                                  |
| scimark_sparse_mat_mult | 3.20 ms                                                             | 2.80 ms: 1.14x faster                                                  |
| spectral_norm           | 72.7 ms                                                             | 72.9 ms: 1.00x slower                                                  |
| sqlglot_parse           | 948 us                                                              | 995 us: 1.05x slower                                                   |
| sqlglot_transpile       | 1.11 ms                                                             | 1.16 ms: 1.04x slower                                                  |
| sqlglot_optimize        | 31.3 ms                                                             | 31.6 ms: 1.01x slower                                                  |
| sqlglot_normalize       | 171 ms                                                              | 174 ms: 1.02x slower                                                   |
| sqlite_synth            | 1.29 us                                                             | 1.41 us: 1.09x slower                                                  |
| sympy_expand            | 242 ms                                                              | 248 ms: 1.02x slower                                                   |
| sympy_integrate         | 11.5 ms                                                             | 11.7 ms: 1.02x slower                                                  |
| sympy_sum               | 85.5 ms                                                             | 87.1 ms: 1.02x slower                                                  |
| sympy_str               | 151 ms                                                              | 154 ms: 1.02x slower                                                   |
| telco                   | 3.39 ms                                                             | 3.42 ms: 1.01x slower                                                  |
| thrift                  | 429 us                                                              | 438 us: 1.02x slower                                                   |
| unpack_sequence         | 33.1 ns                                                             | 61.5 ns: 1.86x slower                                                  |
| unpickle                | 9.68 us                                                             | 9.79 us: 1.01x slower                                                  |
| unpickle_list           | 2.64 us                                                             | 2.62 us: 1.01x faster                                                  |
| unpickle_pure_python    | 159 us                                                              | 161 us: 1.01x slower                                                   |
| xml_etree_parse         | 99.6 ms                                                             | 92.9 ms: 1.07x faster                                                  |
| xml_etree_iterparse     | 65.6 ms                                                             | 66.3 ms: 1.01x slower                                                  |
| Geometric mean          | (ref)                                                               | 1.03x slower                                                           |

Benchmark hidden because not significant (9): bench_mp_pool, docutils, mdp, mypy, pickle_list, pycparser, tornado_http, xml_etree_generate, xml_etree_process
Ignored benchmarks (6) of public/results/bm-20221024-python-deaf509e8fc6e0363bd6-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
