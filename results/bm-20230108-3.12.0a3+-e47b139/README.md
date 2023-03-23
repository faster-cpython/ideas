# Results

- fork: python
- version: 3.12.0a3+
- commit hash: [e47b139](https://github.com/python/cpython/commit/e47b139)
- commit date: 2023-01-08T21:53:56-05:00
- ref: e47b13934b2eb50914e4

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
- [table](bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.10.4.md)
- [plot](bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
- [table](bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.11.0.md)
- [plot](bm-20230108-linux-x86_64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505186)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139.json)

### vs. 3.10.4

- 1.22x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.10.4.md)
- [plot](bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.11.0.md)
- [plot](bm-20230108-darwin-arm64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.11.0.png)

