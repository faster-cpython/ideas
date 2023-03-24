# Results

- fork: python
- version: 3.12.0a5+
- commit hash: [d919917](https://github.com/python/cpython/commit/d919917)
- commit date: 2023-02-13T11:31:15+00:00
- ref: d9199175c7386a95aaac

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4205439451)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5%2B-d919917.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: comprehensions, dask, flaskblogging, pylint
- [table](bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5%2B-d919917-vs-3.10.4.md)
- [plot](bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5%2B-d919917-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5%2B-d919917-vs-3.11.0.md)
- [plot](bm-20230213-linux-x86_64-python-d9199175c7386a95aaac-3.12.0a5%2B-d919917-vs-3.11.0.png)

