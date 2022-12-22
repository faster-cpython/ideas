Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.69 ms: 1.25x faster                                                 |
| docutils       | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| html5lib       | 44.0 ms                                                | 35.8 ms: 1.23x faster                                                 |
| tornado_http   | 90.1 ms                                                | 69.4 ms: 1.30x faster                                                 |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 55.9 ms: 1.29x faster                                                 |
| nbody          | 94.6 ms                                                | 65.4 ms: 1.45x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                 |
| regex_dna      | 164 ms                                                 | 155 ms: 1.06x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.67 ms: 1.09x slower                                                 |
| regex_v8       | 17.7 ms                                                | 16.7 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.09 ms: 1.37x faster                                                 |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                 |
| pickle_dict          | 18.0 us                                                | 17.9 us: 1.00x faster                                                 |
| pickle_pure_python   | 284 us                                                 | 206 us: 1.37x faster                                                  |
| unpickle             | 10.0 us                                                | 9.68 us: 1.04x faster                                                 |
| unpickle_list        | 2.66 us                                                | 2.54 us: 1.05x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 161 us: 1.27x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.1 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 64.8 ms: 1.06x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 47.5 ms: 1.15x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.22 ms: 1.04x faster                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.30 ms: 1.04x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.8 ms: 1.25x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.3 ms: 1.19x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 30.1 ms: 1.25x faster                                                 |
| mako            | 10.6 ms                                                | 8.14 ms: 1.30x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220919-darwin-arm64-python-5b3a2569f4b4dfb58a8f-3.12.0a0-5b3a256 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| async_generators        | 231 ms                                                 | 201 ms: 1.15x faster                                                  |
| async_tree_none         | 396 ms                                                 | 282 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 529 ms: 1.26x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 732 ms: 1.38x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 381 ms: 1.27x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.69 ms: 1.25x faster                                                 |
| chaos                   | 66.5 ms                                                | 50.7 ms: 1.31x faster                                                 |
| bench_thread_pool       | 531 us                                                 | 455 us: 1.17x faster                                                  |
| coroutines              | 20.1 ms                                                | 19.5 ms: 1.03x faster                                                 |
| coverage                | 40.8 ms                                                | 53.3 ms: 1.31x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 52.0 ms: 1.50x faster                                                 |
| deepcopy                | 278 us                                                 | 240 us: 1.16x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.07 us: 1.14x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 28.7 us: 1.20x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.83 ms: 1.90x faster                                                 |
| django_template         | 27.2 ms                                                | 21.8 ms: 1.25x faster                                                 |
| docutils                | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| dulwich_log             | 36.4 ms                                                | 29.1 ms: 1.25x faster                                                 |
| fannkuch                | 318 ms                                                 | 272 ms: 1.17x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.24 ms: 1.16x faster                                                 |
| float                   | 72.1 ms                                                | 55.9 ms: 1.29x faster                                                 |
| generators              | 32.5 ms                                                | 29.2 ms: 1.11x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.3 ms: 1.19x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 30.1 ms: 1.25x faster                                                 |
| go                      | 165 ms                                                 | 118 ms: 1.39x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.92 ms: 1.28x faster                                                 |
| html5lib                | 44.0 ms                                                | 35.8 ms: 1.23x faster                                                 |
| json                    | 3.13 ms                                                | 2.84 ms: 1.10x faster                                                 |
| json_dumps              | 8.34 ms                                                | 6.09 ms: 1.37x faster                                                 |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                 |
| logging_format          | 4.95 us                                                | 3.94 us: 1.25x faster                                                 |
| logging_silent          | 119 ns                                                 | 66.5 ns: 1.79x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.65 us: 1.26x faster                                                 |
| mako                    | 10.6 ms                                                | 8.14 ms: 1.30x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.09x faster                                                |
| meteor_contest          | 77.7 ms                                                | 77.9 ms: 1.00x slower                                                 |
| mypy                    | 521 ms                                                 | 415 ms: 1.26x faster                                                  |
| nbody                   | 94.6 ms                                                | 65.4 ms: 1.45x faster                                                 |
| nqueens                 | 68.6 ms                                                | 61.2 ms: 1.12x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.6 ms: 1.08x faster                                                 |
| pickle_dict             | 18.0 us                                                | 17.9 us: 1.00x faster                                                 |
| pickle_pure_python      | 284 us                                                 | 206 us: 1.37x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.00x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 496 ms: 1.22x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 1.01 sec: 1.23x faster                                                |
| pycparser               | 915 ms                                                 | 713 ms: 1.28x faster                                                  |
| pyflate                 | 454 ms                                                 | 350 ms: 1.30x faster                                                  |
| pylint                  | 302 ms                                                 | 264 ms: 1.14x faster                                                  |
| python_startup          | 9.59 ms                                                | 9.22 ms: 1.04x faster                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.30 ms: 1.04x slower                                                 |
| raytrace                | 329 ms                                                 | 215 ms: 1.53x faster                                                  |
| regex_compile           | 96.2 ms                                                | 75.6 ms: 1.27x faster                                                 |
| regex_dna               | 164 ms                                                 | 155 ms: 1.06x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.67 ms: 1.09x slower                                                 |
| regex_v8                | 17.7 ms                                                | 16.7 ms: 1.06x faster                                                 |
| richards                | 51.4 ms                                                | 33.3 ms: 1.54x faster                                                 |
| scimark_fft             | 231 ms                                                 | 199 ms: 1.16x faster                                                  |
| scimark_lu              | 110 ms                                                 | 72.4 ms: 1.52x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 54.4 ms: 1.33x faster                                                 |
| scimark_sor             | 126 ms                                                 | 101 ms: 1.24x faster                                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.83 ms: 1.23x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 72.9 ms: 1.31x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 61.3 ms: 1.21x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.07 ms: 1.27x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.00 ms: 1.33x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.17 ms: 1.32x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.9 ms: 1.19x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 174 ms: 1.14x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.45 us: 1.03x faster                                                 |
| sympy_expand            | 275 ms                                                 | 248 ms: 1.11x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.7 ms: 1.14x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 86.1 ms: 1.09x faster                                                 |
| sympy_str               | 169 ms                                                 | 154 ms: 1.10x faster                                                  |
| telco                   | 3.63 ms                                                | 3.36 ms: 1.08x faster                                                 |
| thrift                  | 577 us                                                 | 443 us: 1.30x faster                                                  |
| tornado_http            | 90.1 ms                                                | 69.4 ms: 1.30x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 34.2 ns: 1.12x faster                                                 |
| unpickle                | 10.0 us                                                | 9.68 us: 1.04x faster                                                 |
| unpickle_list           | 2.66 us                                                | 2.54 us: 1.05x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 161 us: 1.27x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.1 ms: 1.04x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 64.8 ms: 1.06x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 47.5 ms: 1.15x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 34.9 ms: 1.29x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.20x faster                                                          |

Benchmark hidden because not significant (3): bench_mp_pool, pickle, pickle_list
Ignored benchmarks (2) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, gunicorn
