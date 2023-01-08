
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: 951303f
- commit date: 2023-01-07
- overall geometric mean: 1.23x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 182 ms: 1.22x faster                                   |
| chameleon      | 5.86 ms                                                | 4.48 ms: 1.31x faster                                  |
| docutils       | 1.76 sec                                               | 1.43 sec: 1.23x faster                                 |
| html5lib       | 44.0 ms                                                | 34.7 ms: 1.27x faster                                  |
| Geometric mean | (ref)                                                  | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 72.1 ms                                                | 51.6 ms: 1.40x faster                                  |
| nbody          | 94.6 ms                                                | 63.8 ms: 1.48x faster                                  |
| pidigits       | 284 ms                                                 | 277 ms: 1.02x faster                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 75.2 ms: 1.28x faster                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| regex_effbot   | 2.45 ms                                                | 2.61 ms: 1.06x slower                                  |
| regex_v8       | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 8.34 ms                                                | 6.10 ms: 1.37x faster                                  |
| json_loads           | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| pickle_list          | 2.83 us                                                | 2.86 us: 1.01x slower                                  |
| pickle_pure_python   | 284 us                                                 | 192 us: 1.47x faster                                   |
| unpickle             | 10.0 us                                                | 9.05 us: 1.11x faster                                  |
| unpickle_list        | 2.66 us                                                | 2.63 us: 1.01x faster                                  |
| unpickle_pure_python | 204 us                                                 | 142 us: 1.44x faster                                   |
| xml_etree_parse      | 100 ms                                                 | 92.8 ms: 1.08x faster                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 66.2 ms: 1.04x faster                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.5 ms: 1.13x faster                                  |
| xml_etree_process    | 45.1 ms                                                | 34.7 ms: 1.30x faster                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                           |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 9.28 ms: 1.03x faster                                  |
| python_startup_no_site | 7.00 ms                                                | 7.32 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 27.2 ms                                                | 21.3 ms: 1.28x faster                                  |
| genshi_text     | 18.2 ms                                                | 14.3 ms: 1.28x faster                                  |
| genshi_xml      | 37.7 ms                                                | 28.2 ms: 1.34x faster                                  |
| mako            | 10.6 ms                                                | 7.10 ms: 1.49x faster                                  |
| Geometric mean  | (ref)                                                  | 1.34x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230107-darwin-arm64-python-main-3.12.0a3+-951303f |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 222 ms                                                 | 182 ms: 1.22x faster                                   |
| async_generators        | 231 ms                                                 | 200 ms: 1.15x faster                                   |
| async_tree_none         | 396 ms                                                 | 287 ms: 1.38x faster                                   |
| async_tree_cpu_io_mixed | 665 ms                                                 | 541 ms: 1.23x faster                                   |
| async_tree_io           | 1.01 sec                                               | 736 ms: 1.37x faster                                   |
| async_tree_memoization  | 485 ms                                                 | 328 ms: 1.48x faster                                   |
| chameleon               | 5.86 ms                                                | 4.48 ms: 1.31x faster                                  |
| chaos                   | 66.5 ms                                                | 50.3 ms: 1.32x faster                                  |
| bench_mp_pool           | 40.8 ms                                                | 41.9 ms: 1.03x slower                                  |
| bench_thread_pool       | 531 us                                                 | 450 us: 1.18x faster                                   |
| coroutines              | 20.1 ms                                                | 18.8 ms: 1.07x faster                                  |
| coverage                | 40.8 ms                                                | 57.3 ms: 1.41x slower                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.7 ms: 1.45x faster                                  |
| deepcopy                | 278 us                                                 | 219 us: 1.27x faster                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.91 us: 1.24x faster                                  |
| deepcopy_memo           | 34.4 us                                                | 25.6 us: 1.34x faster                                  |
| deltablue               | 5.37 ms                                                | 2.56 ms: 2.10x faster                                  |
| django_template         | 27.2 ms                                                | 21.3 ms: 1.28x faster                                  |
| docutils                | 1.76 sec                                               | 1.43 sec: 1.23x faster                                 |
| dulwich_log             | 36.4 ms                                                | 28.7 ms: 1.27x faster                                  |
| fannkuch                | 318 ms                                                 | 258 ms: 1.23x faster                                   |
| float                   | 72.1 ms                                                | 51.6 ms: 1.40x faster                                  |
| generators              | 32.5 ms                                                | 33.7 ms: 1.04x slower                                  |
| genshi_text             | 18.2 ms                                                | 14.3 ms: 1.28x faster                                  |
| genshi_xml              | 37.7 ms                                                | 28.2 ms: 1.34x faster                                  |
| go                      | 165 ms                                                 | 108 ms: 1.53x faster                                   |
| hexiom                  | 6.31 ms                                                | 4.78 ms: 1.32x faster                                  |
| html5lib                | 44.0 ms                                                | 34.7 ms: 1.27x faster                                  |
| json                    | 3.13 ms                                                | 2.84 ms: 1.10x faster                                  |
| json_dumps              | 8.34 ms                                                | 6.10 ms: 1.37x faster                                  |
| json_loads              | 17.0 us                                                | 16.3 us: 1.04x faster                                  |
| logging_format          | 4.95 us                                                | 3.81 us: 1.30x faster                                  |
| logging_silent          | 119 ns                                                 | 64.9 ns: 1.84x faster                                  |
| logging_simple          | 4.61 us                                                | 3.52 us: 1.31x faster                                  |
| mako                    | 10.6 ms                                                | 7.10 ms: 1.49x faster                                  |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.08x faster                                 |
| meteor_contest          | 77.7 ms                                                | 76.3 ms: 1.02x faster                                  |
| mypy                    | 521 ms                                                 | 413 ms: 1.26x faster                                   |
| nbody                   | 94.6 ms                                                | 63.8 ms: 1.48x faster                                  |
| nqueens                 | 68.6 ms                                                | 60.2 ms: 1.14x faster                                  |
| pathlib                 | 22.2 ms                                                | 20.8 ms: 1.07x faster                                  |
| pickle_list             | 2.83 us                                                | 2.86 us: 1.01x slower                                  |
| pickle_pure_python      | 284 us                                                 | 192 us: 1.47x faster                                   |
| pidigits                | 284 ms                                                 | 277 ms: 1.02x faster                                   |
| pprint_safe_repr        | 608 ms                                                 | 455 ms: 1.33x faster                                   |
| pprint_pformat          | 1.24 sec                                               | 925 ms: 1.34x faster                                   |
| pycparser               | 915 ms                                                 | 685 ms: 1.34x faster                                   |
| pyflate                 | 454 ms                                                 | 322 ms: 1.41x faster                                   |
| python_startup          | 9.59 ms                                                | 9.28 ms: 1.03x faster                                  |
| python_startup_no_site  | 7.00 ms                                                | 7.32 ms: 1.05x slower                                  |
| raytrace                | 329 ms                                                 | 221 ms: 1.49x faster                                   |
| regex_compile           | 96.2 ms                                                | 75.2 ms: 1.28x faster                                  |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                   |
| regex_effbot            | 2.45 ms                                                | 2.61 ms: 1.06x slower                                  |
| regex_v8                | 17.7 ms                                                | 16.1 ms: 1.10x faster                                  |
| richards                | 51.4 ms                                                | 30.4 ms: 1.69x faster                                  |
| scimark_fft             | 231 ms                                                 | 195 ms: 1.18x faster                                   |
| scimark_lu              | 110 ms                                                 | 71.9 ms: 1.53x faster                                  |
| scimark_monte_carlo     | 72.3 ms                                                | 51.0 ms: 1.42x faster                                  |
| scimark_sor             | 126 ms                                                 | 82.4 ms: 1.53x faster                                  |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.82 ms: 1.23x faster                                  |
| spectral_norm           | 95.8 ms                                                | 72.8 ms: 1.32x faster                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.04 ms: 1.28x faster                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.20 ms: 1.29x faster                                  |
| sqlglot_optimize        | 38.1 ms                                                | 31.0 ms: 1.23x faster                                  |
| sqlglot_normalize       | 198 ms                                                 | 170 ms: 1.17x faster                                   |
| sqlite_synth            | 1.50 us                                                | 1.35 us: 1.11x faster                                  |
| sympy_expand            | 275 ms                                                 | 241 ms: 1.14x faster                                   |
| sympy_integrate         | 13.3 ms                                                | 11.4 ms: 1.16x faster                                  |
| sympy_sum               | 93.5 ms                                                | 85.9 ms: 1.09x faster                                  |
| sympy_str               | 169 ms                                                 | 151 ms: 1.12x faster                                   |
| telco                   | 3.63 ms                                                | 3.47 ms: 1.05x faster                                  |
| thrift                  | 577 us                                                 | 439 us: 1.32x faster                                   |
| unpack_sequence         | 38.2 ns                                                | 32.5 ns: 1.18x faster                                  |
| unpickle                | 10.0 us                                                | 9.05 us: 1.11x faster                                  |
| unpickle_list           | 2.66 us                                                | 2.63 us: 1.01x faster                                  |
| unpickle_pure_python    | 204 us                                                 | 142 us: 1.44x faster                                   |
| xml_etree_parse         | 100 ms                                                 | 92.8 ms: 1.08x faster                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 66.2 ms: 1.04x faster                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.5 ms: 1.13x faster                                  |
| xml_etree_process       | 45.1 ms                                                | 34.7 ms: 1.30x faster                                  |
| Geometric mean          | (ref)                                                  | 1.23x faster                                           |

Benchmark hidden because not significant (2): pickle, pickle_dict
Ignored benchmarks (7) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
