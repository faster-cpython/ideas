Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| chameleon      | 5.86 ms                                                | 5.14 ms: 1.14x faster                                                 |
| docutils       | 1.76 sec                                               | 1.56 sec: 1.13x faster                                                |
| html5lib       | 44.0 ms                                                | 36.9 ms: 1.19x faster                                                 |
| tornado_http   | 90.1 ms                                                | 79.7 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                  | 1.16x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 56.5 ms: 1.28x faster                                                 |
| nbody          | 94.6 ms                                                | 65.2 ms: 1.45x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 78.4 ms: 1.23x faster                                                 |
| regex_dna      | 164 ms                                                 | 163 ms: 1.01x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.50 ms: 1.02x slower                                                 |
| regex_v8       | 17.7 ms                                                | 18.0 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.91 ms: 1.05x faster                                                 |
| json_loads           | 17.0 us                                                | 16.8 us: 1.02x faster                                                 |
| pickle               | 7.50 us                                                | 7.42 us: 1.01x faster                                                 |
| pickle_list          | 2.83 us                                                | 2.85 us: 1.01x slower                                                 |
| pickle_pure_python   | 284 us                                                 | 224 us: 1.27x faster                                                  |
| unpickle             | 10.0 us                                                | 10.1 us: 1.01x slower                                                 |
| unpickle_list        | 2.66 us                                                | 2.50 us: 1.06x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 177 us: 1.15x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.5 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 67.2 ms: 1.03x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 49.9 ms: 1.09x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 37.5 ms: 1.20x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.7 ms: 1.32x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 6.93 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 23.1 ms: 1.18x faster                                                 |
| genshi_text     | 18.2 ms                                                | 16.1 ms: 1.13x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 32.4 ms: 1.16x faster                                                 |
| mako            | 10.6 ms                                                | 8.53 ms: 1.24x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.18x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20211208-darwin-arm64-python-2e91dba437fe5c56c6f8-3.11.0a3-2e91dba |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| async_generators        | 231 ms                                                 | 197 ms: 1.17x faster                                                  |
| async_tree_none         | 396 ms                                                 | 301 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 580 ms: 1.15x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 833 ms: 1.21x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 391 ms: 1.24x faster                                                  |
| chameleon               | 5.86 ms                                                | 5.14 ms: 1.14x faster                                                 |
| chaos                   | 66.5 ms                                                | 49.8 ms: 1.34x faster                                                 |
| bench_mp_pool           | 40.8 ms                                                | 42.1 ms: 1.03x slower                                                 |
| bench_thread_pool       | 531 us                                                 | 501 us: 1.06x faster                                                  |
| coroutines              | 20.1 ms                                                | 18.5 ms: 1.09x faster                                                 |
| coverage                | 40.8 ms                                                | 45.2 ms: 1.11x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 59.6 ms: 1.31x faster                                                 |
| deepcopy                | 278 us                                                 | 240 us: 1.16x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.06 us: 1.15x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 27.9 us: 1.23x faster                                                 |
| deltablue               | 5.37 ms                                                | 3.12 ms: 1.72x faster                                                 |
| django_template         | 27.2 ms                                                | 23.1 ms: 1.18x faster                                                 |
| docutils                | 1.76 sec                                               | 1.56 sec: 1.13x faster                                                |
| dulwich_log             | 36.4 ms                                                | 30.8 ms: 1.18x faster                                                 |
| fannkuch                | 318 ms                                                 | 269 ms: 1.18x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.79 ms: 1.08x slower                                                 |
| float                   | 72.1 ms                                                | 56.5 ms: 1.28x faster                                                 |
| generators              | 32.5 ms                                                | 27.3 ms: 1.19x faster                                                 |
| genshi_text             | 18.2 ms                                                | 16.1 ms: 1.13x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 32.4 ms: 1.16x faster                                                 |
| go                      | 165 ms                                                 | 119 ms: 1.39x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.74 ms: 1.33x faster                                                 |
| html5lib                | 44.0 ms                                                | 36.9 ms: 1.19x faster                                                 |
| json                    | 3.13 ms                                                | 3.04 ms: 1.03x faster                                                 |
| json_dumps              | 8.34 ms                                                | 7.91 ms: 1.05x faster                                                 |
| json_loads              | 17.0 us                                                | 16.8 us: 1.02x faster                                                 |
| logging_format          | 4.95 us                                                | 3.83 us: 1.29x faster                                                 |
| logging_silent          | 119 ns                                                 | 81.8 ns: 1.46x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.51 us: 1.31x faster                                                 |
| mako                    | 10.6 ms                                                | 8.53 ms: 1.24x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.58 sec: 1.05x faster                                                |
| meteor_contest          | 77.7 ms                                                | 73.8 ms: 1.05x faster                                                 |
| nbody                   | 94.6 ms                                                | 65.2 ms: 1.45x faster                                                 |
| nqueens                 | 68.6 ms                                                | 60.7 ms: 1.13x faster                                                 |
| pathlib                 | 22.2 ms                                                | 21.1 ms: 1.05x faster                                                 |
| pickle                  | 7.50 us                                                | 7.42 us: 1.01x faster                                                 |
| pickle_list             | 2.83 us                                                | 2.85 us: 1.01x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 224 us: 1.27x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 503 ms: 1.21x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 1.03 sec: 1.20x faster                                                |
| pycparser               | 915 ms                                                 | 762 ms: 1.20x faster                                                  |
| pyflate                 | 454 ms                                                 | 347 ms: 1.31x faster                                                  |
| pylint                  | 302 ms                                                 | 280 ms: 1.08x faster                                                  |
| python_startup          | 9.59 ms                                                | 12.7 ms: 1.32x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 6.93 ms: 1.01x faster                                                 |
| raytrace                | 329 ms                                                 | 228 ms: 1.45x faster                                                  |
| regex_compile           | 96.2 ms                                                | 78.4 ms: 1.23x faster                                                 |
| regex_dna               | 164 ms                                                 | 163 ms: 1.01x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.50 ms: 1.02x slower                                                 |
| regex_v8                | 17.7 ms                                                | 18.0 ms: 1.01x slower                                                 |
| richards                | 51.4 ms                                                | 36.4 ms: 1.41x faster                                                 |
| scimark_fft             | 231 ms                                                 | 202 ms: 1.14x faster                                                  |
| scimark_lu              | 110 ms                                                 | 78.9 ms: 1.39x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 51.6 ms: 1.40x faster                                                 |
| scimark_sor             | 126 ms                                                 | 86.7 ms: 1.45x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.25 ms: 1.07x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 76.7 ms: 1.25x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.30 ms: 1.02x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.48 ms: 1.04x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 34.5 ms: 1.10x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 180 ms: 1.11x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.39 us: 1.08x faster                                                 |
| sympy_expand            | 275 ms                                                 | 262 ms: 1.05x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 12.1 ms: 1.10x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 88.7 ms: 1.05x faster                                                 |
| sympy_str               | 169 ms                                                 | 161 ms: 1.05x faster                                                  |
| telco                   | 3.63 ms                                                | 3.56 ms: 1.02x faster                                                 |
| thrift                  | 577 us                                                 | 474 us: 1.22x faster                                                  |
| tornado_http            | 90.1 ms                                                | 79.7 ms: 1.13x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 32.2 ns: 1.19x faster                                                 |
| unpickle                | 10.0 us                                                | 10.1 us: 1.01x slower                                                 |
| unpickle_list           | 2.66 us                                                | 2.50 us: 1.06x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 177 us: 1.15x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.5 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 67.2 ms: 1.03x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 49.9 ms: 1.09x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 37.5 ms: 1.20x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.15x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (5) of public/results/bm-20220323-python-v3.10.4-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, gunicorn, mypy, sqlalchemy_declarative, sqlalchemy_imperative
