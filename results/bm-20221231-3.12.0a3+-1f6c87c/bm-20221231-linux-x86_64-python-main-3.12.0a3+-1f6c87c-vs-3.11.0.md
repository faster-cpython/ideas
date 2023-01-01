Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| docutils       | 2.60 sec                                               | 2.50 sec: 1.04x faster                                 |
| html5lib       | 63.2 ms                                                | 60.3 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 76.3 ms                                                | 71.2 ms: 1.07x faster                                  |
| nbody          | 95.0 ms                                                | 94.2 ms: 1.01x faster                                  |
| pidigits       | 199 ms                                                 | 197 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 131 ms: 1.04x faster                                   |
| regex_dna      | 203 ms                                                 | 215 ms: 1.06x slower                                   |
| regex_effbot   | 3.36 ms                                                | 3.64 ms: 1.09x slower                                  |
| regex_v8       | 22.3 ms                                                | 22.2 ms: 1.00x faster                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.33 ms: 1.36x faster                                  |
| json_loads           | 26.2 us                                                | 23.8 us: 1.10x faster                                  |
| pickle               | 9.79 us                                                | 9.96 us: 1.02x slower                                  |
| pickle_dict          | 31.4 us                                                | 30.1 us: 1.04x faster                                  |
| pickle_list          | 4.17 us                                                | 4.00 us: 1.04x faster                                  |
| pickle_pure_python   | 304 us                                                 | 282 us: 1.08x faster                                   |
| unpickle             | 13.3 us                                                | 12.7 us: 1.05x faster                                  |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.15x faster                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.07x faster                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.00x faster                                   |
| xml_etree_process    | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean       | (ref)                                                  | 1.06x faster                                           |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.45 ms: 1.01x slower                                  |
| python_startup_no_site | 5.96 ms                                                | 6.05 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                  | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.7 ms: 1.01x slower                                  |
| genshi_text     | 22.1 ms                                                | 20.7 ms: 1.07x faster                                  |
| genshi_xml      | 52.1 ms                                                | 46.6 ms: 1.12x faster                                  |
| mako            | 9.85 ms                                                | 9.64 ms: 1.02x faster                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 252 ms: 1.02x faster                                   |
| async_generators        | 359 ms                                                 | 352 ms: 1.02x faster                                   |
| async_tree_none         | 529 ms                                                 | 524 ms: 1.01x faster                                   |
| chaos                   | 68.6 ms                                                | 68.0 ms: 1.01x faster                                  |
| bench_thread_pool       | 810 us                                                 | 777 us: 1.04x faster                                   |
| coroutines              | 26.1 ms                                                | 25.5 ms: 1.02x faster                                  |
| crypto_pyaes            | 73.9 ms                                                | 74.4 ms: 1.01x slower                                  |
| deepcopy                | 344 us                                                 | 338 us: 1.02x faster                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                  |
| deepcopy_memo           | 36.4 us                                                | 34.1 us: 1.07x faster                                  |
| deltablue               | 3.64 ms                                                | 3.17 ms: 1.15x faster                                  |
| django_template         | 32.5 ms                                                | 32.7 ms: 1.01x slower                                  |
| docutils                | 2.60 sec                                               | 2.50 sec: 1.04x faster                                 |
| dulwich_log             | 63.9 ms                                                | 62.4 ms: 1.02x faster                                  |
| fannkuch                | 388 ms                                                 | 377 ms: 1.03x faster                                   |
| float                   | 76.3 ms                                                | 71.2 ms: 1.07x faster                                  |
| generators              | 72.2 ms                                                | 76.4 ms: 1.06x slower                                  |
| genshi_text             | 22.1 ms                                                | 20.7 ms: 1.07x faster                                  |
| genshi_xml              | 52.1 ms                                                | 46.6 ms: 1.12x faster                                  |
| go                      | 143 ms                                                 | 137 ms: 1.04x faster                                   |
| hexiom                  | 6.35 ms                                                | 6.04 ms: 1.05x faster                                  |
| html5lib                | 63.2 ms                                                | 60.3 ms: 1.05x faster                                  |
| json                    | 4.95 ms                                                | 4.64 ms: 1.07x faster                                  |
| json_dumps              | 12.7 ms                                                | 9.33 ms: 1.36x faster                                  |
| json_loads              | 26.2 us                                                | 23.8 us: 1.10x faster                                  |
| logging_format          | 6.62 us                                                | 6.44 us: 1.03x faster                                  |
| logging_silent          | 98.5 ns                                                | 91.4 ns: 1.08x faster                                  |
| logging_simple          | 6.06 us                                                | 5.72 us: 1.06x faster                                  |
| mako                    | 9.85 ms                                                | 9.64 ms: 1.02x faster                                  |
| mdp                     | 2.62 sec                                               | 2.64 sec: 1.01x slower                                 |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.02x faster                                   |
| mypy                    | 669 ms                                                 | 811 ms: 1.21x slower                                   |
| nbody                   | 95.0 ms                                                | 94.2 ms: 1.01x faster                                  |
| nqueens                 | 85.0 ms                                                | 78.9 ms: 1.08x faster                                  |
| pickle                  | 9.79 us                                                | 9.96 us: 1.02x slower                                  |
| pickle_dict             | 31.4 us                                                | 30.1 us: 1.04x faster                                  |
| pickle_list             | 4.17 us                                                | 4.00 us: 1.04x faster                                  |
| pickle_pure_python      | 304 us                                                 | 282 us: 1.08x faster                                   |
| pidigits                | 199 ms                                                 | 197 ms: 1.01x faster                                   |
| pprint_pformat          | 1.44 sec                                               | 1.42 sec: 1.02x faster                                 |
| pycparser               | 1.17 sec                                               | 1.14 sec: 1.03x faster                                 |
| pyflate                 | 417 ms                                                 | 402 ms: 1.04x faster                                   |
| python_startup          | 8.36 ms                                                | 8.45 ms: 1.01x slower                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.05 ms: 1.01x slower                                  |
| raytrace                | 290 ms                                                 | 281 ms: 1.04x faster                                   |
| regex_compile           | 136 ms                                                 | 131 ms: 1.04x faster                                   |
| regex_dna               | 203 ms                                                 | 215 ms: 1.06x slower                                   |
| regex_effbot            | 3.36 ms                                                | 3.64 ms: 1.09x slower                                  |
| regex_v8                | 22.3 ms                                                | 22.2 ms: 1.00x faster                                  |
| richards                | 46.2 ms                                                | 41.5 ms: 1.11x faster                                  |
| scimark_fft             | 329 ms                                                 | 314 ms: 1.05x faster                                   |
| scimark_lu              | 107 ms                                                 | 108 ms: 1.01x slower                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 64.5 ms: 1.06x faster                                  |
| scimark_sor             | 115 ms                                                 | 104 ms: 1.11x faster                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.30 ms: 1.02x faster                                  |
| spectral_norm           | 99.9 ms                                                | 94.1 ms: 1.06x faster                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.39 ms: 1.02x slower                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.69 ms: 1.02x slower                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.7 ms: 1.04x faster                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.03x faster                                   |
| sqlite_synth            | 2.49 us                                                | 2.62 us: 1.05x slower                                  |
| sympy_expand            | 472 ms                                                 | 453 ms: 1.04x faster                                   |
| sympy_integrate         | 20.9 ms                                                | 20.1 ms: 1.04x faster                                  |
| sympy_sum               | 166 ms                                                 | 162 ms: 1.02x faster                                   |
| sympy_str               | 287 ms                                                 | 281 ms: 1.02x faster                                   |
| telco                   | 6.62 ms                                                | 6.19 ms: 1.07x faster                                  |
| unpack_sequence         | 43.4 ns                                                | 42.0 ns: 1.03x faster                                  |
| unpickle                | 13.3 us                                                | 12.7 us: 1.05x faster                                  |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.15x faster                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.07x faster                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.00x faster                                   |
| xml_etree_process       | 53.8 ms                                                | 53.3 ms: 1.01x faster                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (11): async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, chameleon, bench_mp_pool, coverage, pathlib, pprint_safe_repr, thrift, unpickle_list, xml_etree_generate
Ignored benchmarks (7) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (1) of public/results/bm-20221231-3.12.0a3+-1f6c87c/bm-20221231-linux-x86_64-python-main-3.12.0a3+-1f6c87c.json: djangocms
