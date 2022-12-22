Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 244 ms: 1.05x faster                                                   |
| chameleon      | 6.41 ms                                                | 6.31 ms: 1.02x faster                                                  |
| docutils       | 2.60 sec                                               | 2.48 sec: 1.05x faster                                                 |
| html5lib       | 63.2 ms                                                | 59.1 ms: 1.07x faster                                                  |
| tornado_http   | 96.6 ms                                                | 92.8 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.3 ms                                                | 73.1 ms: 1.04x faster                                                  |
| nbody          | 95.0 ms                                                | 93.7 ms: 1.01x faster                                                  |
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                 | 127 ms: 1.07x faster                                                   |
| regex_dna      | 203 ms                                                 | 209 ms: 1.03x slower                                                   |
| regex_effbot   | 3.36 ms                                                | 3.55 ms: 1.06x slower                                                  |
| regex_v8       | 22.3 ms                                                | 21.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.51 ms: 1.33x faster                                                  |
| json_loads           | 26.2 us                                                | 23.8 us: 1.10x faster                                                  |
| pickle               | 9.79 us                                                | 10.4 us: 1.06x slower                                                  |
| pickle_dict          | 31.4 us                                                | 31.3 us: 1.00x faster                                                  |
| pickle_list          | 4.17 us                                                | 3.97 us: 1.05x faster                                                  |
| pickle_pure_python   | 304 us                                                 | 281 us: 1.08x faster                                                   |
| unpickle             | 13.3 us                                                | 13.6 us: 1.02x slower                                                  |
| unpickle_list        | 4.95 us                                                | 5.13 us: 1.04x slower                                                  |
| unpickle_pure_python | 225 us                                                 | 198 us: 1.14x faster                                                   |
| xml_etree_parse      | 158 ms                                                 | 147 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 103 ms                                                 | 102 ms: 1.01x faster                                                   |
| xml_etree_process    | 53.8 ms                                                | 52.8 ms: 1.02x faster                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 8.48 ms: 1.01x slower                                                  |
| python_startup_no_site | 5.96 ms                                                | 6.12 ms: 1.03x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 32.5 ms                                                | 32.1 ms: 1.01x faster                                                  |
| genshi_text     | 22.1 ms                                                | 20.2 ms: 1.10x faster                                                  |
| genshi_xml      | 52.1 ms                                                | 46.6 ms: 1.12x faster                                                  |
| mako            | 9.85 ms                                                | 9.56 ms: 1.03x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2+-cdde29d |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3                    | 257 ms                                                 | 244 ms: 1.05x faster                                                   |
| aiohttp                 | 1.05 ms                                                | 991 us: 1.06x faster                                                   |
| async_tree_io           | 1.31 sec                                               | 1.32 sec: 1.01x slower                                                 |
| chameleon               | 6.41 ms                                                | 6.31 ms: 1.02x faster                                                  |
| chaos                   | 68.6 ms                                                | 65.6 ms: 1.05x faster                                                  |
| bench_thread_pool       | 810 us                                                 | 774 us: 1.05x faster                                                   |
| coroutines              | 26.1 ms                                                | 24.5 ms: 1.07x faster                                                  |
| coverage                | 101 ms                                                 | 102 ms: 1.01x slower                                                   |
| crypto_pyaes            | 73.9 ms                                                | 75.1 ms: 1.02x slower                                                  |
| deepcopy                | 344 us                                                 | 330 us: 1.04x faster                                                   |
| deepcopy_reduce         | 2.97 us                                                | 2.99 us: 1.01x slower                                                  |
| deepcopy_memo           | 36.4 us                                                | 33.8 us: 1.08x faster                                                  |
| deltablue               | 3.64 ms                                                | 3.17 ms: 1.15x faster                                                  |
| django_template         | 32.5 ms                                                | 32.1 ms: 1.01x faster                                                  |
| docutils                | 2.60 sec                                               | 2.48 sec: 1.05x faster                                                 |
| dulwich_log             | 63.9 ms                                                | 61.5 ms: 1.04x faster                                                  |
| fannkuch                | 388 ms                                                 | 373 ms: 1.04x faster                                                   |
| float                   | 76.3 ms                                                | 73.1 ms: 1.04x faster                                                  |
| generators              | 72.2 ms                                                | 77.7 ms: 1.08x slower                                                  |
| genshi_text             | 22.1 ms                                                | 20.2 ms: 1.10x faster                                                  |
| genshi_xml              | 52.1 ms                                                | 46.6 ms: 1.12x faster                                                  |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                                   |
| gunicorn                | 1.12 ms                                                | 1.07 ms: 1.05x faster                                                  |
| hexiom                  | 6.35 ms                                                | 6.18 ms: 1.03x faster                                                  |
| html5lib                | 63.2 ms                                                | 59.1 ms: 1.07x faster                                                  |
| json                    | 4.95 ms                                                | 4.61 ms: 1.07x faster                                                  |
| json_dumps              | 12.7 ms                                                | 9.51 ms: 1.33x faster                                                  |
| json_loads              | 26.2 us                                                | 23.8 us: 1.10x faster                                                  |
| logging_format          | 6.62 us                                                | 6.29 us: 1.05x faster                                                  |
| logging_silent          | 98.5 ns                                                | 94.1 ns: 1.05x faster                                                  |
| logging_simple          | 6.06 us                                                | 5.62 us: 1.08x faster                                                  |
| mako                    | 9.85 ms                                                | 9.56 ms: 1.03x faster                                                  |
| mdp                     | 2.62 sec                                               | 2.69 sec: 1.03x slower                                                 |
| meteor_contest          | 105 ms                                                 | 102 ms: 1.03x faster                                                   |
| mypy                    | 669 ms                                                 | 798 ms: 1.19x slower                                                   |
| nbody                   | 95.0 ms                                                | 93.7 ms: 1.01x faster                                                  |
| nqueens                 | 85.0 ms                                                | 82.0 ms: 1.04x faster                                                  |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                  |
| pickle                  | 9.79 us                                                | 10.4 us: 1.06x slower                                                  |
| pickle_dict             | 31.4 us                                                | 31.3 us: 1.00x faster                                                  |
| pickle_list             | 4.17 us                                                | 3.97 us: 1.05x faster                                                  |
| pickle_pure_python      | 304 us                                                 | 281 us: 1.08x faster                                                   |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                                   |
| pprint_safe_repr        | 691 ms                                                 | 676 ms: 1.02x faster                                                   |
| pprint_pformat          | 1.44 sec                                               | 1.39 sec: 1.04x faster                                                 |
| pycparser               | 1.17 sec                                               | 1.07 sec: 1.10x faster                                                 |
| pyflate                 | 417 ms                                                 | 397 ms: 1.05x faster                                                   |
| python_startup          | 8.36 ms                                                | 8.48 ms: 1.01x slower                                                  |
| python_startup_no_site  | 5.96 ms                                                | 6.12 ms: 1.03x slower                                                  |
| raytrace                | 290 ms                                                 | 280 ms: 1.04x faster                                                   |
| regex_compile           | 136 ms                                                 | 127 ms: 1.07x faster                                                   |
| regex_dna               | 203 ms                                                 | 209 ms: 1.03x slower                                                   |
| regex_effbot            | 3.36 ms                                                | 3.55 ms: 1.06x slower                                                  |
| regex_v8                | 22.3 ms                                                | 21.0 ms: 1.06x faster                                                  |
| richards                | 46.2 ms                                                | 41.3 ms: 1.12x faster                                                  |
| scimark_fft             | 329 ms                                                 | 307 ms: 1.07x faster                                                   |
| scimark_lu              | 107 ms                                                 | 106 ms: 1.01x faster                                                   |
| scimark_monte_carlo     | 68.3 ms                                                | 65.0 ms: 1.05x faster                                                  |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.08 ms: 1.08x faster                                                  |
| spectral_norm           | 99.9 ms                                                | 95.6 ms: 1.05x faster                                                  |
| sqlglot_parse           | 1.37 ms                                                | 1.32 ms: 1.03x faster                                                  |
| sqlglot_transpile       | 1.66 ms                                                | 1.61 ms: 1.03x faster                                                  |
| sqlglot_optimize        | 53.0 ms                                                | 50.2 ms: 1.06x faster                                                  |
| sqlglot_normalize       | 108 ms                                                 | 104 ms: 1.04x faster                                                   |
| sqlite_synth            | 2.49 us                                                | 2.59 us: 1.04x slower                                                  |
| sympy_expand            | 472 ms                                                 | 454 ms: 1.04x faster                                                   |
| sympy_integrate         | 20.9 ms                                                | 20.3 ms: 1.03x faster                                                  |
| sympy_sum               | 166 ms                                                 | 163 ms: 1.02x faster                                                   |
| sympy_str               | 287 ms                                                 | 280 ms: 1.03x faster                                                   |
| telco                   | 6.62 ms                                                | 6.44 ms: 1.03x faster                                                  |
| thrift                  | 752 us                                                 | 748 us: 1.01x faster                                                   |
| tornado_http            | 96.6 ms                                                | 92.8 ms: 1.04x faster                                                  |
| unpack_sequence         | 43.4 ns                                                | 45.1 ns: 1.04x slower                                                  |
| unpickle                | 13.3 us                                                | 13.6 us: 1.02x slower                                                  |
| unpickle_list           | 4.95 us                                                | 5.13 us: 1.04x slower                                                  |
| unpickle_pure_python    | 225 us                                                 | 198 us: 1.14x faster                                                   |
| xml_etree_parse         | 158 ms                                                 | 147 ms: 1.08x faster                                                   |
| xml_etree_iterparse     | 103 ms                                                 | 102 ms: 1.01x faster                                                   |
| xml_etree_process       | 53.8 ms                                                | 52.8 ms: 1.02x faster                                                  |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (6): async_generators, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization, bench_mp_pool, xml_etree_generate
Ignored benchmarks (4) of ../ideas/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
