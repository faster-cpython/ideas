Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| chameleon      | 8.86 ms                                                | 6.46 ms: 1.37x faster                                  |
| html5lib       | 85.8 ms                                                | 60.2 ms: 1.43x faster                                  |
| tornado_http   | 128 ms                                                 | 93.0 ms: 1.38x faster                                  |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 108 ms                                                 | 71.1 ms: 1.51x faster                                  |
| nbody          | 136 ms                                                 | 94.8 ms: 1.44x faster                                  |
| pidigits       | 190 ms                                                 | 193 ms: 1.01x slower                                   |
| Geometric mean | (ref)                                                  | 1.29x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna      | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot   | 3.21 ms                                                | 3.40 ms: 1.06x slower                                  |
| regex_v8       | 25.0 ms                                                | 21.4 ms: 1.17x faster                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 13.5 ms                                                | 9.42 ms: 1.43x faster                                  |
| json_loads           | 28.9 us                                                | 24.0 us: 1.20x faster                                  |
| pickle               | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict          | 28.3 us                                                | 31.1 us: 1.10x slower                                  |
| pickle_list          | 4.50 us                                                | 3.99 us: 1.13x faster                                  |
| pickle_pure_python   | 453 us                                                 | 285 us: 1.59x faster                                   |
| unpickle             | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| unpickle_list        | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python | 297 us                                                 | 202 us: 1.47x faster                                   |
| xml_etree_parse      | 163 ms                                                 | 144 ms: 1.13x faster                                   |
| xml_etree_iterparse  | 110 ms                                                 | 106 ms: 1.04x faster                                   |
| xml_etree_generate   | 93.3 ms                                                | 76.9 ms: 1.21x faster                                  |
| xml_etree_process    | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean       | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 13.9 ms                                                | 8.32 ms: 1.68x faster                                  |
| python_startup_no_site | 5.76 ms                                                | 6.03 ms: 1.05x slower                                  |
| Geometric mean         | (ref)                                                  | 1.27x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 46.3 ms                                                | 32.7 ms: 1.41x faster                                  |
| genshi_text     | 30.6 ms                                                | 20.9 ms: 1.46x faster                                  |
| genshi_xml      | 63.6 ms                                                | 49.3 ms: 1.29x faster                                  |
| mako            | 14.3 ms                                                | 9.79 ms: 1.46x faster                                  |
| Geometric mean  | (ref)                                                  | 1.40x faster                                           |

