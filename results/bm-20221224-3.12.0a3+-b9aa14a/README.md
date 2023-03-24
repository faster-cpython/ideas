# Results

- fork: python
- version: 3.12.0a3+
- commit hash: [b9aa14a](https://github.com/python/cpython/commit/b9aa14a)
- commit date: 2022-12-24T18:14:51-06:00
- ref: main

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [pystats raw](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a-pystats.json)
- [pystats table](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a-pystats.md)
- [raw results](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: aiohttp, asyncio_tcp, comprehensions, create_gc_cycles, dask, flaskblogging, gc_traversal, gunicorn, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: mypy
- [table](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a-vs-3.10.4.md)
- [plot](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: djangocms
- [table](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a-vs-3.11.0.md)
- [plot](bm-20221224-linux-x86_64-python-main-3.12.0a3%2B-b9aa14a-vs-3.11.0.png)

