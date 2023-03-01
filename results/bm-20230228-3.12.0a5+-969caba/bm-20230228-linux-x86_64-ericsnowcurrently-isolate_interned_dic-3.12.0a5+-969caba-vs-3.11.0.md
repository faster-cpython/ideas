
# Results vs. 3.11.0

- fork: ericsnowcurrently
- ref: isolate_interned_dic
- machine: linux-x86_64
- commit hash: 969caba
- commit date: 2023-02-28
- overall geometric mean: 1.03x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                 | 250 ms: 1.03x faster                                                              |
| chameleon      | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                             |
| docutils       | 2.60 sec                                               | 2.54 sec: 1.02x faster                                                            |
| html5lib       | 63.2 ms                                                | 61.9 ms: 1.02x faster                                                             |
| tornado_http   | 96.6 ms                                                | 95.3 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                 | 189 ms: 1.05x faster                                                              |
| float          | 76.3 ms                                                | 73.8 ms: 1.03x faster                                                             |
| nbody          | 95.0 ms                                                | 93.6 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                             |
| regex_compile  | 136 ms                                                 | 133 ms: 1.02x faster                                                              |
| regex_dna      | 203 ms                                                 | 200 ms: 1.02x faster                                                              |
| regex_effbot   | 3.36 ms                                                | 3.55 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                  | 1.00x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 12.7 ms                                                | 9.61 ms: 1.32x faster                                                             |
| unpickle_pure_python | 225 us                                                 | 197 us: 1.15x faster                                                              |
| json_loads           | 26.2 us                                                | 23.8 us: 1.10x faster                                                             |
| xml_etree_parse      | 158 ms                                                 | 148 ms: 1.07x faster                                                              |
| pickle_pure_python   | 304 us                                                 | 285 us: 1.07x faster                                                              |
| pickle_dict          | 31.4 us                                                | 29.7 us: 1.06x faster                                                             |
| pickle_list          | 4.17 us                                                | 4.01 us: 1.04x faster                                                             |
| xml_etree_iterparse  | 103 ms                                                 | 99.1 ms: 1.04x faster                                                             |
| unpickle_list        | 4.95 us                                                | 4.91 us: 1.01x faster                                                             |
| pickle               | 9.79 us                                                | 9.95 us: 1.02x slower                                                             |
| xml_etree_process    | 53.8 ms                                                | 55.6 ms: 1.03x slower                                                             |
| xml_etree_generate   | 76.2 ms                                                | 80.7 ms: 1.06x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                                      |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.36 ms                                                | 9.03 ms: 1.08x slower                                                             |
| python_startup_no_site | 5.96 ms                                                | 6.55 ms: 1.10x slower                                                             |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 52.1 ms                                                | 48.2 ms: 1.08x faster                                                             |
| genshi_text     | 22.1 ms                                                | 21.5 ms: 1.03x faster                                                             |
| django_template | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                             |
| mako            | 9.85 ms                                                | 10.2 ms: 1.03x slower                                                             |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                                      |

All benchmarks:
===============

