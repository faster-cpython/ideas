# Results

- fork: python
- version: 3.12.0a2+
- commit hash: [e3a3863](https://github.com/python/cpython/commit/e3a3863)
- commit date: 2022-12-05T12:35:31+02:00
- ref: e3a3863cb9561705d3dd

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20221205-linux-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, flaskblogging, gc_traversal, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: mypy
- [table](bm-20221205-linux-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.md)
- [plot](bm-20221205-linux-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, flaskblogging, gc_traversal, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: mypy
- [table](bm-20221205-linux-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.md)
- [plot](bm-20221205-linux-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513536886)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20221205-pythonperf2-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863.json)

### vs. 3.11.0

- 1.02x faster
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221205-pythonperf2-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.md)
- [plot](bm-20221205-pythonperf2-x86_64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4610450374)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863.json)

### vs. 3.10.4

- 1.19x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.md)
- [plot](bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.png)

### vs. 3.11.0

- 1.07x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.md)
- [plot](bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494504591)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20221205-darwin-arm64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863.json)

### vs. 3.10.4

- 1.18x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20221205-darwin-arm64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.md)
- [plot](bm-20221205-darwin-arm64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20221205-darwin-arm64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.md)
- [plot](bm-20221205-darwin-arm64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.png)

