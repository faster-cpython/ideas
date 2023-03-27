# Results

- fork: python
- version: 3.12.0a5+
- commit hash: [f3cb15c](https://github.com/python/cpython/commit/f3cb15c)
- commit date: 2023-02-26T18:10:34-08:00
- ref: f3cb15c88afa2e87067d

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513538243)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c.json)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.11.0.md)
- [plot](bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494506144)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c.json)

### vs. 3.10.4

- 1.20x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.10.4.md)
- [plot](bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.11.0.md)
- [plot](bm-20230226-darwin-arm64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.11.0.png)

