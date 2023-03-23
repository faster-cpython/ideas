
# Results vs. 3.10.4

- fork: python
- ref: edfbf56f4ca6588dfd20
- machine: darwin-arm64
- commit hash: edfbf56
- commit date: 2023-01-01
- overall geometric mean: 1.21x faster \*

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 222 ms                                                 | 163 ms: 1.36x faster                                                   |
| chameleon      | 5.86 ms                                                | 4.56 ms: 1.28x faster                                                  |
| docutils       | 1.76 sec                                               | 1.46 sec: 1.20x faster                                                 |
| html5lib       | 44.0 ms                                                | 34.1 ms: 1.29x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 94.6 ms                                                | 63.8 ms: 1.48x faster                                                  |
| float          | 72.1 ms                                                | 51.6 ms: 1.40x faster                                                  |
| pidigits       | 284 ms                                                 | 280 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 96.2 ms                                                | 74.9 ms: 1.28x faster                                                  |
| regex_v8       | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                  |
| regex_dna      | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| regex_effbot   | 2.45 ms                                                | 2.60 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 284 us                                                 | 193 us: 1.47x faster                                                   |
| unpickle_pure_python | 204 us                                                 | 142 us: 1.44x faster                                                   |
| json_dumps           | 8.34 ms                                                | 6.13 ms: 1.36x faster                                                  |
| xml_etree_process    | 45.1 ms                                                | 35.2 ms: 1.28x faster                                                  |
| xml_etree_generate   | 54.5 ms                                                | 48.5 ms: 1.12x faster                                                  |
| json_loads           | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| unpickle             | 10.0 us                                                | 9.63 us: 1.04x faster                                                  |
| xml_etree_parse      | 100 ms                                                 | 96.5 ms: 1.04x faster                                                  |
| pickle               | 7.50 us                                                | 7.46 us: 1.01x faster                                                  |
| pickle_dict          | 18.0 us                                                | 18.0 us: 1.00x slower                                                  |
| pickle_list          | 2.83 us                                                | 2.84 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 69.0 ms                                                | 69.9 ms: 1.01x slower                                                  |
| unpickle_list        | 2.66 us                                                | 2.70 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.59 ms                                                | 12.3 ms: 1.29x slower                                                  |
| python_startup_no_site | 7.00 ms                                                | 10.3 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 37.7 ms                                                | 28.4 ms: 1.33x faster                                                  |
| mako            | 10.6 ms                                                | 8.15 ms: 1.30x faster                                                  |
| django_template | 27.2 ms                                                | 22.0 ms: 1.24x faster                                                  |
| genshi_text     | 18.2 ms                                                | 15.0 ms: 1.21x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.27x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deltablue               | 5.37 ms                                                | 2.62 ms: 2.05x faster                                                  |
| logging_silent          | 119 ns                                                 | 64.7 ns: 1.84x faster                                                  |
| richards                | 51.4 ms                                                | 30.4 ms: 1.69x faster                                                  |
| scimark_sor             | 126 ms                                                 | 80.3 ms: 1.57x faster                                                  |
| go                      | 165 ms                                                 | 108 ms: 1.53x faster                                                   |
| scimark_lu              | 110 ms                                                 | 71.8 ms: 1.53x faster                                                  |
| raytrace                | 329 ms                                                 | 217 ms: 1.52x faster                                                   |
| nbody                   | 94.6 ms                                                | 63.8 ms: 1.48x faster                                                  |
| pickle_pure_python      | 284 us                                                 | 193 us: 1.47x faster                                                   |
| async_tree_memoization  | 485 ms                                                 | 333 ms: 1.46x faster                                                   |
| scimark_monte_carlo     | 72.3 ms                                                | 49.8 ms: 1.45x faster                                                  |
| crypto_pyaes            | 77.9 ms                                                | 53.8 ms: 1.45x faster                                                  |
| unpickle_pure_python    | 204 us                                                 | 142 us: 1.44x faster                                                   |
| pyflate                 | 454 ms                                                 | 325 ms: 1.40x faster                                                   |
| float                   | 72.1 ms                                                | 51.6 ms: 1.40x faster                                                  |
| async_tree_none         | 396 ms                                                 | 289 ms: 1.37x faster                                                   |
| 2to3                    | 222 ms                                                 | 163 ms: 1.36x faster                                                   |
| json_dumps              | 8.34 ms                                                | 6.13 ms: 1.36x faster                                                  |
| pycparser               | 915 ms                                                 | 678 ms: 1.35x faster                                                   |
| async_tree_io           | 1.01 sec                                               | 750 ms: 1.35x faster                                                   |
| deepcopy_memo           | 34.4 us                                                | 25.8 us: 1.33x faster                                                  |
| genshi_xml              | 37.7 ms                                                | 28.4 ms: 1.33x faster                                                  |
| logging_simple          | 4.61 us                                                | 3.47 us: 1.33x faster                                                  |
| pprint_pformat          | 1.24 sec                                               | 936 ms: 1.32x faster                                                   |
| pprint_safe_repr        | 608 ms                                                 | 460 ms: 1.32x faster                                                   |
| logging_format          | 4.95 us                                                | 3.76 us: 1.31x faster                                                  |
| thrift                  | 577 us                                                 | 441 us: 1.31x faster                                                   |
| chaos                   | 66.5 ms                                                | 51.0 ms: 1.30x faster                                                  |
| mako                    | 10.6 ms                                                | 8.15 ms: 1.30x faster                                                  |
| spectral_norm           | 95.8 ms                                                | 74.2 ms: 1.29x faster                                                  |
| html5lib                | 44.0 ms                                                | 34.1 ms: 1.29x faster                                                  |
| regex_compile           | 96.2 ms                                                | 74.9 ms: 1.28x faster                                                  |
| sqlglot_transpile       | 1.54 ms                                                | 1.20 ms: 1.28x faster                                                  |
| chameleon               | 5.86 ms                                                | 4.56 ms: 1.28x faster                                                  |
| sqlglot_parse           | 1.33 ms                                                | 1.03 ms: 1.28x faster                                                  |
| xml_etree_process       | 45.1 ms                                                | 35.2 ms: 1.28x faster                                                  |
| hexiom                  | 6.31 ms                                                | 4.93 ms: 1.28x faster                                                  |
| deepcopy                | 278 us                                                 | 221 us: 1.26x faster                                                   |
| deepcopy_reduce         | 2.36 us                                                | 1.90 us: 1.24x faster                                                  |
| fannkuch                | 318 ms                                                 | 257 ms: 1.24x faster                                                   |
| django_template         | 27.2 ms                                                | 22.0 ms: 1.24x faster                                                  |
| dulwich_log             | 36.4 ms                                                | 29.6 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed | 665 ms                                                 | 543 ms: 1.22x faster                                                   |
| scimark_sparse_mat_mult | 3.47 ms                                                | 2.85 ms: 1.22x faster                                                  |
| genshi_text             | 18.2 ms                                                | 15.0 ms: 1.21x faster                                                  |
| docutils                | 1.76 sec                                               | 1.46 sec: 1.20x faster                                                 |
| sqlglot_optimize        | 38.1 ms                                                | 31.8 ms: 1.20x faster                                                  |
| unpack_sequence         | 38.2 ns                                                | 32.7 ns: 1.17x faster                                                  |
| scimark_fft             | 231 ms                                                 | 198 ms: 1.17x faster                                                   |
| sympy_integrate         | 13.3 ms                                                | 11.5 ms: 1.15x faster                                                  |
| async_generators        | 231 ms                                                 | 201 ms: 1.15x faster                                                   |
| bench_thread_pool       | 531 us                                                 | 465 us: 1.14x faster                                                   |
| sqlglot_normalize       | 198 ms                                                 | 175 ms: 1.13x faster                                                   |
| regex_v8                | 17.7 ms                                                | 15.7 ms: 1.13x faster                                                  |
| json                    | 3.13 ms                                                | 2.78 ms: 1.12x faster                                                  |
| xml_etree_generate      | 54.5 ms                                                | 48.5 ms: 1.12x faster                                                  |
| sympy_expand            | 275 ms                                                 | 245 ms: 1.12x faster                                                   |
| sqlite_synth            | 1.50 us                                                | 1.34 us: 1.11x faster                                                  |
| nqueens                 | 68.6 ms                                                | 61.6 ms: 1.11x faster                                                  |
| coroutines              | 20.1 ms                                                | 18.1 ms: 1.11x faster                                                  |
| sympy_str               | 169 ms                                                 | 153 ms: 1.10x faster                                                   |
| regex_dna               | 164 ms                                                 | 149 ms: 1.10x faster                                                   |
| sympy_sum               | 93.5 ms                                                | 86.1 ms: 1.09x faster                                                  |
| mdp                     | 1.66 sec                                               | 1.53 sec: 1.08x faster                                                 |
| json_loads              | 17.0 us                                                | 16.1 us: 1.06x faster                                                  |
| unpickle                | 10.0 us                                                | 9.63 us: 1.04x faster                                                  |
| xml_etree_parse         | 100 ms                                                 | 96.5 ms: 1.04x faster                                                  |
| telco                   | 3.63 ms                                                | 3.54 ms: 1.03x faster                                                  |
| meteor_contest          | 77.7 ms                                                | 76.4 ms: 1.02x faster                                                  |
| pidigits                | 284 ms                                                 | 280 ms: 1.01x faster                                                   |
| pickle                  | 7.50 us                                                | 7.46 us: 1.01x faster                                                  |
| pickle_dict             | 18.0 us                                                | 18.0 us: 1.00x slower                                                  |
| pickle_list             | 2.83 us                                                | 2.84 us: 1.01x slower                                                  |
| xml_etree_iterparse     | 69.0 ms                                                | 69.9 ms: 1.01x slower                                                  |
| unpickle_list           | 2.66 us                                                | 2.70 us: 1.02x slower                                                  |
| generators              | 32.5 ms                                                | 33.2 ms: 1.02x slower                                                  |
| regex_effbot            | 2.45 ms                                                | 2.60 ms: 1.06x slower                                                  |
| bench_mp_pool           | 40.8 ms                                                | 44.3 ms: 1.09x slower                                                  |
| pathlib                 | 22.2 ms                                                | 27.4 ms: 1.24x slower                                                  |
| python_startup          | 9.59 ms                                                | 12.3 ms: 1.29x slower                                                  |
| coverage                | 40.8 ms                                                | 54.6 ms: 1.34x slower                                                  |
| python_startup_no_site  | 7.00 ms                                                | 10.3 ms: 1.47x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.21x faster                                                           |
Ignored benchmarks (8) of public/results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
Ignored benchmarks (6) of public/results/bm-20230101-3.12.0a3+-edfbf56/bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3+-edfbf56.json: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