| Benchmark               | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| generators              | 72.2 ms                                                | 30.7 ms: 2.35x faster                                                             |
| json_dumps              | 12.7 ms                                                | 9.61 ms: 1.32x faster                                                             |
| unpickle_pure_python    | 225 us                                                 | 197 us: 1.15x faster                                                              |
| deltablue               | 3.64 ms                                                | 3.19 ms: 1.14x faster                                                             |
| coroutines              | 26.1 ms                                                | 23.1 ms: 1.13x faster                                                             |
| json_loads              | 26.2 us                                                | 23.8 us: 1.10x faster                                                             |
| mdp                     | 2.62 sec                                               | 2.38 sec: 1.10x faster                                                            |
| richards                | 46.2 ms                                                | 42.2 ms: 1.09x faster                                                             |
| genshi_xml              | 52.1 ms                                                | 48.2 ms: 1.08x faster                                                             |
| json                    | 4.95 ms                                                | 4.59 ms: 1.08x faster                                                             |
| go                      | 143 ms                                                 | 133 ms: 1.08x faster                                                              |
| scimark_sor             | 115 ms                                                 | 107 ms: 1.07x faster                                                              |
| pycparser               | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                            |
| coverage                | 101 ms                                                 | 93.7 ms: 1.07x faster                                                             |
| deepcopy_memo           | 36.4 us                                                | 34.1 us: 1.07x faster                                                             |
| xml_etree_parse         | 158 ms                                                 | 148 ms: 1.07x faster                                                              |
| pickle_pure_python      | 304 us                                                 | 285 us: 1.07x faster                                                              |
| logging_silent          | 98.5 ns                                                | 92.6 ns: 1.06x faster                                                             |
| pickle_dict             | 31.4 us                                                | 29.7 us: 1.06x faster                                                             |
| pidigits                | 199 ms                                                 | 189 ms: 1.05x faster                                                              |
| fannkuch                | 388 ms                                                 | 370 ms: 1.05x faster                                                              |
| sqlglot_normalize       | 108 ms                                                 | 103 ms: 1.05x faster                                                              |
| sqlglot_optimize        | 53.0 ms                                                | 50.6 ms: 1.05x faster                                                             |
| spectral_norm           | 99.9 ms                                                | 95.8 ms: 1.04x faster                                                             |
| pyflate                 | 417 ms                                                 | 400 ms: 1.04x faster                                                              |
| deepcopy                | 344 us                                                 | 330 us: 1.04x faster                                                              |
| pickle_list             | 4.17 us                                                | 4.01 us: 1.04x faster                                                             |
| hexiom                  | 6.35 ms                                                | 6.11 ms: 1.04x faster                                                             |
| xml_etree_iterparse     | 103 ms                                                 | 99.1 ms: 1.04x faster                                                             |
| aiohttp                 | 1.05 ms                                                | 1.01 ms: 1.04x faster                                                             |
| scimark_fft             | 329 ms                                                 | 318 ms: 1.04x faster                                                              |
| float                   | 76.3 ms                                                | 73.8 ms: 1.03x faster                                                             |
| chaos                   | 68.6 ms                                                | 66.3 ms: 1.03x faster                                                             |
| logging_simple          | 6.06 us                                                | 5.87 us: 1.03x faster                                                             |
| logging_format          | 6.62 us                                                | 6.41 us: 1.03x faster                                                             |
| gunicorn                | 1.12 ms                                                | 1.09 ms: 1.03x faster                                                             |
| 2to3                    | 257 ms                                                 | 250 ms: 1.03x faster                                                              |
| genshi_text             | 22.1 ms                                                | 21.5 ms: 1.03x faster                                                             |
| nqueens                 | 85.0 ms                                                | 82.8 ms: 1.03x faster                                                             |
| pprint_pformat          | 1.44 sec                                               | 1.41 sec: 1.03x faster                                                            |
| regex_v8                | 22.3 ms                                                | 21.8 ms: 1.02x faster                                                             |
| scimark_monte_carlo     | 68.3 ms                                                | 66.7 ms: 1.02x faster                                                             |
| telco                   | 6.62 ms                                                | 6.48 ms: 1.02x faster                                                             |
| regex_compile           | 136 ms                                                 | 133 ms: 1.02x faster                                                              |
| pathlib                 | 18.2 ms                                                | 17.8 ms: 1.02x faster                                                             |
| docutils                | 2.60 sec                                               | 2.54 sec: 1.02x faster                                                            |
| async_tree_none         | 529 ms                                                 | 519 ms: 1.02x faster                                                              |
| raytrace                | 290 ms                                                 | 285 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed | 752 ms                                                 | 737 ms: 1.02x faster                                                              |
| html5lib                | 63.2 ms                                                | 61.9 ms: 1.02x faster                                                             |
| bench_thread_pool       | 810 us                                                 | 796 us: 1.02x faster                                                              |
| meteor_contest          | 105 ms                                                 | 103 ms: 1.02x faster                                                              |
| sympy_expand            | 472 ms                                                 | 464 ms: 1.02x faster                                                              |
| regex_dna               | 203 ms                                                 | 200 ms: 1.02x faster                                                              |
| nbody                   | 95.0 ms                                                | 93.6 ms: 1.02x faster                                                             |
| async_tree_io           | 1.31 sec                                               | 1.29 sec: 1.02x faster                                                            |
| tornado_http            | 96.6 ms                                                | 95.3 ms: 1.01x faster                                                             |
| chameleon               | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                             |
| sqlalchemy_declarative  | 139 ms                                                 | 137 ms: 1.01x faster                                                              |
| sympy_integrate         | 20.9 ms                                                | 20.7 ms: 1.01x faster                                                             |
| unpickle_list           | 4.95 us                                                | 4.91 us: 1.01x faster                                                             |
| deepcopy_reduce         | 2.97 us                                                | 2.94 us: 1.01x faster                                                             |
| pprint_safe_repr        | 691 ms                                                 | 687 ms: 1.01x faster                                                              |
| dulwich_log             | 63.9 ms                                                | 64.2 ms: 1.00x slower                                                             |
| sqlalchemy_imperative   | 18.0 ms                                                | 18.2 ms: 1.01x slower                                                             |
| crypto_pyaes            | 73.9 ms                                                | 75.1 ms: 1.02x slower                                                             |
| sympy_sum               | 166 ms                                                 | 169 ms: 1.02x slower                                                              |
| pickle                  | 9.79 us                                                | 9.95 us: 1.02x slower                                                             |
| unpack_sequence         | 43.4 ns                                                | 44.3 ns: 1.02x slower                                                             |
| django_template         | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                             |
| thrift                  | 752 us                                                 | 775 us: 1.03x slower                                                              |
| mako                    | 9.85 ms                                                | 10.2 ms: 1.03x slower                                                             |
| xml_etree_process       | 53.8 ms                                                | 55.6 ms: 1.03x slower                                                             |
| scimark_lu              | 107 ms                                                 | 111 ms: 1.04x slower                                                              |
| sqlglot_transpile       | 1.66 ms                                                | 1.73 ms: 1.04x slower                                                             |
| sqlglot_parse           | 1.37 ms                                                | 1.43 ms: 1.05x slower                                                             |
| sqlite_synth            | 2.49 us                                                | 2.61 us: 1.05x slower                                                             |
| regex_effbot            | 3.36 ms                                                | 3.55 ms: 1.06x slower                                                             |
| xml_etree_generate      | 76.2 ms                                                | 80.7 ms: 1.06x slower                                                             |
| scimark_sparse_mat_mult | 4.40 ms                                                | 4.73 ms: 1.07x slower                                                             |
| python_startup          | 8.36 ms                                                | 9.03 ms: 1.08x slower                                                             |
| python_startup_no_site  | 5.96 ms                                                | 6.55 ms: 1.10x slower                                                             |
| async_generators        | 359 ms                                                 | 418 ms: 1.16x slower                                                              |
| Geometric mean          | (ref)                                                  | 1.03x faster                                                                      |

Benchmark hidden because not significant (4): bench_mp_pool, sympy_str, unpickle, async_tree_memoization
Ignored benchmarks (3) of public/results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, mypy, pylint
Ignored benchmarks (7) of public/results/bm-20230228-3.12.0a5+-969caba/bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5+-969caba.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
