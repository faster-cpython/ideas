# Results

- fork: python
- version: 3.12.0a3+
- commit hash: [ad3c99e](https://github.com/python/cpython/commit/ad3c99e)
- commit date: 2022-12-26T00:22:53-06:00
- ref: ad3c99e521151680afc6

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505019)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20221226-darwin-arm64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e.json)

### vs. 3.10.4

- 1.21x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20221226-darwin-arm64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e-vs-3.10.4.md)
- [plot](bm-20221226-darwin-arm64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20221226-darwin-arm64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e-vs-3.11.0.md)
- [plot](bm-20221226-darwin-arm64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e-vs-3.11.0.png)

