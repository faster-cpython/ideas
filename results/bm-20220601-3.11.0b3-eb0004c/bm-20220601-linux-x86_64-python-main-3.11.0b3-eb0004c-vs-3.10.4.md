Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 256 ms: 1.30x faster                                  |
| chameleon      | 8.86 ms                                                | 6.67 ms: 1.33x faster                                 |
| html5lib       | 85.8 ms                                                | 62.6 ms: 1.37x faster                                 |
| tornado_http   | 128 ms                                                 | 93.8 ms: 1.37x faster                                 |
| Geometric mean | (ref)                                                  | 1.34x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 72.9 ms: 1.48x faster                                 |
| nbody          | 136 ms                                                 | 90.6 ms: 1.50x faster                                 |
| pidigits       | 190 ms                                                 | 194 ms: 1.02x slower                                  |
| Geometric mean | (ref)                                                  | 1.30x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 135 ms: 1.29x faster                                  |
| regex_dna      | 214 ms                                                 | 192 ms: 1.12x faster                                  |
| regex_effbot   | 3.21 ms                                                | 2.92 ms: 1.10x faster                                 |
| regex_v8       | 25.0 ms                                                | 21.2 ms: 1.18x faster                                 |
| Geometric mean | (ref)                                                  | 1.17x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 12.5 ms: 1.08x faster                                 |
| json_loads           | 28.9 us                                                | 24.4 us: 1.18x faster                                 |
| pickle               | 10.1 us                                                | 9.55 us: 1.06x faster                                 |
| pickle_dict          | 28.3 us                                                | 25.6 us: 1.11x faster                                 |
| pickle_list          | 4.50 us                                                | 4.33 us: 1.04x faster                                 |
| pickle_pure_python   | 453 us                                                 | 302 us: 1.50x faster                                  |
| unpickle             | 14.3 us                                                | 13.3 us: 1.07x faster                                 |
| unpickle_list        | 4.99 us                                                | 4.89 us: 1.02x faster                                 |
| unpickle_pure_python | 297 us                                                 | 228 us: 1.30x faster                                  |
| xml_etree_parse      | 163 ms                                                 | 156 ms: 1.05x faster                                  |
| xml_etree_iterparse  | 110 ms                                                 | 105 ms: 1.06x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 76.3 ms: 1.22x faster                                 |
| xml_etree_process    | 74.5 ms                                                | 53.8 ms: 1.38x faster                                 |
| Geometric mean       | (ref)                                                  | 1.15x faster                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.33 ms: 1.67x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 6.17 ms: 1.07x slower                                 |
| Geometric mean         | (ref)                                                  | 1.25x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.9 ms: 1.41x faster                                 |
| mako            | 14.3 ms                                                | 9.82 ms: 1.45x faster                                 |
| Geometric mean  | (ref)                                                  | 1.43x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220601-linux-x86_64-python-main-3.11.0b3-eb0004c |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 256 ms: 1.30x faster                                  |
| chameleon               | 8.86 ms                                                | 6.67 ms: 1.33x faster                                 |
| chaos                   | 104 ms                                                 | 66.9 ms: 1.56x faster                                 |
| crypto_pyaes            | 118 ms                                                 | 73.1 ms: 1.61x faster                                 |
| deltablue               | 7.39 ms                                                | 3.62 ms: 2.04x faster                                 |
| django_template         | 46.3 ms                                                | 32.9 ms: 1.41x faster                                 |
| dulwich_log             | 75.5 ms                                                | 63.1 ms: 1.20x faster                                 |
| fannkuch                | 477 ms                                                 | 372 ms: 1.28x faster                                  |
| float                   | 108 ms                                                 | 72.9 ms: 1.48x faster                                 |
| go                      | 226 ms                                                 | 137 ms: 1.66x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.32 ms: 1.49x faster                                 |
| html5lib                | 85.8 ms                                                | 62.6 ms: 1.37x faster                                 |
| json                    | 5.35 ms                                                | 4.75 ms: 1.13x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.5 ms: 1.08x faster                                 |
| json_loads              | 28.9 us                                                | 24.4 us: 1.18x faster                                 |
| logging_format          | 8.92 us                                                | 6.44 us: 1.39x faster                                 |
| logging_silent          | 173 ns                                                 | 101 ns: 1.71x faster                                  |
| logging_simple          | 8.06 us                                                | 5.95 us: 1.35x faster                                 |
| mako                    | 14.3 ms                                                | 9.82 ms: 1.45x faster                                 |
| meteor_contest          | 114 ms                                                 | 104 ms: 1.10x faster                                  |
| nbody                   | 136 ms                                                 | 90.6 ms: 1.50x faster                                 |
| nqueens                 | 99.3 ms                                                | 80.7 ms: 1.23x faster                                 |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                 |
| pickle                  | 10.1 us                                                | 9.55 us: 1.06x faster                                 |
| pickle_dict             | 28.3 us                                                | 25.6 us: 1.11x faster                                 |
| pickle_list             | 4.50 us                                                | 4.33 us: 1.04x faster                                 |
| pickle_pure_python      | 453 us                                                 | 302 us: 1.50x faster                                  |
| pidigits                | 190 ms                                                 | 194 ms: 1.02x slower                                  |
| pycparser               | 1.51 sec                                               | 1.10 sec: 1.37x faster                                |
| pyflate                 | 675 ms                                                 | 411 ms: 1.64x faster                                  |
| python_startup          | 13.9 ms                                                | 8.33 ms: 1.67x faster                                 |
| python_startup_no_site  | 5.76 ms                                                | 6.17 ms: 1.07x slower                                 |
| raytrace                | 461 ms                                                 | 292 ms: 1.58x faster                                  |
| regex_compile           | 174 ms                                                 | 135 ms: 1.29x faster                                  |
| regex_dna               | 214 ms                                                 | 192 ms: 1.12x faster                                  |
| regex_effbot            | 3.21 ms                                                | 2.92 ms: 1.10x faster                                 |
| regex_v8                | 25.0 ms                                                | 21.2 ms: 1.18x faster                                 |
| richards                | 71.4 ms                                                | 46.5 ms: 1.53x faster                                 |
| scimark_fft             | 414 ms                                                 | 317 ms: 1.30x faster                                  |
| scimark_lu              | 158 ms                                                 | 107 ms: 1.49x faster                                  |
| scimark_monte_carlo     | 105 ms                                                 | 66.0 ms: 1.59x faster                                 |
| scimark_sor             | 193 ms                                                 | 115 ms: 1.68x faster                                  |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.54 ms: 1.21x faster                                 |
| spectral_norm           | 148 ms                                                 | 97.6 ms: 1.52x faster                                 |
| sqlite_synth            | 2.90 us                                                | 2.49 us: 1.17x faster                                 |
| sympy_expand            | 537 ms                                                 | 467 ms: 1.15x faster                                  |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                 |
| sympy_sum               | 183 ms                                                 | 159 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 284 ms: 1.14x faster                                  |
| telco                   | 6.68 ms                                                | 6.49 ms: 1.03x faster                                 |
| thrift                  | 1.03 ms                                                | 759 us: 1.36x faster                                  |
| tornado_http            | 128 ms                                                 | 93.8 ms: 1.37x faster                                 |
| unpack_sequence         | 59.5 ns                                                | 43.4 ns: 1.37x faster                                 |
| unpickle                | 14.3 us                                                | 13.3 us: 1.07x faster                                 |
| unpickle_list           | 4.99 us                                                | 4.89 us: 1.02x faster                                 |
| unpickle_pure_python    | 297 us                                                 | 228 us: 1.30x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 156 ms: 1.05x faster                                  |
| xml_etree_iterparse     | 110 ms                                                 | 105 ms: 1.06x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 76.3 ms: 1.22x faster                                 |
| xml_etree_process       | 74.5 ms                                                | 53.8 ms: 1.38x faster                                 |
| Geometric mean          | (ref)                                                  | 1.30x faster                                          |
Ignored benchmarks (30) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
