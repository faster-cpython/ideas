# Results

- fork: python
- version: 3.11.0b2
- commit hash: [72f00f4](https://github.com/python/cpython/commit/72f00f4)
- commit date: 2022-05-30T22:18:15+01:00
- commit date: 2022-05-30T21:18:15+00:00
- ref: 72f00f420afaba3bc873, main

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-91-generic-x86_64-with-glibc2.31
- [raw results](bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4.json)

### vs. 3.10.4

- 1.29x faster \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4-vs-3.10.4.md)
- [plot](bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x faster \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4-vs-3.11.0.md)
- [plot](bm-20220530-linux-x86_64-python-main-3.11.0b2-72f00f4-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411222)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4.json)

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: flaskblogging
- [table](bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4-vs-3.11.0.md)
- [plot](bm-20220530-pythonperf1-amd64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4-vs-3.11.0.png)

## darwin arm64 (darwin)

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4.json)

### vs. 3.10.4

- 1.21x faster
- missing benchmarks: coverage, flaskblogging

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: coverage, flaskblogging
- [table](bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4-vs-3.11.0.md)
- [plot](bm-20220530-darwin-arm64-python-72f00f420afaba3bc873-3.11.0b2-72f00f4-vs-3.11.0.png)

