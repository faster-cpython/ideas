# Results

- fork: faster-cpython
- version: 3.12.0a4
- commit hash: [1d39009](https://github.com/faster%2dcpython/cpython/commit/1d39009)
- commit date: 2023-04-16T13:41:10-07:00
- ref: nogil_latest

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4744083530)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230416-linux-x86_64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009.json)

### vs. 3.10.4

- 1.19x faster
- missing benchmarks: aiohttp, dask, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230416-linux-x86_64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.10.4.md)
- [plot](bm-20230416-linux-x86_64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.10.4.png)

### vs. 3.11.0

- 1.05x slower
- missing benchmarks: aiohttp, dask, flaskblogging, gunicorn, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230416-linux-x86_64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.11.0.md)
- [plot](bm-20230416-linux-x86_64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4744088784)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230416-pythonperf1-amd64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009.json)

### vs. 3.10.4

- 1.06x faster
- missing benchmarks: aiohttp, dask, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230416-pythonperf1-amd64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.10.4.md)
- [plot](bm-20230416-pythonperf1-amd64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.10.4.png)

### vs. 3.11.0

- 1.05x slower
- missing benchmarks: aiohttp, dask, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [table](bm-20230416-pythonperf1-amd64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.11.0.md)
- [plot](bm-20230416-pythonperf1-amd64-faster%252dcpython-nogil_latest-3.12.0a4-1d39009-vs-3.11.0.png)

