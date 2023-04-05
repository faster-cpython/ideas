# Results

- fork: python
- version: 3.12.0a3+
- commit hash: [edfbf56](https://github.com/python/cpython/commit/edfbf56)
- commit date: 2023-01-01T19:14:18-08:00
- ref: edfbf56f4ca6588dfd20

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513537508)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56.json)

### vs. 3.11.0

- 1.04x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.md)
- [plot](bm-20230101-pythonperf2-x86_64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4610450612)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56.json)

### vs. 3.10.4

- 1.17x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.10.4.md)
- [plot](bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.10.4.png)

### vs. 3.11.0

- 1.06x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.md)
- [plot](bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505090)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56.json)

### vs. 3.10.4

- 1.21x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.10.4.md)
- [plot](bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.md)
- [plot](bm-20230101-darwin-arm64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.png)

