
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 61f1e67
- commit date: 2023-02-18
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 247 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.49 ms: 1.37x faster                                  |
| docutils       | 3.18 sec                                               | 2.54 sec: 1.25x faster                                 |
| html5lib       | 85.8 ms                                                | 61.1 ms: 1.40x faster                                  |
| tornado_http   | 128 ms                                                 | 95.2 ms: 1.35x faster                                  |
| Geometric mean | (ref)                                                  | 1.34x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 73.1 ms: 1.47x faster                                  |
| nbody          | 136 ms                                                 | 92.9 ms: 1.47x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| regex_v8       | 25.0 ms                                                | 22.0 ms: 1.13x faster                                  |
| regex_dna      | 214 ms                                                 | 220 ms: 1.03x slower                                   |
| regex_effbot   | 3.21 ms                                                | 3.38 ms: 1.05x slower                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 283 us: 1.60x faster                                   |
| unpickle_pure_python | 297 us                                                 | 198 us: 1.49x faster                                   |
| json_dumps           | 13.5 ms                                                | 9.58 ms: 1.41x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 55.4 ms: 1.34x faster                                  |
| json_loads           | 28.9 us                                                | 23.7 us: 1.22x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 81.2 ms: 1.15x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 100 ms: 1.10x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 149 ms: 1.10x faster                                   |
| unpickle             | 14.3 us                                                | 13.3 us: 1.07x faster                                  |
| pickle_list          | 4.50 us                                                | 4.29 us: 1.05x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.06 us: 1.01x slower                                  |
| pickle_dict          | 28.3 us                                                | 32.5 us: 1.15x slower                                  |
| Geometric mean       | (ref)                                                  | 1.17x faster                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.00 ms: 1.55x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.52 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| mako            | 14.3 ms                                                | 9.92 ms: 1.44x faster                                  |
| django_template | 46.3 ms                                                | 34.0 ms: 1.36x faster                                  |
| genshi_xml      | 63.6 ms                                                | 48.3 ms: 1.32x faster                                  |
| Geometric mean  | (ref)                                                  | 1.39x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.8 ms                                                | 30.5 ms: 2.48x faster                                  |
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.31x faster                                  |
| logging_silent          | 173 ns                                                 | 93.9 ns: 1.85x faster                                  |
| scimark_sor             | 193 ms                                                 | 109 ms: 1.78x faster                                   |
| go                      | 226 ms                                                 | 133 ms: 1.71x faster                                   |
| richards                | 71.4 ms                                                | 42.0 ms: 1.70x faster                                  |
| pyflate                 | 675 ms                                                 | 400 ms: 1.69x faster                                   |
| raytrace                | 461 ms                                                 | 285 ms: 1.62x faster                                   |
| crypto_pyaes            | 118 ms                                                 | 73.2 ms: 1.61x faster                                  |
| pickle_pure_python      | 453 us                                                 | 283 us: 1.60x faster                                   |
| chaos                   | 104 ms                                                 | 65.7 ms: 1.58x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 66.4 ms: 1.58x faster                                  |
| python_startup          | 13.9 ms                                                | 9.00 ms: 1.55x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.13 ms: 1.54x faster                                  |
| spectral_norm           | 148 ms                                                 | 96.6 ms: 1.53x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 198 us: 1.49x faster                                   |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.48x faster                                   |
| float                   | 108 ms                                                 | 73.1 ms: 1.47x faster                                  |
| nbody                   | 136 ms                                                 | 92.9 ms: 1.47x faster                                  |
| genshi_text             | 30.6 ms                                                | 21.0 ms: 1.46x faster                                  |
| mako                    | 14.3 ms                                                | 9.92 ms: 1.44x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.9 us: 1.43x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                 |
| sqlglot_parse           | 2.04 ms                                                | 1.44 ms: 1.41x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.58 ms: 1.41x faster                                  |
| html5lib                | 85.8 ms                                                | 61.1 ms: 1.40x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.73 ms: 1.39x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 42.7 ns: 1.39x faster                                  |
| logging_simple          | 8.06 us                                                | 5.80 us: 1.39x faster                                  |
| pprint_safe_repr        | 943 ms                                                 | 682 ms: 1.38x faster                                   |
| coroutines              | 31.7 ms                                                | 22.9 ms: 1.38x faster                                  |
| logging_format          | 8.92 us                                                | 6.47 us: 1.38x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.98 ms: 1.38x faster                                  |
| chameleon               | 8.86 ms                                                | 6.49 ms: 1.37x faster                                  |
| django_template         | 46.3 ms                                                | 34.0 ms: 1.36x faster                                  |
| scimark_fft             | 414 ms                                                 | 305 ms: 1.36x faster                                   |
| async_tree_none         | 713 ms                                                 | 527 ms: 1.35x faster                                   |
| pycparser               | 1.51 sec                                               | 1.12 sec: 1.35x faster                                 |
| tornado_http            | 128 ms                                                 | 95.2 ms: 1.35x faster                                  |
| thrift                  | 1.03 ms                                                | 766 us: 1.35x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.32 sec: 1.34x faster                                 |
| 2to3                    | 332 ms                                                 | 247 ms: 1.34x faster                                   |
| xml_etree_process       | 74.5 ms                                                | 55.4 ms: 1.34x faster                                  |
| regex_compile           | 174 ms                                                 | 130 ms: 1.34x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                  |
| fannkuch                | 477 ms                                                 | 360 ms: 1.33x faster                                   |
| genshi_xml              | 63.6 ms                                                | 48.3 ms: 1.32x faster                                  |
| async_tree_memoization  | 854 ms                                                 | 649 ms: 1.32x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.31x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.29x faster                                   |
| deepcopy                | 429 us                                                 | 332 us: 1.29x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                | 51.0 ms: 1.28x faster                                  |
| deepcopy_reduce         | 3.75 us                                                | 2.96 us: 1.27x faster                                  |
| async_tree_cpu_io_mixed | 949 ms                                                 | 749 ms: 1.27x faster                                   |
| docutils                | 3.18 sec                                               | 2.54 sec: 1.25x faster                                 |
| nqueens                 | 99.3 ms                                                | 80.0 ms: 1.24x faster                                  |
| json_loads              | 28.9 us                                                | 23.7 us: 1.22x faster                                  |
| sqlalchemy_declarative  | 165 ms                                                 | 137 ms: 1.20x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 19.9 ms: 1.20x faster                                  |
| dulwich_log             | 75.5 ms                                                | 62.9 ms: 1.20x faster                                  |
| bench_thread_pool       | 943 us                                                 | 790 us: 1.19x faster                                   |
| sympy_str               | 324 ms                                                 | 273 ms: 1.19x faster                                   |
| sympy_expand            | 537 ms                                                 | 454 ms: 1.18x faster                                   |
| json                    | 5.35 ms                                                | 4.54 ms: 1.18x faster                                  |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.1 ms: 1.16x faster                                  |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 81.2 ms: 1.15x faster                                  |
| mdp                     | 2.82 sec                                               | 2.48 sec: 1.14x faster                                 |
| regex_v8                | 25.0 ms                                                | 22.0 ms: 1.13x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.59 us: 1.12x faster                                  |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.11x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 100 ms: 1.10x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 149 ms: 1.10x faster                                   |
| pathlib                 | 20.0 ms                                                | 18.3 ms: 1.09x faster                                  |
| unpickle                | 14.3 us                                                | 13.3 us: 1.07x faster                                  |
| pickle_list             | 4.50 us                                                | 4.29 us: 1.05x faster                                  |
| async_generators        | 428 ms                                                 | 411 ms: 1.04x faster                                   |
| telco                   | 6.68 ms                                                | 6.46 ms: 1.03x faster                                  |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| unpickle_list           | 4.99 us                                                | 5.06 us: 1.01x slower                                  |
| regex_dna               | 214 ms                                                 | 220 ms: 1.03x slower                                   |
| regex_effbot            | 3.21 ms                                                | 3.38 ms: 1.05x slower                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.52 ms: 1.13x slower                                  |
| pickle_dict             | 28.3 us                                                | 32.5 us: 1.15x slower                                  |
| coverage                | 75.3 ms                                                | 96.3 ms: 1.28x slower                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (2): pickle, bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230218-3.12.0a5+-61f1e67/bm-20230218-linux-x86_64-python-main-3.12.0a5+-61f1e67.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
