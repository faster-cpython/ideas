# Results

- fork: python
- version: 3.12.0a4+
- commit hash: [7b14c2e](https://github.com/python/cpython/commit/7b14c2e)
- commit date: 2023-01-16T12:35:21+00:00
- ref: 7b14c2ef194b6eed7967

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513537554)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e.json)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.11.0.md)
- [plot](bm-20230116-pythonperf2-x86_64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505304)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e.json)

### vs. 3.10.4

- 1.21x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.10.4.md)
- [plot](bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.11.0.md)
- [plot](bm-20230116-darwin-arm64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.11.0.png)

