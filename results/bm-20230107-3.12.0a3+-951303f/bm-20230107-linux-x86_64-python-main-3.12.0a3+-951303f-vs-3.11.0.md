
# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 951303f
- commit date: 2023-01-07
- overall geometric mean: 1.02x faster

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 255 ms: 1.01x faster                                   |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                 |
| html5lib       | 63.2 ms                                                | 59.7 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 72.8 ms: 1.05x faster                                  |
| nbody          | 95.0 ms                                                | 96.7 ms: 1.02x slower                                  |
| pidigits       | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_dna      | 203 ms                                                 | 189 ms: 1.08x faster                                   |
| regex_effbot   | 3.36 ms                                                | 3.17 ms: 1.06x faster                                  |
| regex_v8       | 22.3 ms                                                | 20.8 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.51 ms: 1.33x faster                                  |
| json_loads           | 26.2 us                                                | 26.1 us: 1.01x faster                                  |
| pickle               | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_list          | 4.17 us                                                | 4.14 us: 1.01x faster                                  |
| pickle_pure_python   | 304 us                                                 | 284 us: 1.07x faster                                   |
| unpickle_list        | 4.95 us                                                | 5.01 us: 1.01x slower                                  |
| unpickle_pure_python | 225 us                                                 | 210 us: 1.07x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 150 ms: 1.06x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 104 ms: 1.02x slower                                   |
| xml_etree_generate   | 76.2 ms                                                | 78.2 ms: 1.03x slower                                  |
| xml_etree_process    | 53.8 ms                                                | 53.4 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (2): pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.51 ms: 1.02x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.09 ms: 1.02x slower                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.9 ms: 1.02x slower                                  |
| genshi_text     | 22.1 ms                                                | 20.7 ms: 1.07x faster                                  |
| genshi_xml      | 52.1 ms                                                | 47.4 ms: 1.10x faster                                  |
| mako            | 9.85 ms                                                | 9.54 ms: 1.03x faster                                  |
| Geometric mean  | (ref)                                                  | 1.04x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 255 ms: 1.01x faster                                   |
| async_generators        | 359 ms                                                 | 356 ms: 1.01x faster                                   |
| async_tree_none         | 529 ms                                                 | 536 ms: 1.01x slower                                   |
| async_tree_cpu_io_mixed | 752 ms                                                 | 757 ms: 1.01x slower                                   |
| async_tree_io           | 1.31 sec                                               | 1.33 sec: 1.02x slower                                 |
| async_tree_memoization  | 625 ms                                                 | 672 ms: 1.07x slower                                   |
| chaos                   | 68.6 ms                                                | 70.2 ms: 1.02x slower                                  |
| bench_thread_pool       | 810 us                                                 | 781 us: 1.04x faster                                   |
| coroutines              | 26.1 ms                                                | 25.2 ms: 1.03x faster                                  |
| coverage                | 101 ms                                                 | 99.3 ms: 1.01x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 77.2 ms: 1.05x slower                                  |
| deepcopy                | 344 us                                                 | 330 us: 1.04x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.90 us: 1.02x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 33.6 us: 1.08x faster                                  |
| deltablue               | 3.64 ms                                                | 3.25 ms: 1.12x faster                                  |
| django_template         | 32.5 ms                                                | 32.9 ms: 1.02x slower                                  |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.9 ms: 1.02x faster                                  |
| fannkuch                | 388 ms                                                 | 376 ms: 1.03x faster                                   |
| float                   | 76.3 ms                                                | 72.8 ms: 1.05x faster                                  |
| generators              | 72.2 ms                                                | 76.2 ms: 1.06x slower                                  |
| genshi_text             | 22.1 ms                                                | 20.7 ms: 1.07x faster                                  |
| genshi_xml              | 52.1 ms                                                | 47.4 ms: 1.10x faster                                  |
| go                      | 143 ms                                                 | 136 ms: 1.05x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.06 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 59.7 ms: 1.06x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.51 ms: 1.33x faster                                  |
| json_loads              | 26.2 us                                                | 26.1 us: 1.01x faster                                  |
| logging_format          | 6.62 us                                                | 6.31 us: 1.05x faster                                  |
| logging_silent          | 98.5 ns                                                | 94.1 ns: 1.05x faster                                  |
| logging_simple          | 6.06 us                                                | 5.77 us: 1.05x faster                                  |
| mako                    | 9.85 ms                                                | 9.54 ms: 1.03x faster                                  |
| meteor_contest          | 105 ms                                                 | 105 ms: 1.01x slower                                   |
| mypy                    | 669 ms                                                 | 815 ms: 1.22x slower                                   |
| nbody                   | 95.0 ms                                                | 96.7 ms: 1.02x slower                                  |
| nqueens                 | 85.0 ms                                                | 81.0 ms: 1.05x faster                                  |
| pathlib                 | 18.2 ms                                                | 17.9 ms: 1.02x faster                                  |
| pickle                  | 9.79 us                                                | 10.2 us: 1.04x slower                                  |
| pickle_list             | 4.17 us                                                | 4.14 us: 1.01x faster                                  |
| pickle_pure_python      | 304 us                                                 | 284 us: 1.07x faster                                   |
| pidigits                | 199 ms                                                 | 190 ms: 1.05x faster                                   |
| pprint_safe_repr        | 691 ms                                                 | 681 ms: 1.01x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.40 sec: 1.03x faster                                 |
| pycparser               | 1.17 sec                                               | 1.13 sec: 1.04x faster                                 |
| pyflate                 | 417 ms                                                 | 402 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.51 ms: 1.02x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.09 ms: 1.02x slower                                  |
| raytrace                | 290 ms                                                 | 282 ms: 1.03x faster                                   |
| regex_compile           | 136 ms                                                 | 128 ms: 1.06x faster                                   |
| regex_dna               | 203 ms                                                 | 189 ms: 1.08x faster                                   |
| regex_effbot            | 3.36 ms                                                | 3.17 ms: 1.06x faster                                  |
| regex_v8                | 22.3 ms                                                | 20.8 ms: 1.07x faster                                  |
| richards                | 46.2 ms                                                | 42.3 ms: 1.09x faster                                  |
| scimark_fft             | 329 ms                                                 | 325 ms: 1.01x faster                                   |
| scimark_lu              | 107 ms                                                 | 109 ms: 1.01x slower                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.6 ms: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 108 ms: 1.07x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.11 ms: 1.07x faster                                  |
| spectral_norm           | 99.9 ms                                                | 98.6 ms: 1.01x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.40 ms: 1.02x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.69 ms: 1.02x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 51.7 ms: 1.03x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 107 ms: 1.01x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.60 us: 1.04x slower                                  |
| sympy_expand            | 472 ms                                                 | 462 ms: 1.02x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.4 ms: 1.02x faster                                  |
| sympy_str               | 287 ms                                                 | 285 ms: 1.01x faster                                   |
| telco                   | 6.62 ms                                                | 6.36 ms: 1.04x faster                                  |
| thrift                  | 752 us                                                 | 757 us: 1.01x slower                                   |
| unpack_sequence         | 43.4 ns                                                | 42.4 ns: 1.02x faster                                  |
| unpickle_list           | 4.95 us                                                | 5.01 us: 1.01x slower                                  |
| unpickle_pure_python    | 225 us                                                 | 210 us: 1.07x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 150 ms: 1.06x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 104 ms: 1.02x slower                                   |
| xml_etree_generate      | 76.2 ms                                                | 78.2 ms: 1.03x slower                                  |
| xml_etree_process       | 53.8 ms                                                | 53.4 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (7): chameleon, bench_mp_pool, json, mdp, pickle_dict, sympy_sum, unpickle
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20230107-3.12.0a3+-951303f/bm-20230107-linux-x86_64-python-main-3.12.0a3+-951303f.json: djangocms
