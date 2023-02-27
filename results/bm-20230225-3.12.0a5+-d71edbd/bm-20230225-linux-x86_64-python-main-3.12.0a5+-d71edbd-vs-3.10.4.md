
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d71edbd
- commit date: 2023-02-25
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.39 ms: 1.39x faster                                  |
| docutils       | 3.18 sec                                               | 2.54 sec: 1.25x faster                                 |
| html5lib       | 85.8 ms                                                | 61.1 ms: 1.40x faster                                  |
| tornado_http   | 128 ms                                                 | 94.3 ms: 1.36x faster                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 73.9 ms: 1.46x faster                                  |
| nbody          | 136 ms                                                 | 96.6 ms: 1.41x faster                                  |
| pidigits       | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 131 ms: 1.33x faster                                   |
| regex_v8       | 25.0 ms                                                | 21.6 ms: 1.15x faster                                  |
| regex_dna      | 214 ms                                                 | 208 ms: 1.03x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.65 ms: 1.14x slower                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 282 us: 1.61x faster                                   |
| unpickle_pure_python | 297 us                                                 | 195 us: 1.52x faster                                   |
| json_dumps           | 13.5 ms                                                | 9.45 ms: 1.43x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 55.0 ms: 1.35x faster                                  |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 80.3 ms: 1.16x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 99.3 ms: 1.11x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.10x faster                                   |
| unpickle             | 14.3 us                                                | 13.2 us: 1.08x faster                                  |
| pickle_list          | 4.50 us                                                | 4.19 us: 1.07x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| pickle               | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.7 us: 1.12x slower                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.01 ms: 1.55x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.54 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                  | 1.17x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.4 ms: 1.50x faster                                  |
| mako            | 14.3 ms                                                | 9.89 ms: 1.44x faster                                  |
| django_template | 46.3 ms                                                | 33.0 ms: 1.40x faster                                  |
| genshi_xml      | 63.6 ms                                                | 46.3 ms: 1.37x faster                                  |
| Geometric mean  | (ref)                                                  | 1.43x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| generators              | 75.8 ms                                                | 29.6 ms: 2.56x faster                                  |
| deltablue               | 7.39 ms                                                | 3.14 ms: 2.36x faster                                  |
| logging_silent          | 173 ns                                                 | 94.4 ns: 1.83x faster                                  |
| scimark_sor             | 193 ms                                                 | 106 ms: 1.82x faster                                   |
| richards                | 71.4 ms                                                | 40.6 ms: 1.76x faster                                  |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                   |
| pyflate                 | 675 ms                                                 | 407 ms: 1.66x faster                                   |
| raytrace                | 461 ms                                                 | 280 ms: 1.65x faster                                   |
| pickle_pure_python      | 453 us                                                 | 282 us: 1.61x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 66.0 ms: 1.59x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 74.7 ms: 1.57x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.01 ms: 1.57x faster                                  |
| chaos                   | 104 ms                                                 | 67.0 ms: 1.55x faster                                  |
| python_startup          | 13.9 ms                                                | 9.01 ms: 1.55x faster                                  |
| spectral_norm           | 148 ms                                                 | 96.4 ms: 1.54x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 195 us: 1.52x faster                                   |
| genshi_text             | 30.6 ms                                                | 20.4 ms: 1.50x faster                                  |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.46x faster                                   |
| float                   | 108 ms                                                 | 73.9 ms: 1.46x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.41 ms: 1.44x faster                                  |
| mako                    | 14.3 ms                                                | 9.89 ms: 1.44x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.7 us: 1.44x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.45 ms: 1.43x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.70 ms: 1.42x faster                                  |
| logging_format          | 8.92 us                                                | 6.31 us: 1.42x faster                                  |
| nbody                   | 136 ms                                                 | 96.6 ms: 1.41x faster                                  |
| pprint_pformat          | 1.97 sec                                               | 1.40 sec: 1.41x faster                                 |
| logging_simple          | 8.06 us                                                | 5.72 us: 1.41x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 42.4 ns: 1.40x faster                                  |
| html5lib                | 85.8 ms                                                | 61.1 ms: 1.40x faster                                  |
| django_template         | 46.3 ms                                                | 33.0 ms: 1.40x faster                                  |
| chameleon               | 8.86 ms                                                | 6.39 ms: 1.39x faster                                  |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.38x faster                                 |
| pprint_safe_repr        | 943 ms                                                 | 681 ms: 1.38x faster                                   |
| coroutines              | 31.7 ms                                                | 23.0 ms: 1.38x faster                                  |
| genshi_xml              | 63.6 ms                                                | 46.3 ms: 1.37x faster                                  |
| async_tree_io           | 1.78 sec                                               | 1.30 sec: 1.37x faster                                 |
| tornado_http            | 128 ms                                                 | 94.3 ms: 1.36x faster                                  |
| async_tree_none         | 713 ms                                                 | 526 ms: 1.36x faster                                   |
| xml_etree_process       | 74.5 ms                                                | 55.0 ms: 1.35x faster                                  |
| 2to3                    | 332 ms                                                 | 248 ms: 1.34x faster                                   |
| thrift                  | 1.03 ms                                                | 771 us: 1.34x faster                                   |
| async_tree_memoization  | 854 ms                                                 | 640 ms: 1.34x faster                                   |
| regex_compile           | 174 ms                                                 | 131 ms: 1.33x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.33x faster                                  |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.32x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 103 ms: 1.31x faster                                   |
| fannkuch                | 477 ms                                                 | 364 ms: 1.31x faster                                   |
| scimark_fft             | 414 ms                                                 | 317 ms: 1.31x faster                                   |
| sqlglot_optimize        | 65.3 ms                                                | 50.5 ms: 1.29x faster                                  |
| deepcopy                | 429 us                                                 | 332 us: 1.29x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 739 ms: 1.28x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.99 us: 1.26x faster                                  |
| docutils                | 3.18 sec                                               | 2.54 sec: 1.25x faster                                 |
| nqueens                 | 99.3 ms                                                | 80.0 ms: 1.24x faster                                  |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                  |
| sqlalchemy_declarative  | 165 ms                                                 | 138 ms: 1.20x faster                                   |
| bench_thread_pool       | 943 us                                                 | 787 us: 1.20x faster                                   |
| dulwich_log             | 75.5 ms                                                | 63.1 ms: 1.20x faster                                  |
| sqlalchemy_imperative   | 21.0 ms                                                | 17.7 ms: 1.19x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.62 ms: 1.19x faster                                  |
| sympy_expand            | 537 ms                                                 | 454 ms: 1.18x faster                                   |
| json                    | 5.35 ms                                                | 4.54 ms: 1.18x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.4 ms: 1.17x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 80.3 ms: 1.16x faster                                  |
| regex_v8                | 25.0 ms                                                | 21.6 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 282 ms: 1.15x faster                                   |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 99.3 ms: 1.11x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.62 us: 1.11x faster                                  |
| sympy_sum               | 183 ms                                                 | 166 ms: 1.10x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.10x faster                                   |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.10x faster                                   |
| unpickle                | 14.3 us                                                | 13.2 us: 1.08x faster                                  |
| pickle_list             | 4.50 us                                                | 4.19 us: 1.07x faster                                  |
| mdp                     | 2.82 sec                                               | 2.66 sec: 1.06x faster                                 |
| regex_dna               | 214 ms                                                 | 208 ms: 1.03x faster                                   |
| async_generators        | 428 ms                                                 | 420 ms: 1.02x faster                                   |
| telco                   | 6.68 ms                                                | 6.57 ms: 1.02x faster                                  |
| pidigits                | 190 ms                                                 | 189 ms: 1.00x faster                                   |
| unpickle_list           | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| pickle                  | 10.1 us                                                | 10.4 us: 1.03x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.7 us: 1.12x slower                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.54 ms: 1.13x slower                                  |
| regex_effbot            | 3.21 ms                                                | 3.65 ms: 1.14x slower                                  |
| coverage                | 75.3 ms                                                | 96.5 ms: 1.28x slower                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (6) of public/results/bm-20230225-3.12.0a5+-d71edbd/bm-20230225-linux-x86_64-python-main-3.12.0a5+-d71edbd.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
