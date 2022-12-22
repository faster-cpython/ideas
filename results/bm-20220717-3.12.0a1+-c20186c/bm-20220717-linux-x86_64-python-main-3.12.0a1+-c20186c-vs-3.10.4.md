Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.28 ms: 1.41x faster                                  |
| html5lib       | 85.8 ms                                                | 62.8 ms: 1.36x faster                                  |
| tornado_http   | 128 ms                                                 | 91.3 ms: 1.41x faster                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 72.0 ms: 1.50x faster                                  |
| nbody          | 136 ms                                                 | 88.8 ms: 1.53x faster                                  |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| Geometric mean | (ref)                                                  | 1.32x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 127 ms: 1.36x faster                                   |
| regex_dna      | 214 ms                                                 | 197 ms: 1.09x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.47 ms: 1.08x slower                                  |
| regex_v8       | 25.0 ms                                                | 20.9 ms: 1.19x faster                                  |
| Geometric mean | (ref)                                                  | 1.13x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 11.9 ms: 1.14x faster                                  |
| json_loads           | 28.9 us                                                | 24.3 us: 1.19x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 30.6 us: 1.08x slower                                  |
| pickle_list          | 4.50 us                                                | 4.24 us: 1.06x faster                                  |
| pickle_pure_python   | 453 us                                                 | 286 us: 1.58x faster                                   |
| unpickle             | 14.3 us                                                | 13.5 us: 1.06x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.08 us: 1.02x slower                                  |
| unpickle_pure_python | 297 us                                                 | 202 us: 1.47x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 160 ms: 1.02x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 106 ms: 1.04x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 75.2 ms: 1.24x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 52.2 ms: 1.43x faster                                  |
| Geometric mean       | (ref)                                                  | 1.15x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.17 ms: 1.71x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.02 ms: 1.04x slower                                  |
| Geometric mean         | (ref)                                                  | 1.28x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.1 ms: 1.44x faster                                  |
| mako            | 14.3 ms                                                | 9.33 ms: 1.53x faster                                  |
| Geometric mean  | (ref)                                                  | 1.49x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220717-linux-x86_64-python-main-3.12.0a1+-c20186c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon               | 8.86 ms                                                | 6.28 ms: 1.41x faster                                  |
| chaos                   | 104 ms                                                 | 66.2 ms: 1.57x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 72.9 ms: 1.61x faster                                  |
| deltablue               | 7.39 ms                                                | 3.21 ms: 2.30x faster                                  |
| django_template         | 46.3 ms                                                | 32.1 ms: 1.44x faster                                  |
| dulwich_log             | 75.5 ms                                                | 60.8 ms: 1.24x faster                                  |
| fannkuch                | 477 ms                                                 | 373 ms: 1.28x faster                                   |
| float                   | 108 ms                                                 | 72.0 ms: 1.50x faster                                  |
| go                      | 226 ms                                                 | 133 ms: 1.71x faster                                   |
| hexiom                  | 9.42 ms                                                | 6.05 ms: 1.56x faster                                  |
| html5lib                | 85.8 ms                                                | 62.8 ms: 1.36x faster                                  |
| json                    | 5.35 ms                                                | 4.61 ms: 1.16x faster                                  |
| json_dumps              | 13.5 ms                                                | 11.9 ms: 1.14x faster                                  |
| json_loads              | 28.9 us                                                | 24.3 us: 1.19x faster                                  |
| logging_format          | 8.92 us                                                | 6.22 us: 1.44x faster                                  |
| logging_silent          | 173 ns                                                 | 91.9 ns: 1.89x faster                                  |
| logging_simple          | 8.06 us                                                | 5.61 us: 1.44x faster                                  |
| mako                    | 14.3 ms                                                | 9.33 ms: 1.53x faster                                  |
| meteor_contest          | 114 ms                                                 | 101 ms: 1.12x faster                                   |
| nbody                   | 136 ms                                                 | 88.8 ms: 1.53x faster                                  |
| nqueens                 | 99.3 ms                                                | 78.8 ms: 1.26x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.7 ms: 1.13x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 30.6 us: 1.08x slower                                  |
| pickle_list             | 4.50 us                                                | 4.24 us: 1.06x faster                                  |
| pickle_pure_python      | 453 us                                                 | 286 us: 1.58x faster                                   |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                   |
| pycparser               | 1.51 sec                                               | 1.05 sec: 1.44x faster                                 |
| pyflate                 | 675 ms                                                 | 401 ms: 1.68x faster                                   |
| python_startup          | 13.9 ms                                                | 8.17 ms: 1.71x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.02 ms: 1.04x slower                                  |
| raytrace                | 461 ms                                                 | 285 ms: 1.62x faster                                   |
| regex_compile           | 174 ms                                                 | 127 ms: 1.36x faster                                   |
| regex_dna               | 214 ms                                                 | 197 ms: 1.09x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.47 ms: 1.08x slower                                  |
| regex_v8                | 25.0 ms                                                | 20.9 ms: 1.19x faster                                  |
| richards                | 71.4 ms                                                | 44.7 ms: 1.60x faster                                  |
| scimark_fft             | 414 ms                                                 | 313 ms: 1.32x faster                                   |
| scimark_lu              | 158 ms                                                 | 105 ms: 1.50x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 65.1 ms: 1.61x faster                                  |
| scimark_sor             | 193 ms                                                 | 117 ms: 1.65x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.04 ms: 1.36x faster                                  |
| spectral_norm           | 148 ms                                                 | 93.4 ms: 1.59x faster                                  |
| sqlite_synth            | 2.90 us                                                | 2.60 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 452 ms: 1.19x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.1 ms: 1.19x faster                                  |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                   |
| sympy_str               | 324 ms                                                 | 278 ms: 1.17x faster                                   |
| telco                   | 6.68 ms                                                | 6.50 ms: 1.03x faster                                  |
| thrift                  | 1.03 ms                                                | 739 us: 1.40x faster                                   |
| tornado_http            | 128 ms                                                 | 91.3 ms: 1.41x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 43.2 ns: 1.38x faster                                  |
| unpickle                | 14.3 us                                                | 13.5 us: 1.06x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.08 us: 1.02x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 202 us: 1.47x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 160 ms: 1.02x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 106 ms: 1.04x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 75.2 ms: 1.24x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 52.2 ms: 1.43x faster                                  |
| Geometric mean          | (ref)                                                  | 1.32x faster                                           |
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
