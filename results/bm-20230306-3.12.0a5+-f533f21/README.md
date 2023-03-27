# Results

- fork: python
- version: 3.12.0a5+
- commit hash: [f533f21](https://github.com/python/cpython/commit/f533f21)
- commit date: 2023-03-06T14:41:53+01:00
- ref: f533f216e6aaba3f3663

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513538290)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21.json)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.11.0.md)
- [plot](bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494506299)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21.json)

### vs. 3.10.4

- 1.19x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.10.4.md)
- [plot](bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.11.0.md)
- [plot](bm-20230306-darwin-arm64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.11.0.png)

