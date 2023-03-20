# Results

- fork: python
- version: 3.12.0a5+
- commit hash: [d3ca042](https://github.com/python/cpython/commit/d3ca042)
- commit date: 2023-03-06T22:56:19+09:00
- ref: main

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4333575608)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042.json)

### vs. 3.10.4

- 1.20x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042-vs-3.10.4.md)
- [plot](bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x slower \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042-vs-3.11.0.md)
- [plot](bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042-vs-3.11.0.png)

