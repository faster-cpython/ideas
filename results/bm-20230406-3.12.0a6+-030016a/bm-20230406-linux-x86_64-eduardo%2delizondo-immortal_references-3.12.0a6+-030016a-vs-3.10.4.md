
# Results vs. 3.10.4

- fork: eduardo-elizondo
- ref: immortal_references
- machine: linux-x86_64
- commit hash: 030016a
- commit date: 2023-04-06
- overall geometric mean: 1.22x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 336 ms                                                              | 271 ms: 1.24x faster                                                              |
| chameleon      | 9.13 ms                                                             | 6.94 ms: 1.32x faster                                                             |
| docutils       | 3.19 sec                                                            | 2.80 sec: 1.14x faster                                                            |
| html5lib       | 86.4 ms                                                             | 66.6 ms: 1.30x faster                                                             |
| tornado_http   | 129 ms                                                              | 104 ms: 1.24x faster                                                              |
| Geometric mean | (ref)                                                               | 1.25x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 146 ms                                                              | 91.1 ms: 1.60x faster                                                             |
| float          | 110 ms                                                              | 81.0 ms: 1.36x faster                                                             |
| pidigits       | 190 ms                                                              | 197 ms: 1.04x slower                                                              |
| Geometric mean | (ref)                                                               | 1.28x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                              | 148 ms: 1.20x faster                                                              |
| regex_v8       | 24.9 ms                                                             | 21.9 ms: 1.14x faster                                                             |
| regex_dna      | 213 ms                                                              | 203 ms: 1.05x faster                                                              |
| regex_effbot   | 3.22 ms                                                             | 3.61 ms: 1.12x slower                                                             |
| Geometric mean | (ref)                                                               | 1.06x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_pure_python   | 457 us                                                              | 316 us: 1.45x faster                                                              |
| json_dumps           | 13.7 ms                                                             | 9.96 ms: 1.38x faster                                                             |
| unpickle_pure_python | 300 us                                                              | 219 us: 1.37x faster                                                              |
| xml_etree_process    | 74.8 ms                                                             | 59.0 ms: 1.27x faster                                                             |
| json_loads           | 29.3 us                                                             | 25.8 us: 1.14x faster                                                             |
| xml_etree_generate   | 94.9 ms                                                             | 84.1 ms: 1.13x faster                                                             |
| unpickle             | 15.0 us                                                             | 13.5 us: 1.11x faster                                                             |
| xml_etree_iterparse  | 111 ms                                                              | 102 ms: 1.09x faster                                                              |
| xml_etree_parse      | 164 ms                                                              | 151 ms: 1.08x faster                                                              |
| pickle_list          | 4.73 us                                                             | 4.45 us: 1.06x faster                                                             |
| unpickle_list        | 4.94 us                                                             | 5.14 us: 1.04x slower                                                             |
| pickle               | 10.2 us                                                             | 10.7 us: 1.05x slower                                                             |
| pickle_dict          | 27.8 us                                                             | 31.0 us: 1.11x slower                                                             |
| Geometric mean       | (ref)                                                               | 1.13x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 14.1 ms                                                             | 9.02 ms: 1.57x faster                                                             |
| python_startup_no_site | 5.80 ms                                                             | 6.59 ms: 1.14x slower                                                             |
| Geometric mean         | (ref)                                                               | 1.17x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                             | 11.0 ms: 1.34x faster                                                             |
| genshi_text     | 30.4 ms                                                             | 22.9 ms: 1.33x faster                                                             |
| django_template | 45.8 ms                                                             | 35.6 ms: 1.29x faster                                                             |
| genshi_xml      | 64.3 ms                                                             | 50.5 ms: 1.27x faster                                                             |
| Geometric mean  | (ref)                                                               | 1.31x faster                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20230406-linux-x86_64-eduardo%2delizondo-immortal_references-3.12.0a6+-030016a |
|-------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| generators              | 75.7 ms                                                             | 31.8 ms: 2.38x faster                                                             |
| deltablue               | 7.30 ms                                                             | 3.59 ms: 2.03x faster                                                             |
| asyncio_tcp             | 922 ms                                                              | 517 ms: 1.78x faster                                                              |
| logging_silent          | 169 ns                                                              | 103 ns: 1.65x faster                                                              |
| richards                | 74.2 ms                                                             | 45.9 ms: 1.62x faster                                                             |
| go                      | 226 ms                                                              | 140 ms: 1.61x faster                                                              |
| nbody                   | 146 ms                                                              | 91.1 ms: 1.60x faster                                                             |
| raytrace                | 470 ms                                                              | 298 ms: 1.58x faster                                                              |
| python_startup          | 14.1 ms                                                             | 9.02 ms: 1.57x faster                                                             |
| scimark_monte_carlo     | 109 ms                                                              | 71.9 ms: 1.51x faster                                                             |
| chaos                   | 106 ms                                                              | 70.5 ms: 1.50x faster                                                             |
| hexiom                  | 9.50 ms                                                             | 6.33 ms: 1.50x faster                                                             |
| crypto_pyaes            | 117 ms                                                              | 80.0 ms: 1.46x faster                                                             |
| pickle_pure_python      | 457 us                                                              | 316 us: 1.45x faster                                                              |
| pyflate                 | 671 ms                                                              | 464 ms: 1.45x faster                                                              |
| scimark_sor             | 198 ms                                                              | 137 ms: 1.44x faster                                                              |
| scimark_lu              | 160 ms                                                              | 114 ms: 1.41x faster                                                              |
| spectral_norm           | 150 ms                                                              | 107 ms: 1.41x faster                                                              |
| coroutines              | 31.8 ms                                                             | 22.8 ms: 1.40x faster                                                             |
| json_dumps              | 13.7 ms                                                             | 9.96 ms: 1.38x faster                                                             |
| unpickle_pure_python    | 300 us                                                              | 219 us: 1.37x faster                                                              |
| float                   | 110 ms                                                              | 81.0 ms: 1.36x faster                                                             |
| async_tree_io           | 1.78 sec                                                            | 1.31 sec: 1.36x faster                                                            |
| deepcopy_memo           | 51.8 us                                                             | 38.5 us: 1.34x faster                                                             |
| mako                    | 14.7 ms                                                             | 11.0 ms: 1.34x faster                                                             |
| genshi_text             | 30.4 ms                                                             | 22.9 ms: 1.33x faster                                                             |
| async_tree_none         | 713 ms                                                              | 539 ms: 1.32x faster                                                              |
| pprint_pformat          | 1.98 sec                                                            | 1.50 sec: 1.32x faster                                                            |
| pycparser               | 1.53 sec                                                            | 1.16 sec: 1.32x faster                                                            |
| sqlglot_parse           | 2.07 ms                                                             | 1.57 ms: 1.32x faster                                                             |
| chameleon               | 9.13 ms                                                             | 6.94 ms: 1.32x faster                                                             |
| html5lib                | 86.4 ms                                                             | 66.6 ms: 1.30x faster                                                             |
| logging_format          | 9.07 us                                                             | 7.00 us: 1.30x faster                                                             |
| pprint_safe_repr        | 953 ms                                                              | 737 ms: 1.29x faster                                                              |
| logging_simple          | 8.21 us                                                             | 6.35 us: 1.29x faster                                                             |
| thrift                  | 1.04 ms                                                             | 802 us: 1.29x faster                                                              |
| sqlglot_transpile       | 2.45 ms                                                             | 1.90 ms: 1.29x faster                                                             |
| django_template         | 45.8 ms                                                             | 35.6 ms: 1.29x faster                                                             |
| genshi_xml              | 64.3 ms                                                             | 50.5 ms: 1.27x faster                                                             |
| xml_etree_process       | 74.8 ms                                                             | 59.0 ms: 1.27x faster                                                             |
| async_tree_memoization  | 853 ms                                                              | 680 ms: 1.25x faster                                                              |
| tornado_http            | 129 ms                                                              | 104 ms: 1.24x faster                                                              |
| async_tree_cpu_io_mixed | 944 ms                                                              | 761 ms: 1.24x faster                                                              |
| fannkuch                | 485 ms                                                              | 391 ms: 1.24x faster                                                              |
| 2to3                    | 336 ms                                                              | 271 ms: 1.24x faster                                                              |
| unpack_sequence         | 65.6 ns                                                             | 53.0 ns: 1.24x faster                                                             |
| scimark_sparse_mat_mult | 5.62 ms                                                             | 4.64 ms: 1.21x faster                                                             |
| scimark_fft             | 425 ms                                                              | 352 ms: 1.21x faster                                                              |
| nqueens                 | 98.8 ms                                                             | 81.9 ms: 1.21x faster                                                             |
| regex_compile           | 177 ms                                                              | 148 ms: 1.20x faster                                                              |
| deepcopy                | 438 us                                                              | 367 us: 1.19x faster                                                              |
| mypy2                   | 432 ms                                                              | 366 ms: 1.18x faster                                                              |
| sqlglot_optimize        | 65.3 ms                                                             | 55.6 ms: 1.18x faster                                                             |
| sqlglot_normalize       | 135 ms                                                              | 115 ms: 1.17x faster                                                              |
| deepcopy_reduce         | 3.80 us                                                             | 3.26 us: 1.16x faster                                                             |
| docutils                | 3.19 sec                                                            | 2.80 sec: 1.14x faster                                                            |
| regex_v8                | 24.9 ms                                                             | 21.9 ms: 1.14x faster                                                             |
| bench_thread_pool       | 954 us                                                              | 838 us: 1.14x faster                                                              |
| json_loads              | 29.3 us                                                             | 25.8 us: 1.14x faster                                                             |
| xml_etree_generate      | 94.9 ms                                                             | 84.1 ms: 1.13x faster                                                             |
| sqlalchemy_declarative  | 166 ms                                                              | 149 ms: 1.12x faster                                                              |
| unpickle                | 15.0 us                                                             | 13.5 us: 1.11x faster                                                             |
| create_gc_cycles        | 1.64 ms                                                             | 1.48 ms: 1.11x faster                                                             |
| sqlite_synth            | 2.97 us                                                             | 2.70 us: 1.10x faster                                                             |
| sympy_integrate         | 24.3 ms                                                             | 22.2 ms: 1.10x faster                                                             |
| dulwich_log             | 76.3 ms                                                             | 69.8 ms: 1.09x faster                                                             |
| xml_etree_iterparse     | 111 ms                                                              | 102 ms: 1.09x faster                                                              |
| comprehensions          | 27.3 us                                                             | 25.1 us: 1.08x faster                                                             |
| xml_etree_parse         | 164 ms                                                              | 151 ms: 1.08x faster                                                              |
| sqlalchemy_imperative   | 21.2 ms                                                             | 19.8 ms: 1.07x faster                                                             |
| pathlib                 | 19.8 ms                                                             | 18.5 ms: 1.07x faster                                                             |
| sympy_expand            | 540 ms                                                              | 506 ms: 1.07x faster                                                              |
| djangocms               | 36.3 us                                                             | 34.1 us: 1.07x faster                                                             |
| pickle_list             | 4.73 us                                                             | 4.45 us: 1.06x faster                                                             |
| json                    | 5.41 ms                                                             | 5.15 ms: 1.05x faster                                                             |
| regex_dna               | 213 ms                                                              | 203 ms: 1.05x faster                                                              |
| sympy_str               | 328 ms                                                              | 319 ms: 1.03x faster                                                              |
| mdp                     | 2.75 sec                                                            | 2.68 sec: 1.03x faster                                                            |
| meteor_contest          | 115 ms                                                              | 113 ms: 1.01x faster                                                              |
| sympy_sum               | 185 ms                                                              | 183 ms: 1.01x faster                                                              |
| bench_mp_pool           | 24.0 ms                                                             | 24.0 ms: 1.00x slower                                                             |
| telco                   | 6.67 ms                                                             | 6.73 ms: 1.01x slower                                                             |
| async_generators        | 420 ms                                                              | 429 ms: 1.02x slower                                                              |
| gc_traversal            | 3.53 ms                                                             | 3.66 ms: 1.04x slower                                                             |
| pidigits                | 190 ms                                                              | 197 ms: 1.04x slower                                                              |
| unpickle_list           | 4.94 us                                                             | 5.14 us: 1.04x slower                                                             |
| pickle                  | 10.2 us                                                             | 10.7 us: 1.05x slower                                                             |
| pickle_dict             | 27.8 us                                                             | 31.0 us: 1.11x slower                                                             |
| regex_effbot            | 3.22 ms                                                             | 3.61 ms: 1.12x slower                                                             |
| python_startup_no_site  | 5.80 ms                                                             | 6.59 ms: 1.14x slower                                                             |
| dask                    | 437 ms                                                              | 555 ms: 1.27x slower                                                              |
| coverage                | 70.6 ms                                                             | 98.5 ms: 1.39x slower                                                             |
| Geometric mean          | (ref)                                                               | 1.22x faster                                                                      |
Ignored benchmarks (4) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, pylint