All benchmarks:
===============

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20221019-linux-x86_64-python-main-3.12.0a1+-5055300 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3                    | 332 ms                                                 | 249 ms: 1.34x faster                                   |
| aiohttp                 | 1.34 ms                                                | 1.00 ms: 1.34x faster                                  |
| async_tree_none         | 713 ms                                                 | 526 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed | 949 ms                                                 | 732 ms: 1.30x faster                                   |
| async_tree_io           | 1.78 sec                                               | 1.31 sec: 1.35x faster                                 |
| async_tree_memoization  | 854 ms                                                 | 657 ms: 1.30x faster                                   |
| chameleon               | 8.86 ms                                                | 6.46 ms: 1.37x faster                                  |
| chaos                   | 104 ms                                                 | 67.8 ms: 1.53x faster                                  |
| coroutines              | 31.7 ms                                                | 24.5 ms: 1.29x faster                                  |
| coverage                | 75.3 ms                                                | 97.7 ms: 1.30x slower                                  |
| crypto_pyaes            | 118 ms                                                 | 75.4 ms: 1.56x faster                                  |
| deepcopy                | 429 us                                                 | 333 us: 1.29x faster                                   |
| deepcopy_reduce         | 3.75 us                                                | 2.89 us: 1.30x faster                                  |
| deepcopy_memo           | 50.0 us                                                | 34.5 us: 1.45x faster                                  |
| deltablue               | 7.39 ms                                                | 3.36 ms: 2.20x faster                                  |
| django_template         | 46.3 ms                                                | 32.7 ms: 1.41x faster                                  |
| dulwich_log             | 75.5 ms                                                | 61.2 ms: 1.23x faster                                  |
| fannkuch                | 477 ms                                                 | 363 ms: 1.32x faster                                   |
| float                   | 108 ms                                                 | 71.1 ms: 1.51x faster                                  |
| generators              | 75.8 ms                                                | 71.4 ms: 1.06x faster                                  |
| genshi_text             | 30.6 ms                                                | 20.9 ms: 1.46x faster                                  |
| genshi_xml              | 63.6 ms                                                | 49.3 ms: 1.29x faster                                  |
| go                      | 226 ms                                                 | 136 ms: 1.66x faster                                   |
| gunicorn                | 1.43 ms                                                | 1.08 ms: 1.33x faster                                  |
| hexiom                  | 9.42 ms                                                | 6.11 ms: 1.54x faster                                  |
| html5lib                | 85.8 ms                                                | 60.2 ms: 1.43x faster                                  |
| json                    | 5.35 ms                                                | 4.77 ms: 1.12x faster                                  |
| json_dumps              | 13.5 ms                                                | 9.42 ms: 1.43x faster                                  |
| json_loads              | 28.9 us                                                | 24.0 us: 1.20x faster                                  |
| logging_format          | 8.92 us                                                | 6.49 us: 1.38x faster                                  |
| logging_silent          | 173 ns                                                 | 93.3 ns: 1.86x faster                                  |
| logging_simple          | 8.06 us                                                | 5.83 us: 1.38x faster                                  |
| mako                    | 14.3 ms                                                | 9.79 ms: 1.46x faster                                  |
| mdp                     | 2.82 sec                                               | 2.69 sec: 1.05x faster                                 |
| meteor_contest          | 114 ms                                                 | 102 ms: 1.12x faster                                   |
| mypy                    | 1.01 sec                                               | 799 ms: 1.27x faster                                   |
| nbody                   | 136 ms                                                 | 94.8 ms: 1.44x faster                                  |
| nqueens                 | 99.3 ms                                                | 80.9 ms: 1.23x faster                                  |
| pathlib                 | 20.0 ms                                                | 17.6 ms: 1.14x faster                                  |
| pickle                  | 10.1 us                                                | 10.3 us: 1.02x slower                                  |
| pickle_dict             | 28.3 us                                                | 31.1 us: 1.10x slower                                  |
| pickle_list             | 4.50 us                                                | 3.99 us: 1.13x faster                                  |
| pickle_pure_python      | 453 us                                                 | 285 us: 1.59x faster                                   |
| pidigits                | 190 ms                                                 | 193 ms: 1.01x slower                                   |
| pprint_safe_repr        | 943 ms                                                 | 669 ms: 1.41x faster                                   |
| pprint_pformat          | 1.97 sec                                               | 1.37 sec: 1.44x faster                                 |
| pycparser               | 1.51 sec                                               | 1.08 sec: 1.39x faster                                 |
| pyflate                 | 675 ms                                                 | 409 ms: 1.65x faster                                   |
| pylint                  | 519 ms                                                 | 454 ms: 1.15x faster                                   |
| python_startup          | 13.9 ms                                                | 8.32 ms: 1.68x faster                                  |
| python_startup_no_site  | 5.76 ms                                                | 6.03 ms: 1.05x slower                                  |
| raytrace                | 461 ms                                                 | 289 ms: 1.60x faster                                   |
| regex_compile           | 174 ms                                                 | 128 ms: 1.36x faster                                   |
| regex_dna               | 214 ms                                                 | 205 ms: 1.04x faster                                   |
| regex_effbot            | 3.21 ms                                                | 3.40 ms: 1.06x slower                                  |
| regex_v8                | 25.0 ms                                                | 21.4 ms: 1.17x faster                                  |
| richards                | 71.4 ms                                                | 45.2 ms: 1.58x faster                                  |
| scimark_fft             | 414 ms                                                 | 311 ms: 1.33x faster                                   |
| scimark_lu              | 158 ms                                                 | 108 ms: 1.47x faster                                   |
| scimark_monte_carlo     | 105 ms                                                 | 67.0 ms: 1.56x faster                                  |
| scimark_sor             | 193 ms                                                 | 104 ms: 1.86x faster                                   |
| scimark_sparse_mat_mult | 5.48 ms                                                | 4.04 ms: 1.36x faster                                  |
| spectral_norm           | 148 ms                                                 | 95.4 ms: 1.55x faster                                  |
| sqlglot_parse           | 2.04 ms                                                | 1.33 ms: 1.53x faster                                  |
| sqlglot_transpile       | 2.42 ms                                                | 1.63 ms: 1.49x faster                                  |
| sqlglot_optimize        | 65.3 ms                                                | 51.0 ms: 1.28x faster                                  |
| sqlglot_normalize       | 135 ms                                                 | 104 ms: 1.30x faster                                   |
| sqlite_synth            | 2.90 us                                                | 2.60 us: 1.12x faster                                  |
| sympy_expand            | 537 ms                                                 | 456 ms: 1.18x faster                                   |
| sympy_integrate         | 23.9 ms                                                | 20.3 ms: 1.18x faster                                  |
| sympy_sum               | 183 ms                                                 | 163 ms: 1.13x faster                                   |
| sympy_str               | 324 ms                                                 | 280 ms: 1.16x faster                                   |
| telco                   | 6.68 ms                                                | 6.43 ms: 1.04x faster                                  |
| thrift                  | 1.03 ms                                                | 742 us: 1.39x faster                                   |
| tornado_http            | 128 ms                                                 | 93.0 ms: 1.38x faster                                  |
| unpack_sequence         | 59.5 ns                                                | 45.7 ns: 1.30x faster                                  |
| unpickle                | 14.3 us                                                | 13.3 us: 1.08x faster                                  |
| unpickle_list           | 4.99 us                                                | 5.02 us: 1.01x slower                                  |
| unpickle_pure_python    | 297 us                                                 | 202 us: 1.47x faster                                   |
| xml_etree_parse         | 163 ms                                                 | 144 ms: 1.13x faster                                   |
| xml_etree_iterparse     | 110 ms                                                 | 106 ms: 1.04x faster                                   |
| xml_etree_generate      | 93.3 ms                                                | 76.9 ms: 1.21x faster                                  |
| xml_etree_process       | 74.5 ms                                                | 53.3 ms: 1.40x faster                                  |
| Geometric mean          | (ref)                                                  | 1.30x faster                                           |
Ignored benchmarks (7) of ../ideas/results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
