
# Results vs. 3.10.4

- fork: barneygale
- ref: optimize_pathlib_par
- machine: linux-x86_64
- commit hash: d5231b6
- commit date: 2023-02-04
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 252 ms: 1.32x faster                                                       |
| chameleon      | 8.86 ms                                                | 6.27 ms: 1.41x faster                                                      |
| docutils       | 3.18 sec                                               | 2.51 sec: 1.27x faster                                                     |
| html5lib       | 85.8 ms                                                | 60.4 ms: 1.42x faster                                                      |
| tornado_http   | 128 ms                                                 | 93.7 ms: 1.37x faster                                                      |
| Geometric mean | (ref)                                                  | 1.36x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 72.2 ms: 1.49x faster                                                      |
| nbody          | 136 ms                                                 | 92.6 ms: 1.47x faster                                                      |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                  | 1.30x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.37x faster                                                       |
| regex_v8       | 25.0 ms                                                | 22.6 ms: 1.10x faster                                                      |
| regex_dna      | 214 ms                                                 | 216 ms: 1.01x slower                                                       |
| regex_effbot   | 3.21 ms                                                | 3.59 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                  | 1.07x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 280 us: 1.62x faster                                                       |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.50x faster                                                       |
| json_dumps           | 13.5 ms                                                | 9.22 ms: 1.46x faster                                                      |
| xml_etree_process    | 74.5 ms                                                | 54.0 ms: 1.38x faster                                                      |
| json_loads           | 28.9 us                                                | 23.9 us: 1.21x faster                                                      |
| xml_etree_generate   | 93.3 ms                                                | 77.7 ms: 1.20x faster                                                      |
| xml_etree_parse      | 163 ms                                                 | 146 ms: 1.12x faster                                                       |
| pickle_list          | 4.50 us                                                | 4.17 us: 1.08x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                 | 102 ms: 1.08x faster                                                       |
| unpickle             | 14.3 us                                                | 13.5 us: 1.05x faster                                                      |
| pickle               | 10.1 us                                                | 10.1 us: 1.01x faster                                                      |
| pickle_dict          | 28.3 us                                                | 30.6 us: 1.08x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.18x faster                                                               |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.91 ms: 1.56x faster                                                      |
| python_startup_no_site | 5.76 ms                                                | 6.44 ms: 1.12x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.18x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 20.8 ms: 1.48x faster                                                      |
| mako            | 14.3 ms                                                | 9.74 ms: 1.46x faster                                                      |
| django_template | 46.3 ms                                                | 32.6 ms: 1.42x faster                                                      |
| genshi_xml      | 63.6 ms                                                | 46.5 ms: 1.37x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.43x faster                                                               |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.19 ms: 2.32x faster                                                      |
| logging_silent          | 173 ns                                                 | 94.0 ns: 1.84x faster                                                      |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.80x faster                                                       |
| pyflate                 | 675 ms                                                 | 397 ms: 1.70x faster                                                       |
| richards                | 71.4 ms                                                | 42.3 ms: 1.69x faster                                                      |
| go                      | 226 ms                                                 | 135 ms: 1.67x faster                                                       |
| raytrace                | 461 ms                                                 | 281 ms: 1.64x faster                                                       |
| chaos                   | 104 ms                                                 | 63.6 ms: 1.64x faster                                                      |
| pickle_pure_python      | 453 us                                                 | 280 us: 1.62x faster                                                       |
| scimark_monte_carlo     | 105 ms                                                 | 65.1 ms: 1.61x faster                                                      |
| crypto_pyaes            | 118 ms                                                 | 73.4 ms: 1.60x faster                                                      |
| spectral_norm           | 148 ms                                                 | 94.5 ms: 1.57x faster                                                      |
| python_startup          | 13.9 ms                                                | 8.91 ms: 1.56x faster                                                      |
| hexiom                  | 9.42 ms                                                | 6.03 ms: 1.56x faster                                                      |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.50x faster                                                       |
| float                   | 108 ms                                                 | 72.2 ms: 1.49x faster                                                      |
| genshi_text             | 30.6 ms                                                | 20.8 ms: 1.48x faster                                                      |
| nbody                   | 136 ms                                                 | 92.6 ms: 1.47x faster                                                      |
| mako                    | 14.3 ms                                                | 9.74 ms: 1.46x faster                                                      |
| json_dumps              | 13.5 ms                                                | 9.22 ms: 1.46x faster                                                      |
| deepcopy_memo           | 50.0 us                                                | 34.5 us: 1.45x faster                                                      |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                                     |
| scimark_lu              | 158 ms                                                 | 110 ms: 1.44x faster                                                       |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.42x faster                                                      |
| django_template         | 46.3 ms                                                | 32.6 ms: 1.42x faster                                                      |
| html5lib                | 85.8 ms                                                | 60.4 ms: 1.42x faster                                                      |
| pprint_safe_repr        | 943 ms                                                 | 666 ms: 1.42x faster                                                       |
| chameleon               | 8.86 ms                                                | 6.27 ms: 1.41x faster                                                      |
| logging_simple          | 8.06 us                                                | 5.72 us: 1.41x faster                                                      |
| sqlglot_transpile       | 2.42 ms                                                | 1.72 ms: 1.40x faster                                                      |
| logging_format          | 8.92 us                                                | 6.36 us: 1.40x faster                                                      |
| unpack_sequence         | 59.5 ns                                                | 43.1 ns: 1.38x faster                                                      |
| xml_etree_process       | 74.5 ms                                                | 54.0 ms: 1.38x faster                                                      |
| scimark_sparse_mat_mult | 5.48 ms                                                | 3.99 ms: 1.37x faster                                                      |
| thrift                  | 1.03 ms                                                | 752 us: 1.37x faster                                                       |
| scimark_fft             | 414 ms                                                 | 302 ms: 1.37x faster                                                       |
| tornado_http            | 128 ms                                                 | 93.7 ms: 1.37x faster                                                      |
| genshi_xml              | 63.6 ms                                                | 46.5 ms: 1.37x faster                                                      |
| regex_compile           | 174 ms                                                 | 127 ms: 1.37x faster                                                       |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.36x faster                                                     |
| async_tree_none         | 713 ms                                                 | 525 ms: 1.36x faster                                                       |
| aiohttp                 | 1.34 ms                                                | 995 us: 1.34x faster                                                       |
| gunicorn                | 1.43 ms                                                | 1.07 ms: 1.34x faster                                                      |
| fannkuch                | 477 ms                                                 | 359 ms: 1.33x faster                                                       |
| 2to3                    | 332 ms                                                 | 252 ms: 1.32x faster                                                       |
| pycparser               | 1.51 sec                                               | 1.15 sec: 1.31x faster                                                     |
| deepcopy                | 429 us                                                 | 328 us: 1.31x faster                                                       |
| async_tree_memoization  | 854 ms                                                 | 654 ms: 1.30x faster                                                       |
| nqueens                 | 99.3 ms                                                | 77.0 ms: 1.29x faster                                                      |
| deepcopy_reduce         | 3.75 us                                                | 2.93 us: 1.28x faster                                                      |
| sqlglot_normalize       | 135 ms                                                 | 106 ms: 1.28x faster                                                       |
| sqlglot_optimize        | 65.3 ms                                                | 51.1 ms: 1.28x faster                                                      |
| coroutines              | 31.7 ms                                                | 24.8 ms: 1.28x faster                                                      |
| docutils                | 3.18 sec                                               | 2.51 sec: 1.27x faster                                                     |
| async_tree_cpu_io_mixed | 949 ms                                                 | 757 ms: 1.25x faster                                                       |
| mypy                    | 1.01 sec                                               | 810 ms: 1.25x faster                                                       |
| async_generators        | 428 ms                                                 | 350 ms: 1.22x faster                                                       |
| sympy_integrate         | 23.9 ms                                                | 19.8 ms: 1.21x faster                                                      |
| json_loads              | 28.9 us                                                | 23.9 us: 1.21x faster                                                      |
| sympy_str               | 324 ms                                                 | 269 ms: 1.21x faster                                                       |
| dulwich_log             | 75.5 ms                                                | 62.8 ms: 1.20x faster                                                      |
| bench_thread_pool       | 943 us                                                 | 785 us: 1.20x faster                                                       |
| xml_etree_generate      | 93.3 ms                                                | 77.7 ms: 1.20x faster                                                      |
| sympy_sum               | 183 ms                                                 | 155 ms: 1.18x faster                                                       |
| sympy_expand            | 537 ms                                                 | 456 ms: 1.18x faster                                                       |
| mdp                     | 2.82 sec                                               | 2.44 sec: 1.16x faster                                                     |
| json                    | 5.35 ms                                                | 4.63 ms: 1.16x faster                                                      |
| xml_etree_parse         | 163 ms                                                 | 146 ms: 1.12x faster                                                       |
| sqlite_synth            | 2.90 us                                                | 2.61 us: 1.11x faster                                                      |
| regex_v8                | 25.0 ms                                                | 22.6 ms: 1.10x faster                                                      |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.09x faster                                                       |
| pickle_list             | 4.50 us                                                | 4.17 us: 1.08x faster                                                      |
| xml_etree_iterparse     | 110 ms                                                 | 102 ms: 1.08x faster                                                       |
| pathlib                 | 20.0 ms                                                | 19.0 ms: 1.06x faster                                                      |
| unpickle                | 14.3 us                                                | 13.5 us: 1.05x faster                                                      |
| telco                   | 6.68 ms                                                | 6.41 ms: 1.04x faster                                                      |
| generators              | 75.8 ms                                                | 74.2 ms: 1.02x faster                                                      |
| pickle                  | 10.1 us                                                | 10.1 us: 1.01x faster                                                      |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                                       |
| regex_dna               | 214 ms                                                 | 216 ms: 1.01x slower                                                       |
| pickle_dict             | 28.3 us                                                | 30.6 us: 1.08x slower                                                      |
| python_startup_no_site  | 5.76 ms                                                | 6.44 ms: 1.12x slower                                                      |
| regex_effbot            | 3.21 ms                                                | 3.59 ms: 1.12x slower                                                      |
| coverage                | 75.3 ms                                                | 95.1 ms: 1.26x slower                                                      |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                               |

Benchmark hidden because not significant (2): unpickle_list, bench_mp_pool
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of public/results/bm-20230204-3.12.0a4+-d5231b6/bm-20230204-linux-x86_64-barneygale-optimize_pathlib_par-3.12.0a4+-d5231b6.json: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
