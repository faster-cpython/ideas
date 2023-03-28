# Results

- fork: python
- version: 3.12.0a1
- commit hash: [4ae1a0e](https://github.com/python/cpython/commit/4ae1a0e)
- commit date: 2022-10-25T00:08:22+02:00
- ref: 4ae1a0ecaffe4320fe97

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4546461065)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e.json)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.md)
- [plot](bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4511435250)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e.json)

### vs. 3.10.4

- 1.12x faster
- missing benchmarks: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.10.4.md)
- [plot](bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x faster
- missing benchmarks: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.md)
- [plot](bm-20221025-pythonperf1-amd64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4546451537)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e.json)

### vs. 3.10.4

- 1.18x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.10.4.md)
- [plot](bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.md)
- [plot](bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.png)

