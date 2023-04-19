
# Results vs. base

- fork: faster-cpython
- ref: nogil_latest
- machine: linux-x86_64
- commit hash: 1d39009
- commit date: 2023-04-16
- overall geometric mean: 1.10x slower

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                | 290 ms: 1.15x slower                                                    |
| chameleon      | 6.33 ms                                                               | 7.81 ms: 1.23x slower                                                   |
| docutils       | 2.48 sec                                                              | 3.15 sec: 1.27x slower                                                  |
| html5lib       | 59.3 ms                                                               | 69.2 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.20x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.4 ms                                                               | 65.9 ms: 1.08x faster                                                   |
| pidigits       | 190 ms                                                                | 186 ms: 1.02x faster                                                    |
| nbody          | 94.2 ms                                                               | 107 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 201 ms                                                                | 205 ms: 1.02x slower                                                    |
| regex_v8       | 20.5 ms                                                               | 21.1 ms: 1.03x slower                                                   |
| regex_effbot   | 3.36 ms                                                               | 3.46 ms: 1.03x slower                                                   |
| regex_compile  | 131 ms                                                                | 152 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.06x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 148 ms                                                                | 137 ms: 1.08x faster                                                    |
| pickle_dict          | 31.0 us                                                               | 30.0 us: 1.04x faster                                                   |
| pickle               | 10.2 us                                                               | 10.3 us: 1.01x slower                                                   |
| unpickle_list        | 5.00 us                                                               | 5.20 us: 1.04x slower                                                   |
| pickle_list          | 4.15 us                                                               | 4.33 us: 1.04x slower                                                   |
| xml_etree_iterparse  | 105 ms                                                                | 114 ms: 1.08x slower                                                    |
| json_dumps           | 9.53 ms                                                               | 10.4 ms: 1.09x slower                                                   |
| xml_etree_generate   | 76.6 ms                                                               | 83.7 ms: 1.09x slower                                                   |
| pickle_pure_python   | 284 us                                                                | 321 us: 1.13x slower                                                    |
| xml_etree_process    | 53.7 ms                                                               | 61.3 ms: 1.14x slower                                                   |
| unpickle_pure_python | 200 us                                                                | 229 us: 1.14x slower                                                    |
| json_loads           | 24.1 us                                                               | 28.0 us: 1.16x slower                                                   |
| unpickle             | 13.1 us                                                               | 15.5 us: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.08x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.54 ms                                                               | 9.18 ms: 1.08x slower                                                   |
| python_startup_no_site | 6.08 ms                                                               | 6.59 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 46.5 ms                                                               | 52.0 ms: 1.12x slower                                                   |
| django_template | 31.9 ms                                                               | 37.4 ms: 1.17x slower                                                   |
| genshi_text     | 20.6 ms                                                               | 24.4 ms: 1.18x slower                                                   |
| mako            | 9.67 ms                                                               | 13.2 ms: 1.37x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark               | bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7 | bm-20230416-linux-x86_64-faster%2dcpython-nogil_latest-3.12.0a4-1d39009 |
|-------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io           | 1.33 sec                                                              | 616 ms: 2.15x faster                                                    |
| async_tree_none         | 529 ms                                                                | 311 ms: 1.70x faster                                                    |
| async_tree_memoization  | 630 ms                                                                | 381 ms: 1.65x faster                                                    |
| async_tree_cpu_io_mixed | 753 ms                                                                | 534 ms: 1.41x faster                                                    |
| gc_traversal            | 4.15 ms                                                               | 3.67 ms: 1.13x faster                                                   |
| float                   | 71.4 ms                                                               | 65.9 ms: 1.08x faster                                                   |
| xml_etree_parse         | 148 ms                                                                | 137 ms: 1.08x faster                                                    |
| pickle_dict             | 31.0 us                                                               | 30.0 us: 1.04x faster                                                   |
| pidigits                | 190 ms                                                                | 186 ms: 1.02x faster                                                    |
| bench_mp_pool           | 24.0 ms                                                               | 23.8 ms: 1.01x faster                                                   |
| pickle                  | 10.2 us                                                               | 10.3 us: 1.01x slower                                                   |
| regex_dna               | 201 ms                                                                | 205 ms: 1.02x slower                                                    |
| pathlib                 | 17.8 ms                                                               | 18.2 ms: 1.02x slower                                                   |
| sqlite_synth            | 2.56 us                                                               | 2.62 us: 1.02x slower                                                   |
| generators              | 77.0 ms                                                               | 78.8 ms: 1.02x slower                                                   |
| regex_v8                | 20.5 ms                                                               | 21.1 ms: 1.03x slower                                                   |
| regex_effbot            | 3.36 ms                                                               | 3.46 ms: 1.03x slower                                                   |
| asyncio_tcp             | 506 ms                                                                | 525 ms: 1.04x slower                                                    |
| unpickle_list           | 5.00 us                                                               | 5.20 us: 1.04x slower                                                   |
| pickle_list             | 4.15 us                                                               | 4.33 us: 1.04x slower                                                   |
| mdp                     | 2.66 sec                                                              | 2.79 sec: 1.05x slower                                                  |
| json                    | 4.77 ms                                                               | 5.06 ms: 1.06x slower                                                   |
| pycparser               | 1.08 sec                                                              | 1.15 sec: 1.06x slower                                                  |
| async_generators        | 353 ms                                                                | 377 ms: 1.07x slower                                                    |
| python_startup          | 8.54 ms                                                               | 9.18 ms: 1.08x slower                                                   |
| coroutines              | 24.8 ms                                                               | 26.8 ms: 1.08x slower                                                   |
| python_startup_no_site  | 6.08 ms                                                               | 6.59 ms: 1.08x slower                                                   |
| go                      | 135 ms                                                                | 146 ms: 1.08x slower                                                    |
| xml_etree_iterparse     | 105 ms                                                                | 114 ms: 1.08x slower                                                    |
| dulwich_log             | 62.5 ms                                                               | 68.1 ms: 1.09x slower                                                   |
| json_dumps              | 9.53 ms                                                               | 10.4 ms: 1.09x slower                                                   |
| crypto_pyaes            | 75.1 ms                                                               | 81.8 ms: 1.09x slower                                                   |
| coverage                | 100 ms                                                                | 109 ms: 1.09x slower                                                    |
| nqueens                 | 78.6 ms                                                               | 85.8 ms: 1.09x slower                                                   |
| xml_etree_generate      | 76.6 ms                                                               | 83.7 ms: 1.09x slower                                                   |
| sqlglot_normalize       | 104 ms                                                                | 115 ms: 1.10x slower                                                    |
| chaos                   | 67.7 ms                                                               | 74.6 ms: 1.10x slower                                                   |
| logging_silent          | 93.8 ns                                                               | 104 ns: 1.11x slower                                                    |
| pprint_safe_repr        | 691 ms                                                                | 765 ms: 1.11x slower                                                    |
| create_gc_cycles        | 1.43 ms                                                               | 1.59 ms: 1.11x slower                                                   |
| telco                   | 6.24 ms                                                               | 6.92 ms: 1.11x slower                                                   |
| comprehensions          | 23.6 us                                                               | 26.3 us: 1.12x slower                                                   |
| pprint_pformat          | 1.41 sec                                                              | 1.58 sec: 1.12x slower                                                  |
| genshi_xml              | 46.5 ms                                                               | 52.0 ms: 1.12x slower                                                   |
| sympy_integrate         | 20.3 ms                                                               | 22.8 ms: 1.12x slower                                                   |
| hexiom                  | 6.13 ms                                                               | 6.89 ms: 1.13x slower                                                   |
| deepcopy                | 334 us                                                                | 375 us: 1.13x slower                                                    |
| sqlglot_optimize        | 50.7 ms                                                               | 57.1 ms: 1.13x slower                                                   |
| pickle_pure_python      | 284 us                                                                | 321 us: 1.13x slower                                                    |
| nbody                   | 94.2 ms                                                               | 107 ms: 1.14x slower                                                    |
| thrift                  | 748 us                                                                | 851 us: 1.14x slower                                                    |
| scimark_sor             | 107 ms                                                                | 123 ms: 1.14x slower                                                    |
| xml_etree_process       | 53.7 ms                                                               | 61.3 ms: 1.14x slower                                                   |
| unpickle_pure_python    | 200 us                                                                | 229 us: 1.14x slower                                                    |
| 2to3                    | 252 ms                                                                | 290 ms: 1.15x slower                                                    |
| sympy_str               | 284 ms                                                                | 329 ms: 1.16x slower                                                    |
| json_loads              | 24.1 us                                                               | 28.0 us: 1.16x slower                                                   |
| richards                | 41.6 ms                                                               | 48.4 ms: 1.16x slower                                                   |
| regex_compile           | 131 ms                                                                | 152 ms: 1.16x slower                                                    |
| sympy_expand            | 461 ms                                                                | 537 ms: 1.17x slower                                                    |
| html5lib                | 59.3 ms                                                               | 69.2 ms: 1.17x slower                                                   |
| djangocms               | 32.4 us                                                               | 37.9 us: 1.17x slower                                                   |
| scimark_sparse_mat_mult | 4.22 ms                                                               | 4.94 ms: 1.17x slower                                                   |
| deepcopy_reduce         | 2.92 us                                                               | 3.42 us: 1.17x slower                                                   |
| django_template         | 31.9 ms                                                               | 37.4 ms: 1.17x slower                                                   |
| spectral_norm           | 95.6 ms                                                               | 112 ms: 1.17x slower                                                    |
| scimark_lu              | 109 ms                                                                | 128 ms: 1.17x slower                                                    |
| sympy_sum               | 164 ms                                                                | 192 ms: 1.18x slower                                                    |
| genshi_text             | 20.6 ms                                                               | 24.4 ms: 1.18x slower                                                   |
| deepcopy_memo           | 34.0 us                                                               | 40.1 us: 1.18x slower                                                   |
| unpickle                | 13.1 us                                                               | 15.5 us: 1.18x slower                                                   |
| fannkuch                | 369 ms                                                                | 436 ms: 1.18x slower                                                    |
| scimark_monte_carlo     | 64.3 ms                                                               | 76.4 ms: 1.19x slower                                                   |
| pyflate                 | 395 ms                                                                | 470 ms: 1.19x slower                                                    |
| deltablue               | 3.29 ms                                                               | 3.91 ms: 1.19x slower                                                   |
| logging_format          | 6.37 us                                                               | 7.66 us: 1.20x slower                                                   |
| meteor_contest          | 103 ms                                                                | 124 ms: 1.21x slower                                                    |
| scimark_fft             | 315 ms                                                                | 383 ms: 1.22x slower                                                    |
| logging_simple          | 5.74 us                                                               | 7.00 us: 1.22x slower                                                   |
| chameleon               | 6.33 ms                                                               | 7.81 ms: 1.23x slower                                                   |
| raytrace                | 280 ms                                                                | 346 ms: 1.24x slower                                                    |
| sqlglot_transpile       | 1.69 ms                                                               | 2.10 ms: 1.25x slower                                                   |
| docutils                | 2.48 sec                                                              | 3.15 sec: 1.27x slower                                                  |
| sqlglot_parse           | 1.40 ms                                                               | 1.79 ms: 1.28x slower                                                   |
| unpack_sequence         | 42.9 ns                                                               | 58.1 ns: 1.35x slower                                                   |
| mako                    | 9.67 ms                                                               | 13.2 ms: 1.37x slower                                                   |
| mypy2                   | 332 ms                                                                | 457 ms: 1.38x slower                                                    |
| bench_thread_pool       | 783 us                                                                | 1.64 ms: 2.10x slower                                                   |
| Geometric mean          | (ref)                                                                 | 1.10x slower                                                            |
Ignored benchmarks (1) of public/results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7.json: dask
