# Results

- fork: python
- version: 3.12.0a4+
- commit hash: [c4170c3](https://github.com/python/cpython/commit/c4170c3)
- commit date: 2023-01-29T16:41:27-08:00
- ref: c4170c36b0b54c10456f

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505524)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230129-darwin-arm64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3.json)

### vs. 3.10.4

- 1.21x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230129-darwin-arm64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3-vs-3.10.4.md)
- [plot](bm-20230129-darwin-arm64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230129-darwin-arm64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3-vs-3.11.0.md)
- [plot](bm-20230129-darwin-arm64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3-vs-3.11.0.png)

