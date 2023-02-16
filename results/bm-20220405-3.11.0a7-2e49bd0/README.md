# Results

- fork: python
- ref: 2e49bd06c5ffab7d1540
- version: 3.11.0a7
- commit hash: [2e49bd0](https://github.com/python/cpython/commit/2e49bd0)
- commit date: 2022-04-05T20:54:03+01:00
- ref: main
- commit date: 2022-04-05T19:54:03+00:00

## darwin arm64

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0.json)

### vs. 3.10.4

- 1.22x faster
- missing benchmarks: coverage
- [table](bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0-vs-3.10.4.md)
- [plot](bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: coverage
- [table](bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0-vs-3.11.0.md)
- [plot](bm-20220405-darwin-arm64-python-2e49bd06c5ffab7d1540-3.11.0a7-2e49bd0-vs-3.11.0.png)

## linux x86_64

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-91-generic-x86_64-with-glibc2.31
- [raw results](bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0.json)

### vs. 3.10.4

- 1.24x faster \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0-vs-3.10.4.md)
- [plot](bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x slower \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0-vs-3.11.0.md)
- [plot](bm-20220405-linux-x86_64-python-main-3.11.0a7-2e49bd0-vs-3.11.0.png)

