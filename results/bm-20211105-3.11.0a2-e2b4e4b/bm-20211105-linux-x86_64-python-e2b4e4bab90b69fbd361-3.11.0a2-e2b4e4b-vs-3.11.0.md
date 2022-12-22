Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 274 ms: 1.06x slower                                                  |
| chameleon      | 6.41 ms                                                | 7.46 ms: 1.16x slower                                                 |
| docutils       | 2.60 sec                                               | 2.79 sec: 1.08x slower                                                |
| html5lib       | 63.2 ms                                                | 71.5 ms: 1.13x slower                                                 |
| tornado_http   | 96.6 ms                                                | 111 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 83.3 ms: 1.09x slower                                                 |
| nbody          | 95.0 ms                                                | 112 ms: 1.18x slower                                                  |
| pidigits       | 199 ms                                                 | 188 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 145 ms: 1.06x slower                                                  |
| regex_dna      | 203 ms                                                 | 219 ms: 1.08x slower                                                  |
| regex_effbot   | 3.36 ms                                                | 3.26 ms: 1.03x faster                                                 |
| regex_v8       | 22.3 ms                                                | 23.7 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 12.4 ms: 1.02x faster                                                 |
| json_loads           | 26.2 us                                                | 25.9 us: 1.01x faster                                                 |
| pickle               | 9.79 us                                                | 10.1 us: 1.03x slower                                                 |
| pickle_dict          | 31.4 us                                                | 28.6 us: 1.10x faster                                                 |
| pickle_list          | 4.17 us                                                | 4.68 us: 1.12x slower                                                 |
| pickle_pure_python   | 304 us                                                 | 364 us: 1.20x slower                                                  |
| unpickle             | 13.3 us                                                | 13.7 us: 1.03x slower                                                 |
| unpickle_list        | 4.95 us                                                | 5.13 us: 1.04x slower                                                 |
| unpickle_pure_python | 225 us                                                 | 271 us: 1.20x slower                                                  |
| xml_etree_iterparse  | 103 ms                                                 | 110 ms: 1.08x slower                                                  |
| xml_etree_generate   | 76.2 ms                                                | 81.6 ms: 1.07x slower                                                 |
| xml_etree_process    | 53.8 ms                                                | 59.6 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 14.6 ms: 1.74x slower                                                 |
| python_startup_no_site | 5.96 ms                                                | 5.77 ms: 1.03x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 32.5 ms                                                | 37.9 ms: 1.17x slower                                                 |
| genshi_text     | 22.1 ms                                                | 24.6 ms: 1.11x slower                                                 |
| genshi_xml      | 52.1 ms                                                | 56.1 ms: 1.08x slower                                                 |
| mako            | 9.85 ms                                                | 12.1 ms: 1.23x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.15x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 274 ms: 1.06x slower                                                  |
| async_generators        | 359 ms                                                 | 361 ms: 1.00x slower                                                  |
| async_tree_none         | 529 ms                                                 | 518 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed | 752 ms                                                 | 818 ms: 1.09x slower                                                  |
| async_tree_io           | 1.31 sec                                               | 1.41 sec: 1.08x slower                                                |
| async_tree_memoization  | 625 ms                                                 | 676 ms: 1.08x slower                                                  |
| chameleon               | 6.41 ms                                                | 7.46 ms: 1.16x slower                                                 |
| chaos                   | 68.6 ms                                                | 77.1 ms: 1.12x slower                                                 |
| bench_thread_pool       | 810 us                                                 | 892 us: 1.10x slower                                                  |
| coroutines              | 26.1 ms                                                | 28.8 ms: 1.10x slower                                                 |
| coverage                | 101 ms                                                 | 75.8 ms: 1.33x faster                                                 |
| crypto_pyaes            | 73.9 ms                                                | 90.2 ms: 1.22x slower                                                 |
| deepcopy                | 344 us                                                 | 382 us: 1.11x slower                                                  |
| deepcopy_reduce         | 2.97 us                                                | 3.27 us: 1.10x slower                                                 |
| deepcopy_memo           | 36.4 us                                                | 40.4 us: 1.11x slower                                                 |
| deltablue               | 3.64 ms                                                | 4.86 ms: 1.33x slower                                                 |
| django_template         | 32.5 ms                                                | 37.9 ms: 1.17x slower                                                 |
| docutils                | 2.60 sec                                               | 2.79 sec: 1.08x slower                                                |
| dulwich_log             | 63.9 ms                                                | 68.3 ms: 1.07x slower                                                 |
| fannkuch                | 388 ms                                                 | 427 ms: 1.10x slower                                                  |
| flaskblogging           | 7.08 ms                                                | 7.46 ms: 1.05x slower                                                 |
| float                   | 76.3 ms                                                | 83.3 ms: 1.09x slower                                                 |
| generators              | 72.2 ms                                                | 57.4 ms: 1.26x faster                                                 |
| genshi_text             | 22.1 ms                                                | 24.6 ms: 1.11x slower                                                 |
| genshi_xml              | 52.1 ms                                                | 56.1 ms: 1.08x slower                                                 |
| go                      | 143 ms                                                 | 167 ms: 1.17x slower                                                  |
| gunicorn                | 1.12 ms                                                | 1.15 ms: 1.03x slower                                                 |
| hexiom                  | 6.35 ms                                                | 7.42 ms: 1.17x slower                                                 |
| html5lib                | 63.2 ms                                                | 71.5 ms: 1.13x slower                                                 |
| json_dumps              | 12.7 ms                                                | 12.4 ms: 1.02x faster                                                 |
| json_loads              | 26.2 us                                                | 25.9 us: 1.01x faster                                                 |
| logging_format          | 6.62 us                                                | 6.71 us: 1.01x slower                                                 |
| logging_silent          | 98.5 ns                                                | 117 ns: 1.18x slower                                                  |
| mako                    | 9.85 ms                                                | 12.1 ms: 1.23x slower                                                 |
| mdp                     | 2.62 sec                                               | 2.71 sec: 1.03x slower                                                |
| meteor_contest          | 105 ms                                                 | 106 ms: 1.02x slower                                                  |
| nbody                   | 95.0 ms                                                | 112 ms: 1.18x slower                                                  |
| nqueens                 | 85.0 ms                                                | 91.4 ms: 1.07x slower                                                 |
| pathlib                 | 18.2 ms                                                | 19.1 ms: 1.05x slower                                                 |
| pickle                  | 9.79 us                                                | 10.1 us: 1.03x slower                                                 |
| pickle_dict             | 31.4 us                                                | 28.6 us: 1.10x faster                                                 |
| pickle_list             | 4.17 us                                                | 4.68 us: 1.12x slower                                                 |
| pickle_pure_python      | 304 us                                                 | 364 us: 1.20x slower                                                  |
| pidigits                | 199 ms                                                 | 188 ms: 1.06x faster                                                  |
| pprint_safe_repr        | 691 ms                                                 | 763 ms: 1.10x slower                                                  |
| pprint_pformat          | 1.44 sec                                               | 1.58 sec: 1.09x slower                                                |
| pycparser               | 1.17 sec                                               | 1.26 sec: 1.07x slower                                                |
| pyflate                 | 417 ms                                                 | 541 ms: 1.30x slower                                                  |
| python_startup          | 8.36 ms                                                | 14.6 ms: 1.74x slower                                                 |
| python_startup_no_site  | 5.96 ms                                                | 5.77 ms: 1.03x faster                                                 |
| raytrace                | 290 ms                                                 | 326 ms: 1.12x slower                                                  |
| regex_compile           | 136 ms                                                 | 145 ms: 1.06x slower                                                  |
| regex_dna               | 203 ms                                                 | 219 ms: 1.08x slower                                                  |
| regex_effbot            | 3.36 ms                                                | 3.26 ms: 1.03x faster                                                 |
| regex_v8                | 22.3 ms                                                | 23.7 ms: 1.06x slower                                                 |
| richards                | 46.2 ms                                                | 55.7 ms: 1.21x slower                                                 |
| scimark_fft             | 329 ms                                                 | 355 ms: 1.08x slower                                                  |
| scimark_lu              | 107 ms                                                 | 136 ms: 1.27x slower                                                  |
| scimark_monte_carlo     | 68.3 ms                                                | 78.4 ms: 1.15x slower                                                 |
| scimark_sor             | 115 ms                                                 | 156 ms: 1.35x slower                                                  |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.86 ms: 1.10x slower                                                 |
| spectral_norm           | 99.9 ms                                                | 106 ms: 1.06x slower                                                  |
| sqlalchemy_declarative  | 139 ms                                                 | 145 ms: 1.05x slower                                                  |
| sqlalchemy_imperative   | 18.0 ms                                                | 18.8 ms: 1.04x slower                                                 |
| sqlglot_parse           | 1.37 ms                                                | 2.06 ms: 1.50x slower                                                 |
| sqlglot_transpile       | 1.66 ms                                                | 2.37 ms: 1.43x slower                                                 |
| sqlglot_optimize        | 53.0 ms                                                | 58.4 ms: 1.10x slower                                                 |
| sqlglot_normalize       | 108 ms                                                 | 119 ms: 1.11x slower                                                  |
| sqlite_synth            | 2.49 us                                                | 2.76 us: 1.11x slower                                                 |
| sympy_expand            | 472 ms                                                 | 505 ms: 1.07x slower                                                  |
| sympy_integrate         | 20.9 ms                                                | 22.2 ms: 1.07x slower                                                 |
| sympy_sum               | 166 ms                                                 | 170 ms: 1.03x slower                                                  |
| sympy_str               | 287 ms                                                 | 306 ms: 1.07x slower                                                  |
| telco                   | 6.62 ms                                                | 6.50 ms: 1.02x faster                                                 |
| thrift                  | 752 us                                                 | 821 us: 1.09x slower                                                  |
| tornado_http            | 96.6 ms                                                | 111 ms: 1.14x slower                                                  |
| unpickle                | 13.3 us                                                | 13.7 us: 1.03x slower                                                 |
| unpickle_list           | 4.95 us                                                | 5.13 us: 1.04x slower                                                 |
| unpickle_pure_python    | 225 us                                                 | 271 us: 1.20x slower                                                  |
| xml_etree_iterparse     | 103 ms                                                 | 110 ms: 1.08x slower                                                  |
| xml_etree_generate      | 76.2 ms                                                | 81.6 ms: 1.07x slower                                                 |
| xml_etree_process       | 53.8 ms                                                | 59.6 ms: 1.11x slower                                                 |
| Geometric mean          | (ref)                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (6): bench_mp_pool, json, logging_simple, pylint, unpack_sequence, xml_etree_parse
Ignored benchmarks (2) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, mypy
