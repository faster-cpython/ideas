
# Results vs. 3.10.4

- fork: ericsnowcurrently
- ref: isolate_interned_dic
- machine: linux-x86_64
- commit hash: 969caba
- commit date: 2023-02-28
- overall geometric mean: 1.30x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 250 ms: 1.33x faster                                                              |
| chameleon      | 8.86 ms                                                | 6.33 ms: 1.40x faster                                                             |
| docutils       | 3.18 sec                                               | 2.54 sec: 1.25x faster                                                            |
| html5lib       | 85.8 ms                                                | 61.9 ms: 1.38x faster                                                             |
| tornado_http   | 128 ms                                                 | 95.3 ms: 1.35x faster                                                             |
| Geometric mean | (ref)                                                  | 1.34x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 108 ms                                                 | 73.8 ms: 1.46x faster                                                             |
| nbody          | 136 ms                                                 | 93.6 ms: 1.46x faster                                                             |
| pidigits       | 190 ms                                                 | 189 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                  | 1.29x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 133 ms: 1.31x faster                                                              |
| regex_v8       | 25.0 ms                                                | 21.8 ms: 1.15x faster                                                             |
| regex_dna      | 214 ms                                                 | 200 ms: 1.07x faster                                                              |
| regex_effbot   | 3.21 ms                                                | 3.55 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 285 us: 1.59x faster                                                              |
| unpickle_pure_python | 297 us                                                 | 197 us: 1.51x faster                                                              |
| json_dumps           | 13.5 ms                                                | 9.61 ms: 1.40x faster                                                             |
| xml_etree_process    | 74.5 ms                                                | 55.6 ms: 1.34x faster                                                             |
| json_loads           | 28.9 us                                                | 23.8 us: 1.21x faster                                                             |
| xml_etree_generate   | 93.3 ms                                                | 80.7 ms: 1.16x faster                                                             |
| pickle_list          | 4.50 us                                                | 4.01 us: 1.12x faster                                                             |
| xml_etree_iterparse  | 110 ms                                                 | 99.1 ms: 1.11x faster                                                             |
| xml_etree_parse      | 163 ms                                                 | 148 ms: 1.11x faster                                                              |
| unpickle             | 14.3 us                                                | 13.3 us: 1.07x faster                                                             |
| pickle               | 10.1 us                                                | 9.95 us: 1.02x faster                                                             |
| unpickle_list        | 4.99 us                                                | 4.91 us: 1.02x faster                                                             |
| pickle_dict          | 28.3 us                                                | 29.7 us: 1.05x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.19x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 9.03 ms: 1.54x faster                                                             |
| python_startup_no_site | 5.76 ms                                                | 6.55 ms: 1.14x slower                                                             |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text     | 30.6 ms                                                | 21.5 ms: 1.42x faster                                                             |
| mako            | 14.3 ms                                                | 10.2 ms: 1.40x faster                                                             |
| django_template | 46.3 ms                                                | 33.2 ms: 1.40x faster                                                             |
| genshi_xml      | 63.6 ms                                                | 48.2 ms: 1.32x faster                                                             |
| Geometric mean  | (ref)                                                  | 1.38x faster                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| generators              | 75.8 ms                                                | 30.7 ms: 2.47x faster                                                             |
| deltablue               | 7.39 ms                                                | 3.19 ms: 2.32x faster                                                             |
| logging_silent          | 173 ns                                                 | 92.6 ns: 1.87x faster                                                             |
| scimark_sor             | 193 ms                                                 | 107 ms: 1.80x faster                                                              |
| go                      | 226 ms                                                 | 133 ms: 1.70x faster                                                              |
| richards                | 71.4 ms                                                | 42.2 ms: 1.69x faster                                                             |
| pyflate                 | 675 ms                                                 | 400 ms: 1.69x faster                                                              |
| raytrace                | 461 ms                                                 | 285 ms: 1.62x faster                                                              |
| pickle_pure_python      | 453 us                                                 | 285 us: 1.59x faster                                                              |
| scimark_monte_carlo     | 105 ms                                                 | 66.7 ms: 1.57x faster                                                             |
| chaos                   | 104 ms                                                 | 66.3 ms: 1.57x faster                                                             |
| crypto_pyaes            | 118 ms                                                 | 75.1 ms: 1.57x faster                                                             |
| spectral_norm           | 148 ms                                                 | 95.8 ms: 1.55x faster                                                             |
| python_startup          | 13.9 ms                                                | 9.03 ms: 1.54x faster                                                             |
| hexiom                  | 9.42 ms                                                | 6.11 ms: 1.54x faster                                                             |
| unpickle_pure_python    | 297 us                                                 | 197 us: 1.51x faster                                                              |
| deepcopy_memo           | 50.0 us                                                | 34.1 us: 1.47x faster                                                             |
| float                   | 108 ms                                                 | 73.8 ms: 1.46x faster                                                             |
| nbody                   | 136 ms                                                 | 93.6 ms: 1.46x faster                                                             |
| genshi_text             | 30.6 ms                                                | 21.5 ms: 1.42x faster                                                             |
| scimark_lu              | 158 ms                                                 | 111 ms: 1.42x faster                                                              |
| sqlglot_parse           | 2.04 ms                                                | 1.43 ms: 1.42x faster                                                             |
| pprint_pformat          | 1.97 sec                                               | 1.41 sec: 1.40x faster                                                            |
| json_dumps              | 13.5 ms                                                | 9.61 ms: 1.40x faster                                                             |
| mako                    | 14.3 ms                                                | 10.2 ms: 1.40x faster                                                             |
| chameleon               | 8.86 ms                                                | 6.33 ms: 1.40x faster                                                             |
| sqlglot_transpile       | 2.42 ms                                                | 1.73 ms: 1.40x faster                                                             |
| django_template         | 46.3 ms                                                | 33.2 ms: 1.40x faster                                                             |
| logging_format          | 8.92 us                                                | 6.41 us: 1.39x faster                                                             |
| html5lib                | 85.8 ms                                                | 61.9 ms: 1.38x faster                                                             |
| pycparser               | 1.51 sec                                               | 1.09 sec: 1.38x faster                                                            |
| async_tree_io           | 1.78 sec                                               | 1.29 sec: 1.38x faster                                                            |
| async_tree_none         | 713 ms                                                 | 519 ms: 1.37x faster                                                              |
| logging_simple          | 8.06 us                                                | 5.87 us: 1.37x faster                                                             |
| pprint_safe_repr        | 943 ms                                                 | 687 ms: 1.37x faster                                                              |
| coroutines              | 31.7 ms                                                | 23.1 ms: 1.37x faster                                                             |
| async_tree_memoization  | 854 ms                                                 | 632 ms: 1.35x faster                                                              |
| tornado_http            | 128 ms                                                 | 95.3 ms: 1.35x faster                                                             |
| unpack_sequence         | 59.5 ns                                                | 44.3 ns: 1.34x faster                                                             |
| xml_etree_process       | 74.5 ms                                                | 55.6 ms: 1.34x faster                                                             |
| thrift                  | 1.03 ms                                                | 775 us: 1.33x faster                                                              |
| 2to3                    | 332 ms                                                 | 250 ms: 1.33x faster                                                              |
| aiohttp                 | 1.34 ms                                                | 1.01 ms: 1.32x faster                                                             |
| genshi_xml              | 63.6 ms                                                | 48.2 ms: 1.32x faster                                                             |
| gunicorn                | 1.43 ms                                                | 1.09 ms: 1.31x faster                                                             |
| sqlglot_normalize       | 135 ms                                                 | 103 ms: 1.31x faster                                                              |
| regex_compile           | 174 ms                                                 | 133 ms: 1.31x faster                                                              |
| deepcopy                | 429 us                                                 | 330 us: 1.30x faster                                                              |
| scimark_fft             | 414 ms                                                 | 318 ms: 1.30x faster                                                              |
| sqlglot_optimize        | 65.3 ms                                                | 50.6 ms: 1.29x faster                                                             |
| fannkuch                | 477 ms                                                 | 370 ms: 1.29x faster                                                              |
| async_tree_cpu_io_mixed | 949 ms                                                 | 737 ms: 1.29x faster                                                              |
| deepcopy_reduce         | 3.75 us                                                | 2.94 us: 1.28x faster                                                             |
| docutils                | 3.18 sec                                               | 2.54 sec: 1.25x faster                                                            |
| json_loads              | 28.9 us                                                | 23.8 us: 1.21x faster                                                             |
| sqlalchemy_declarative  | 165 ms                                                 | 137 ms: 1.20x faster                                                              |
| nqueens                 | 99.3 ms                                                | 82.8 ms: 1.20x faster                                                             |
| bench_thread_pool       | 943 us                                                 | 796 us: 1.19x faster                                                              |
| mdp                     | 2.82 sec                                               | 2.38 sec: 1.18x faster                                                            |
| dulwich_log             | 75.5 ms                                                | 64.2 ms: 1.18x faster                                                             |
| json                    | 5.35 ms                                                | 4.59 ms: 1.17x faster                                                             |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.73 ms: 1.16x faster                                                             |
| sympy_integrate         | 23.9 ms                                                | 20.7 ms: 1.16x faster                                                             |
| sympy_expand            | 537 ms                                                 | 464 ms: 1.16x faster                                                              |
| xml_etree_generate      | 93.3 ms                                                | 80.7 ms: 1.16x faster                                                             |
| sqlalchemy_imperative   | 21.0 ms                                                | 18.2 ms: 1.15x faster                                                             |
| regex_v8                | 25.0 ms                                                | 21.8 ms: 1.15x faster                                                             |
| sympy_str               | 324 ms                                                 | 287 ms: 1.13x faster                                                              |
| pathlib                 | 20.0 ms                                                | 17.8 ms: 1.13x faster                                                             |
| pickle_list             | 4.50 us                                                | 4.01 us: 1.12x faster                                                             |
| xml_etree_iterparse     | 110 ms                                                 | 99.1 ms: 1.11x faster                                                             |
| sqlite_synth            | 2.90 us                                                | 2.61 us: 1.11x faster                                                             |
| meteor_contest          | 114 ms                                                 | 103 ms: 1.11x faster                                                              |
| xml_etree_parse         | 163 ms                                                 | 148 ms: 1.11x faster                                                              |
| sympy_sum               | 183 ms                                                 | 169 ms: 1.09x faster                                                              |
| unpickle                | 14.3 us                                                | 13.3 us: 1.07x faster                                                             |
| regex_dna               | 214 ms                                                 | 200 ms: 1.07x faster                                                              |
| telco                   | 6.68 ms                                                | 6.48 ms: 1.03x faster                                                             |
| async_generators        | 428 ms                                                 | 418 ms: 1.02x faster                                                              |
| pickle                  | 10.1 us                                                | 9.95 us: 1.02x faster                                                             |
| unpickle_list           | 4.99 us                                                | 4.91 us: 1.02x faster                                                             |
| pidigits                | 190 ms                                                 | 189 ms: 1.01x faster                                                              |
| pickle_dict             | 28.3 us                                                | 29.7 us: 1.05x slower                                                             |
| regex_effbot            | 3.21 ms                                                | 3.55 ms: 1.11x slower                                                             |
| python_startup_no_site  | 5.76 ms                                                | 6.55 ms: 1.14x slower                                                             |
| coverage                | 75.3 ms                                                | 93.7 ms: 1.24x slower                                                             |
| Geometric mean          | (ref)                                                  | 1.30x faster                                                                      |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (3) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230228-3.12.0a5+-969caba/bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
