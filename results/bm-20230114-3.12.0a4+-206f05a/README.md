# Results

- fork: python
- version: 3.12.0a4+
- commit hash: [206f05a](https://github.com/python/cpython/commit/206f05a)
- commit date: 2023-01-14T23:58:06+01:00
- ref: main

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [pystats raw](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a-pystats.json)
- [pystats table](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a-pystats.md)
- [raw results](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
- [table](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a-vs-3.10.4.md)
- [plot](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
- [table](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a-vs-3.11.0.md)
- [plot](bm-20230114-linux-x86_64-python-main-3.12.0a4%2B-206f05a-vs-3.11.0.png)

## darwin arm64 (darwin)

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20230114-darwin-arm64-python-main-3.12.0a4%2B-206f05a.json)

### vs. 3.10.4

- 1.22x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, gc_traversal
- [table](bm-20230114-darwin-arm64-python-main-3.12.0a4%2B-206f05a-vs-3.10.4.md)
- [plot](bm-20230114-darwin-arm64-python-main-3.12.0a4%2B-206f05a-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster \*
- missing benchmarks: aiohttp, comprehensions, flaskblogging, gunicorn, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: mypy
- [table](bm-20230114-darwin-arm64-python-main-3.12.0a4%2B-206f05a-vs-3.11.0.md)
- [plot](bm-20230114-darwin-arm64-python-main-3.12.0a4%2B-206f05a-vs-3.11.0.png)

