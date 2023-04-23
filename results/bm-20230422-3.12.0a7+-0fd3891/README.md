# Results

- fork: python
- version: 3.12.0a7+
- commit hash: [0fd3891](https://github.com/python/cpython/commit/0fd3891)
- commit date: 2023-04-22T18:08:27-06:00
- ref: main

## linux x86_64 (azure)

- [pystats raw](bm-20230422-azure-x86_64-python-main-3.12.0a7%2B-0fd3891-pystats.json)
- [pystats table](bm-20230422-azure-x86_64-python-main-3.12.0a7%2B-0fd3891-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4775485741)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230422-linux-x86_64-python-main-3.12.0a7%2B-0fd3891.json)

### vs. 3.10.4

- 1.24x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn
- [table](bm-20230422-linux-x86_64-python-main-3.12.0a7%2B-0fd3891-vs-3.10.4.md)
- [plot](bm-20230422-linux-x86_64-python-main-3.12.0a7%2B-0fd3891-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn
- [table](bm-20230422-linux-x86_64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.md)
- [plot](bm-20230422-linux-x86_64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4775485741)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7%2B-0fd3891.json)

### vs. 3.11.0

- 1.04x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.md)
- [plot](bm-20230422-pythonperf2-x86_64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4775485741)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230422-pythonperf1-amd64-python-main-3.12.0a7%2B-0fd3891.json)

### vs. 3.10.4

- 1.17x faster
- missing benchmarks: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230422-pythonperf1-amd64-python-main-3.12.0a7%2B-0fd3891-vs-3.10.4.md)
- [plot](bm-20230422-pythonperf1-amd64-python-main-3.12.0a7%2B-0fd3891-vs-3.10.4.png)

### vs. 3.11.0

- 1.06x faster
- missing benchmarks: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230422-pythonperf1-amd64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.md)
- [plot](bm-20230422-pythonperf1-amd64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4775485741)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230422-darwin-arm64-python-main-3.12.0a7%2B-0fd3891.json)

### vs. 3.10.4

- 1.24x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230422-darwin-arm64-python-main-3.12.0a7%2B-0fd3891-vs-3.10.4.md)
- [plot](bm-20230422-darwin-arm64-python-main-3.12.0a7%2B-0fd3891-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn
- [table](bm-20230422-darwin-arm64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.md)
- [plot](bm-20230422-darwin-arm64-python-main-3.12.0a7%2B-0fd3891-vs-3.11.0.png)

