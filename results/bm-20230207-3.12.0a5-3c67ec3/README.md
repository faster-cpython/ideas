# Results

- fork: python
- version: 3.12.0a5
- commit hash: [3c67ec3](https://github.com/python/cpython/commit/3c67ec3)
- commit date: 2023-02-07T13:21:15+01:00
- ref: 3c67ec394faac79d2608

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4511434995)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3.json)

### vs. 3.10.4

- 1.22x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.10.4.md)
- [plot](bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.10.4.png)

### vs. 3.11.0

- 1.10x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.md)
- [plot](bm-20230207-pythonperf1-amd64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4546451814)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3.json)

### vs. 3.10.4

- 1.21x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.10.4.md)
- [plot](bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.md)
- [plot](bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.png)

