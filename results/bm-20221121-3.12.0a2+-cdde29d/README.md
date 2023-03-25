# Results

- fork: python
- version: 3.12.0a2+
- commit hash: [cdde29d](https://github.com/python/cpython/commit/cdde29d)
- commit date: 2022-11-21T10:50:20+01:00
- ref: cdde29dde90947df9bac

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d.json)

### vs. 3.10.4

- 1.31x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, flaskblogging, gc_traversal, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: mypy
- [table](bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.10.4.md)
- [plot](bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, flaskblogging, gc_traversal, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: mypy
- [table](bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.md)
- [plot](bm-20221121-linux-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513536703)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d.json)

### vs. 3.11.0

- 1.02x faster
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.md)
- [plot](bm-20221121-pythonperf2-x86_64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494504370)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d.json)

### vs. 3.10.4

- 1.19x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.10.4.md)
- [plot](bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.md)
- [plot](bm-20221121-darwin-arm64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.png)

