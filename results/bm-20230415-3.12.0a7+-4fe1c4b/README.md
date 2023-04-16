# Results

- fork: python
- version: 3.12.0a7+
- commit hash: [4fe1c4b](https://github.com/python/cpython/commit/4fe1c4b)
- commit date: 2023-04-15T13:48:31-07:00
- ref: main

## linux x86_64 (azure)

- [pystats raw](bm-20230415-azure-x86_64-python-main-3.12.0a7%2B-4fe1c4b-pystats.json)
- [pystats table](bm-20230415-azure-x86_64-python-main-3.12.0a7%2B-4fe1c4b-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4710535001)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230415-linux-x86_64-python-main-3.12.0a7%2B-4fe1c4b.json)

### vs. 3.10.4

- 1.31x faster
- missing benchmarks: flaskblogging
- [table](bm-20230415-linux-x86_64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.10.4.md)
- [plot](bm-20230415-linux-x86_64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.10.4.png)

### vs. 3.11.0

- 1.05x faster
- missing benchmarks: flaskblogging
- [table](bm-20230415-linux-x86_64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.md)
- [plot](bm-20230415-linux-x86_64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4710535001)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7%2B-4fe1c4b.json)

### vs. 3.11.0

- 1.04x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.md)
- [plot](bm-20230415-pythonperf2-x86_64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4710535001)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230415-pythonperf1-amd64-python-main-3.12.0a7%2B-4fe1c4b.json)

### vs. 3.10.4

- 1.20x faster
- missing benchmarks: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230415-pythonperf1-amd64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.10.4.md)
- [plot](bm-20230415-pythonperf1-amd64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.10.4.png)

### vs. 3.11.0

- 1.09x faster
- missing benchmarks: aiohttp, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230415-pythonperf1-amd64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.md)
- [plot](bm-20230415-pythonperf1-amd64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4710535001)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230415-darwin-arm64-python-main-3.12.0a7%2B-4fe1c4b.json)

### vs. 3.10.4

- 1.25x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230415-darwin-arm64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.10.4.md)
- [plot](bm-20230415-darwin-arm64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn
- [table](bm-20230415-darwin-arm64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.md)
- [plot](bm-20230415-darwin-arm64-python-main-3.12.0a7%2B-4fe1c4b-vs-3.11.0.png)

