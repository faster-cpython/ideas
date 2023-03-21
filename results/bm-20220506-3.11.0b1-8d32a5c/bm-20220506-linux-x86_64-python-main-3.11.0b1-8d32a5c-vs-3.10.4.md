
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8d32a5c
- commit date: 2022-05-06
- overall geometric mean: 1.29x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 332 ms                                                 | 256 ms: 1.30x faster                                  |
| chameleon      | 8.86 ms                                                | 6.57 ms: 1.35x faster                                 |
| html5lib       | 85.8 ms                                                | 60.1 ms: 1.43x faster                                 |
| tornado_http   | 128 ms                                                 | 94.6 ms: 1.36x faster                                 |
| Geometric mean | (ref)                                                  | 1.36x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 108 ms                                                 | 72.5 ms: 1.48x faster                                 |
| nbody          | 136 ms                                                 | 93.1 ms: 1.46x faster                                 |
| pidigits       | 190 ms                                                 | 190 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                  | 1.30x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 135 ms: 1.29x faster                                  |
| regex_v8       | 25.0 ms                                                | 21.6 ms: 1.16x faster                                 |
| regex_effbot   | 3.21 ms                                                | 2.93 ms: 1.09x faster                                 |
| regex_dna      | 214 ms                                                 | 204 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.14x faster                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_pure_python   | 453 us                                                 | 305 us: 1.49x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.6 ms: 1.39x faster                                 |
| unpickle_pure_python | 297 us                                                 | 229 us: 1.30x faster                                  |
| xml_etree_generate   | 93.3 ms                                                | 76.5 ms: 1.22x faster                                 |
| json_loads           | 28.9 us                                                | 25.4 us: 1.14x faster                                 |
| pickle_dict          | 28.3 us                                                | 25.6 us: 1.11x faster                                 |
| json_dumps           | 13.5 ms                                                | 12.4 ms: 1.09x faster                                 |
| unpickle             | 14.3 us                                                | 13.4 us: 1.07x faster                                 |
| pickle               | 10.1 us                                                | 9.56 us: 1.06x faster                                 |
| xml_etree_iterparse  | 110 ms                                                 | 104 ms: 1.06x faster                                  |
| pickle_list          | 4.50 us                                                | 4.26 us: 1.06x faster                                 |
| xml_etree_parse      | 163 ms                                                 | 157 ms: 1.04x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.05 us: 1.01x slower                                 |
| Geometric mean       | (ref)                                                  | 1.15x faster                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.25 ms: 1.69x faster                                 |
| python_startup_no_site | 5.76 ms                                                | 6.16 ms: 1.07x slower                                 |
| Geometric mean         | (ref)                                                  | 1.26x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| mako            | 14.3 ms                                                | 9.88 ms: 1.44x faster                                 |
| django_template | 46.3 ms                                                | 32.8 ms: 1.41x faster                                 |
| Geometric mean  | (ref)                                                  | 1.43x faster                                          |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20220506-linux-x86_64-python-main-3.11.0b1-8d32a5c |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| deltablue               | 7.39 ms                                                | 3.61 ms: 2.05x faster                                 |
| logging_silent          | 173 ns                                                 | 98.2 ns: 1.76x faster                                 |
| python_startup          | 13.9 ms                                                | 8.25 ms: 1.69x faster                                 |
| scimark_sor             | 193 ms                                                 | 115 ms: 1.69x faster                                  |
| go                      | 226 ms                                                 | 136 ms: 1.66x faster                                  |
| pyflate                 | 675 ms                                                 | 411 ms: 1.64x faster                                  |
| crypto_pyaes            | 118 ms                                                 | 74.3 ms: 1.58x faster                                 |
| scimark_monte_carlo     | 105 ms                                                 | 66.5 ms: 1.58x faster                                 |
| raytrace                | 461 ms                                                 | 294 ms: 1.57x faster                                  |
| richards                | 71.4 ms                                                | 46.4 ms: 1.54x faster                                 |
| chaos                   | 104 ms                                                 | 68.6 ms: 1.52x faster                                 |
| spectral_norm           | 148 ms                                                 | 97.6 ms: 1.52x faster                                 |
| hexiom                  | 9.42 ms                                                | 6.29 ms: 1.50x faster                                 |
| pickle_pure_python      | 453 us                                                 | 305 us: 1.49x faster                                  |
| float                   | 108 ms                                                 | 72.5 ms: 1.48x faster                                 |
| nbody                   | 136 ms                                                 | 93.1 ms: 1.46x faster                                 |
| scimark_lu              | 158 ms                                                 | 109 ms: 1.45x faster                                  |
| mako                    | 14.3 ms                                                | 9.88 ms: 1.44x faster                                 |
| html5lib                | 85.8 ms                                                | 60.1 ms: 1.43x faster                                 |
| django_template         | 46.3 ms                                                | 32.8 ms: 1.41x faster                                 |
| thrift                  | 1.03 ms                                                | 741 us: 1.39x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.6 ms: 1.39x faster                                 |
| logging_format          | 8.92 us                                                | 6.44 us: 1.39x faster                                 |
| logging_simple          | 8.06 us                                                | 5.89 us: 1.37x faster                                 |
| tornado_http            | 128 ms                                                 | 94.6 ms: 1.36x faster                                 |
| chameleon               | 8.86 ms                                                | 6.57 ms: 1.35x faster                                 |
| unpack_sequence         | 59.5 ns                                                | 44.3 ns: 1.34x faster                                 |
| 2to3                    | 332 ms                                                 | 256 ms: 1.30x faster                                  |
| unpickle_pure_python    | 297 us                                                 | 229 us: 1.30x faster                                  |
| regex_compile           | 174 ms                                                 | 135 ms: 1.29x faster                                  |
| pycparser               | 1.51 sec                                               | 1.18 sec: 1.28x faster                                |
| scimark_fft             | 414 ms                                                 | 325 ms: 1.27x faster                                  |
| fannkuch                | 477 ms                                                 | 385 ms: 1.24x faster                                  |
| xml_etree_generate      | 93.3 ms                                                | 76.5 ms: 1.22x faster                                 |
| dulwich_log             | 75.5 ms                                                | 62.8 ms: 1.20x faster                                 |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.57 ms: 1.20x faster                                 |
| nqueens                 | 99.3 ms                                                | 84.7 ms: 1.17x faster                                 |
| sympy_integrate         | 23.9 ms                                                | 20.5 ms: 1.17x faster                                 |
| regex_v8                | 25.0 ms                                                | 21.6 ms: 1.16x faster                                 |
| sqlite_synth            | 2.90 us                                                | 2.53 us: 1.15x faster                                 |
| sympy_expand            | 537 ms                                                 | 468 ms: 1.15x faster                                  |
| sympy_str               | 324 ms                                                 | 284 ms: 1.14x faster                                  |
| sympy_sum               | 183 ms                                                 | 161 ms: 1.14x faster                                  |
| json_loads              | 28.9 us                                                | 25.4 us: 1.14x faster                                 |
| pathlib                 | 20.0 ms                                                | 17.9 ms: 1.12x faster                                 |
| pickle_dict             | 28.3 us                                                | 25.6 us: 1.11x faster                                 |
| regex_effbot            | 3.21 ms                                                | 2.93 ms: 1.09x faster                                 |
| json_dumps              | 13.5 ms                                                | 12.4 ms: 1.09x faster                                 |
| json                    | 5.35 ms                                                | 4.91 ms: 1.09x faster                                 |
| meteor_contest          | 114 ms                                                 | 105 ms: 1.09x faster                                  |
| unpickle                | 14.3 us                                                | 13.4 us: 1.07x faster                                 |
| pickle                  | 10.1 us                                                | 9.56 us: 1.06x faster                                 |
| xml_etree_iterparse     | 110 ms                                                 | 104 ms: 1.06x faster                                  |
| pickle_list             | 4.50 us                                                | 4.26 us: 1.06x faster                                 |
| regex_dna               | 214 ms                                                 | 204 ms: 1.05x faster                                  |
| xml_etree_parse         | 163 ms                                                 | 157 ms: 1.04x faster                                  |
| pidigits                | 190 ms                                                 | 190 ms: 1.00x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.05 us: 1.01x slower                                 |
| telco                   | 6.68 ms                                                | 6.84 ms: 1.02x slower                                 |
| python_startup_no_site  | 5.76 ms                                                | 6.16 ms: 1.07x slower                                 |
| Geometric mean          | (ref)                                                  | 1.29x faster                                          |
Ignored benchmarks (30) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
