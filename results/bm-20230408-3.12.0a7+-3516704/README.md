# Results

- fork: python
- version: 3.12.0a7+
- commit hash: [3516704](https://github.com/python/cpython/commit/3516704)
- commit date: 2023-04-08T10:56:42-07:00
- ref: main

## linux x86_64 (azure)

- [pystats raw](bm-20230408-azure-x86_64-python-main-3.12.0a7%2B-3516704-pystats.json)
- [pystats table](bm-20230408-azure-x86_64-python-main-3.12.0a7%2B-3516704-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4647840179)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704.json)

### vs. 3.10.4

- 1.31x faster
- missing benchmarks: flaskblogging, pylint
- [table](bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.md)
- [plot](bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster
- missing benchmarks: flaskblogging, pylint
- [table](bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md)
- [plot](bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4647840179)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7%2B-3516704.json)

### vs. 3.11.0

- 1.04x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md)
- [plot](bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4647840179)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704.json)

### vs. 3.10.4

- 1.20x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.md)
- [plot](bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.png)

### vs. 3.11.0

- 1.08x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md)
- [plot](bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4647840179)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704.json)

### vs. 3.10.4

- 1.20x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.md)
- [plot](bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md)
- [plot](bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.png)

