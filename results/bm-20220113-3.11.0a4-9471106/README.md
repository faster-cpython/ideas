# Results

- fork: python
- ref: 9471106fd5b47418ffd2
- version: 3.11.0a4
- commit hash: [9471106](https://github.com/python/cpython/commit/9471106)
- commit date: 2022-01-13T19:38:15+00:00
- ref: main

## darwin arm64

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20220113-darwin-arm64-python-9471106fd5b47418ffd2-3.11.0a4-9471106.json)

### vs. 3.10.4

- 1.17x faster
- missing benchmarks: aiohttp, gunicorn, mypy
- [table](bm-20220113-darwin-arm64-python-9471106fd5b47418ffd2-3.11.0a4-9471106-vs-3.10.4.md)
- [plot](bm-20220113-darwin-arm64-python-9471106fd5b47418ffd2-3.11.0a4-9471106-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x slower
- missing benchmarks: aiohttp, gunicorn, mypy
- [table](bm-20220113-darwin-arm64-python-9471106fd5b47418ffd2-3.11.0a4-9471106-vs-3.11.0.md)
- [plot](bm-20220113-darwin-arm64-python-9471106fd5b47418ffd2-3.11.0a4-9471106-vs-3.11.0.png)

## linux x86_64

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-91-generic-x86_64-with-glibc2.31
- [raw results](bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106.json)

### vs. 3.10.4

- 1.22x faster \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106-vs-3.10.4.md)
- [plot](bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x slower \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, bench_mp_pool, bench_thread_pool, coroutines, coverage, deepcopy, deepcopy_memo, deepcopy_reduce, docutils, flaskblogging, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106-vs-3.11.0.md)
- [plot](bm-20220113-linux-x86_64-python-main-3.11.0a4-9471106-vs-3.11.0.png)

