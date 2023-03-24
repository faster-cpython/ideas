# Results

- fork: python
- version: 3.12.0a6+
- commit hash: [bb396ee](https://github.com/python/cpython/commit/bb396ee)
- commit date: 2023-03-11T11:10:52-08:00
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4394889240)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [pystats raw](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee-pystats.json)
- [pystats table](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee-pystats.md)
- [raw results](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee.json)

### vs. 3.10.4

- 1.30x faster
- missing benchmarks: flaskblogging, pylint
- [table](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee-vs-3.10.4.md)
- [plot](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee-vs-3.11.0.md)
- [plot](bm-20230311-linux-x86_64-python-main-3.12.0a6%2B-bb396ee-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4394889240)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee.json)

### vs. 3.10.4

- 1.19x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.10.4.md)
- [plot](bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.11.0.md)
- [plot](bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.11.0.png)

