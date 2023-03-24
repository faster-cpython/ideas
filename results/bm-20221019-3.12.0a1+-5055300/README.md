# Results

- fork: python
- version: 3.12.0a1+
- commit hash: [5055300](https://github.com/python/cpython/commit/5055300)
- commit date: 2022-10-19T12:00:28+00:00
- ref: main

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20221019-linux-x86_64-python-main-3.12.0a1%2B-5055300.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: async_generators, asyncio_tcp, bench_mp_pool, bench_thread_pool, comprehensions, create_gc_cycles, dask, djangocms, docutils, flaskblogging, gc_traversal, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: mypy
- [table](bm-20221019-linux-x86_64-python-main-3.12.0a1%2B-5055300-vs-3.10.4.md)
- [plot](bm-20221019-linux-x86_64-python-main-3.12.0a1%2B-5055300-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: async_generators, bench_mp_pool, bench_thread_pool, docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221019-linux-x86_64-python-main-3.12.0a1%2B-5055300-vs-3.11.0.md)
- [plot](bm-20221019-linux-x86_64-python-main-3.12.0a1%2B-5055300-vs-3.11.0.png)

