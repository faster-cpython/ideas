# Results

- fork: eduardo-elizondo
- version: 3.12.0a3+
- commit hash: [1dfe27a](https://github.com/eduardo%2delizondo/cpython/commit/1dfe27a)
- commit date: 2023-01-08T23:39:54-05:00
- commit merge base: [e47b13934b2eb50914e4dbae91f1dc59f8325e30](https://github.com/eduardo%2delizondo/cpython/commit/e47b13934b2eb50914e4dbae91f1dc59f8325e30)
- ref: immortal_references

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a.json)

### vs. 3.10.4

- 1.22x faster \*
- missing benchmarks: aiohttp, comprehensions, flaskblogging, gunicorn, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: mypy
- [table](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.10.4.md)
- [plot](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x slower \*
- missing benchmarks: aiohttp, comprehensions, flaskblogging, gunicorn, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: mypy
- [table](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.11.0.md)
- [plot](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.11.0.png)

### vs. base

- 1.06x slower
- [table](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-base.md)
- [plot](bm-20230108-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-base.png)

## darwin arm64 (darwin)

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a.json)

### vs. 3.10.4

- 1.24x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, gc_traversal
- [table](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.10.4.md)
- [plot](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x faster \*
- missing benchmarks: aiohttp, comprehensions, flaskblogging, gunicorn, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: mypy
- [table](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.11.0.md)
- [plot](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-3.11.0.png)

### vs. base

- 1.02x faster \*
- missing benchmarks: 🔴 comprehensions, mypy2
- new benchmarks: mypy
- [table](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-base.md)
- [plot](bm-20230108-darwin-arm64-eduardo%252delizondo-immortal_references-3.12.0a3%2B-1dfe27a-vs-base.png)

