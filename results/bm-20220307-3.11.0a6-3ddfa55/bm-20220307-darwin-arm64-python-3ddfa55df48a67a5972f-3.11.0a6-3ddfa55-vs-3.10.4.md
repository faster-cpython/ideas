Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| chameleon      | 5.86 ms                                                | 4.64 ms: 1.26x faster                                                 |
| docutils       | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| html5lib       | 44.0 ms                                                | 33.3 ms: 1.32x faster                                                 |
| tornado_http   | 90.1 ms                                                | 73.9 ms: 1.22x faster                                                 |
| Geometric mean | (ref)                                                  | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.1 ms                                                | 53.8 ms: 1.34x faster                                                 |
| nbody          | 94.6 ms                                                | 66.0 ms: 1.43x faster                                                 |
| pidigits       | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 76.1 ms: 1.26x faster                                                 |
| regex_dna      | 164 ms                                                 | 162 ms: 1.02x faster                                                  |
| regex_effbot   | 2.45 ms                                                | 2.45 ms: 1.00x faster                                                 |
| regex_v8       | 17.7 ms                                                | 18.2 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 7.68 ms: 1.09x faster                                                 |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                 |
| pickle               | 7.50 us                                                | 7.24 us: 1.04x faster                                                 |
| pickle_dict          | 18.0 us                                                | 18.2 us: 1.01x slower                                                 |
| pickle_pure_python   | 284 us                                                 | 205 us: 1.38x faster                                                  |
| unpickle_list        | 2.66 us                                                | 2.63 us: 1.01x faster                                                 |
| unpickle_pure_python | 204 us                                                 | 169 us: 1.21x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 95.4 ms: 1.05x faster                                                 |
| xml_etree_iterparse  | 69.0 ms                                                | 64.8 ms: 1.07x faster                                                 |
| xml_etree_generate   | 54.5 ms                                                | 48.0 ms: 1.14x faster                                                 |
| xml_etree_process    | 45.1 ms                                                | 35.7 ms: 1.26x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (2): pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.9 ms: 1.35x slower                                                 |
| python_startup_no_site | 7.00 ms                                                | 7.12 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 27.2 ms                                                | 22.2 ms: 1.23x faster                                                 |
| genshi_text     | 18.2 ms                                                | 15.0 ms: 1.21x faster                                                 |
| genshi_xml      | 37.7 ms                                                | 31.6 ms: 1.19x faster                                                 |
| mako            | 10.6 ms                                                | 7.66 ms: 1.38x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.25x faster                                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20220307-darwin-arm64-python-3ddfa55df48a67a5972f-3.11.0a6-3ddfa55 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 185 ms: 1.20x faster                                                  |
| aiohttp                 | 1.19 ms                                                | 1.01 ms: 1.18x faster                                                 |
| async_generators        | 231 ms                                                 | 195 ms: 1.18x faster                                                  |
| async_tree_none         | 396 ms                                                 | 284 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 538 ms: 1.24x faster                                                  |
| async_tree_io           | 1.01 sec                                               | 701 ms: 1.44x faster                                                  |
| async_tree_memoization  | 485 ms                                                 | 376 ms: 1.29x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.64 ms: 1.26x faster                                                 |
| chaos                   | 66.5 ms                                                | 48.2 ms: 1.38x faster                                                 |
| bench_mp_pool           | 40.8 ms                                                | 44.8 ms: 1.10x slower                                                 |
| bench_thread_pool       | 531 us                                                 | 495 us: 1.07x faster                                                  |
| coroutines              | 20.1 ms                                                | 18.7 ms: 1.07x faster                                                 |
| coverage                | 40.8 ms                                                | 50.4 ms: 1.23x slower                                                 |
| crypto_pyaes            | 77.9 ms                                                | 57.2 ms: 1.36x faster                                                 |
| deepcopy                | 278 us                                                 | 232 us: 1.20x faster                                                  |
| deepcopy_reduce         | 2.36 us                                                | 2.01 us: 1.18x faster                                                 |
| deepcopy_memo           | 34.4 us                                                | 27.4 us: 1.26x faster                                                 |
| deltablue               | 5.37 ms                                                | 2.97 ms: 1.81x faster                                                 |
| django_template         | 27.2 ms                                                | 22.2 ms: 1.23x faster                                                 |
| docutils                | 1.76 sec                                               | 1.48 sec: 1.19x faster                                                |
| dulwich_log             | 36.4 ms                                                | 30.0 ms: 1.22x faster                                                 |
| fannkuch                | 318 ms                                                 | 266 ms: 1.20x faster                                                  |
| flaskblogging           | 2.59 ms                                                | 2.31 ms: 1.12x faster                                                 |
| float                   | 72.1 ms                                                | 53.8 ms: 1.34x faster                                                 |
| generators              | 32.5 ms                                                | 29.0 ms: 1.12x faster                                                 |
| genshi_text             | 18.2 ms                                                | 15.0 ms: 1.21x faster                                                 |
| genshi_xml              | 37.7 ms                                                | 31.6 ms: 1.19x faster                                                 |
| go                      | 165 ms                                                 | 109 ms: 1.52x faster                                                  |
| gunicorn                | 1.28 ms                                                | 1.12 ms: 1.14x faster                                                 |
| hexiom                  | 6.31 ms                                                | 4.66 ms: 1.35x faster                                                 |
| html5lib                | 44.0 ms                                                | 33.3 ms: 1.32x faster                                                 |
| json                    | 3.13 ms                                                | 2.83 ms: 1.10x faster                                                 |
| json_dumps              | 8.34 ms                                                | 7.68 ms: 1.09x faster                                                 |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                 |
| logging_format          | 4.95 us                                                | 3.31 us: 1.50x faster                                                 |
| logging_silent          | 119 ns                                                 | 73.9 ns: 1.61x faster                                                 |
| logging_simple          | 4.61 us                                                | 3.03 us: 1.52x faster                                                 |
| mako                    | 10.6 ms                                                | 7.66 ms: 1.38x faster                                                 |
| mdp                     | 1.66 sec                                               | 1.58 sec: 1.05x faster                                                |
| meteor_contest          | 77.7 ms                                                | 74.3 ms: 1.05x faster                                                 |
| nbody                   | 94.6 ms                                                | 66.0 ms: 1.43x faster                                                 |
| nqueens                 | 68.6 ms                                                | 61.2 ms: 1.12x faster                                                 |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                                 |
| pickle                  | 7.50 us                                                | 7.24 us: 1.04x faster                                                 |
| pickle_dict             | 18.0 us                                                | 18.2 us: 1.01x slower                                                 |
| pickle_pure_python      | 284 us                                                 | 205 us: 1.38x faster                                                  |
| pidigits                | 284 ms                                                 | 282 ms: 1.01x faster                                                  |
| pprint_safe_repr        | 608 ms                                                 | 490 ms: 1.24x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 998 ms: 1.24x faster                                                  |
| pycparser               | 915 ms                                                 | 739 ms: 1.24x faster                                                  |
| pyflate                 | 454 ms                                                 | 325 ms: 1.40x faster                                                  |
| pylint                  | 302 ms                                                 | 276 ms: 1.09x faster                                                  |
| python_startup          | 9.59 ms                                                | 12.9 ms: 1.35x slower                                                 |
| python_startup_no_site  | 7.00 ms                                                | 7.12 ms: 1.02x slower                                                 |
| raytrace                | 329 ms                                                 | 216 ms: 1.52x faster                                                  |
| regex_compile           | 96.2 ms                                                | 76.1 ms: 1.26x faster                                                 |
| regex_dna               | 164 ms                                                 | 162 ms: 1.02x faster                                                  |
| regex_effbot            | 2.45 ms                                                | 2.45 ms: 1.00x faster                                                 |
| regex_v8                | 17.7 ms                                                | 18.2 ms: 1.02x slower                                                 |
| richards                | 51.4 ms                                                | 33.4 ms: 1.54x faster                                                 |
| scimark_fft             | 231 ms                                                 | 203 ms: 1.14x faster                                                  |
| scimark_lu              | 110 ms                                                 | 74.7 ms: 1.47x faster                                                 |
| scimark_monte_carlo     | 72.3 ms                                                | 51.3 ms: 1.41x faster                                                 |
| scimark_sor             | 126 ms                                                 | 80.0 ms: 1.58x faster                                                 |
| scimark_sparse_mat_mult | 3.47 ms                                                | 3.25 ms: 1.07x faster                                                 |
| spectral_norm           | 95.8 ms                                                | 76.6 ms: 1.25x faster                                                 |
| sqlalchemy_declarative  | 74.4 ms                                                | 64.4 ms: 1.15x faster                                                 |
| sqlalchemy_imperative   | 9.01 ms                                                | 7.49 ms: 1.20x faster                                                 |
| sqlglot_parse           | 1.33 ms                                                | 1.18 ms: 1.13x faster                                                 |
| sqlglot_transpile       | 1.54 ms                                                | 1.35 ms: 1.14x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 32.9 ms: 1.16x faster                                                 |
| sqlglot_normalize       | 198 ms                                                 | 175 ms: 1.13x faster                                                  |
| sqlite_synth            | 1.50 us                                                | 1.30 us: 1.15x faster                                                 |
| sympy_expand            | 275 ms                                                 | 250 ms: 1.10x faster                                                  |
| sympy_integrate         | 13.3 ms                                                | 11.5 ms: 1.15x faster                                                 |
| sympy_sum               | 93.5 ms                                                | 84.9 ms: 1.10x faster                                                 |
| sympy_str               | 169 ms                                                 | 152 ms: 1.11x faster                                                  |
| telco                   | 3.63 ms                                                | 3.51 ms: 1.03x faster                                                 |
| thrift                  | 577 us                                                 | 446 us: 1.29x faster                                                  |
| tornado_http            | 90.1 ms                                                | 73.9 ms: 1.22x faster                                                 |
| unpack_sequence         | 38.2 ns                                                | 90.4 ns: 2.36x slower                                                 |
| unpickle_list           | 2.66 us                                                | 2.63 us: 1.01x faster                                                 |
| unpickle_pure_python    | 204 us                                                 | 169 us: 1.21x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 95.4 ms: 1.05x faster                                                 |
| xml_etree_iterparse     | 69.0 ms                                                | 64.8 ms: 1.07x faster                                                 |
| xml_etree_generate      | 54.5 ms                                                | 48.0 ms: 1.14x faster                                                 |
| xml_etree_process       | 45.1 ms                                                | 35.7 ms: 1.26x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.17x faster                                                          |

Benchmark hidden because not significant (2): pickle_list, unpickle
Ignored benchmarks (1) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: mypy
