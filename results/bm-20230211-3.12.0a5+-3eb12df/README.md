# Results

- fork: python
- version: 3.12.0a5+
- commit hash: [3eb12df](https://github.com/python/cpython/commit/3eb12df)
- commit date: 2023-02-11T21:04:15+05:30
- ref: main

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [pystats raw](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df-pystats.json)
- [pystats table](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df-pystats.md)
- [raw results](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df.json)

### vs. 3.10.4

- 1.29x faster \*
- missing benchmarks: comprehensions, dask, flaskblogging, pylint
- [table](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df-vs-3.10.4.md)
- [plot](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df-vs-3.11.0.md)
- [plot](bm-20230211-linux-x86_64-python-main-3.12.0a5%2B-3eb12df-vs-3.11.0.png)

## darwin arm64 (darwin)

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df.json)

### vs. 3.10.4

- 1.24x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, gc_traversal, mypy2
- [table](bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df-vs-3.10.4.md)
- [plot](bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x faster \*
- missing benchmarks: aiohttp, comprehensions, dask, flaskblogging, gunicorn, pylint
- [table](bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df-vs-3.11.0.md)
- [plot](bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df-vs-3.11.0.png)

