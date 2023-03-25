# Results

- fork: python
- version: 3.11.0a5
- commit hash: [c4e4b91](https://github.com/python/cpython/commit/c4e4b91)
- commit date: 2022-02-03T18:37:08+00:00
- ref: c4e4b91557f18f881f39, main

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-91-generic-x86_64-with-glibc2.31
- [raw results](bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91.json)

### vs. 3.10.4

- 1.22x faster \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, asyncio_tcp, bench_mp_pool, bench_thread_pool, comprehensions, coroutines, coverage, create_gc_cycles, dask, deepcopy, deepcopy_memo, deepcopy_reduce, djangocms, docutils, flaskblogging, gc_traversal, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy2, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91-vs-3.10.4.md)
- [plot](bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x slower \*
- missing benchmarks: aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_none, asyncio_tcp, bench_mp_pool, bench_thread_pool, comprehensions, coroutines, coverage, create_gc_cycles, dask, deepcopy, deepcopy_memo, deepcopy_reduce, djangocms, docutils, flaskblogging, gc_traversal, generators, genshi_text, genshi_xml, gunicorn, mdp, mypy2, pprint_pformat, pprint_safe_repr, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- [table](bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91-vs-3.11.0.md)
- [plot](bm-20220203-linux-x86_64-python-main-3.11.0a5-c4e4b91-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513535495)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20220203-pythonperf2-x86_64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91.json)

### vs. 3.11.0

- 1.06x slower
- missing benchmarks: mypy2, pylint
- [table](bm-20220203-pythonperf2-x86_64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91-vs-3.11.0.md)
- [plot](bm-20220203-pythonperf2-x86_64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494503386)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20220203-darwin-arm64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91.json)

### vs. 3.10.4

- 1.09x faster \*
- missing benchmarks: aiohttp, gunicorn, mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal
- [table](bm-20220203-darwin-arm64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91-vs-3.10.4.md)
- [plot](bm-20220203-darwin-arm64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91-vs-3.10.4.png)

### vs. 3.11.0

- 1.12x slower
- missing benchmarks: aiohttp, gunicorn, mypy2
- [table](bm-20220203-darwin-arm64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91-vs-3.11.0.md)
- [plot](bm-20220203-darwin-arm64-python-c4e4b91557f18f881f39-3.11.0a5-c4e4b91-vs-3.11.0.png)

