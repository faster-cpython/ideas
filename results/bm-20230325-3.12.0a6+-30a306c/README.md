# Results

- fork: python
- version: 3.12.0a6+
- commit hash: [30a306c](https://github.com/python/cpython/commit/30a306c)
- commit date: 2023-03-25T16:38:24-07:00
- ref: main

## linux x86_64 (azure)

- [pystats raw](bm-20230325-azure-x86_64-python-main-3.12.0a6%2B-30a306c-pystats.json)
- [pystats table](bm-20230325-azure-x86_64-python-main-3.12.0a6%2B-30a306c-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4521917987)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c.json)

### vs. 3.10.4

- 1.30x faster
- missing benchmarks: flaskblogging, pylint
- [table](bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md)
- [plot](bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: flaskblogging, pylint
- [table](bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md)
- [plot](bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4521917987)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6%2B-30a306c.json)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md)
- [plot](bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4521917987)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c.json)

### vs. 3.10.4

- 1.21x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md)
- [plot](bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.png)

### vs. 3.11.0

- 1.09x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md)
- [plot](bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4521917987)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c.json)

### vs. 3.10.4

- 1.19x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md)
- [plot](bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md)
- [plot](bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.png)

