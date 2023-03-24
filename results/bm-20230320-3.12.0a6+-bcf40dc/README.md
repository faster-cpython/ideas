# Results

- fork: itamaro
- version: 3.12.0a6+
- commit hash: [bcf40dc](https://github.com/itamaro/cpython/commit/bcf40dc)
- commit date: 2023-03-20T16:03:51-07:00
- commit merge base: [094cf392f49d3c16fe798863717f6c8e0f3734bb](https://github.com/itamaro/cpython/commit/094cf392f49d3c16fe798863717f6c8e0f3734bb)
- ref: eager_tasks_factory

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4475369618)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc.json)

### vs. 3.10.4

- 1.31x faster
- missing benchmarks: flaskblogging, pylint, tornado_http
- [table](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc-vs-3.10.4.md)
- [plot](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster \*
- missing benchmarks: flaskblogging, mypy, pylint, tornado_http
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc-vs-3.11.0.md)
- [plot](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc-vs-3.11.0.png)

### vs. base

- 1.00x slower
- missing benchmarks: 🔴 tornado_http
- [table](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc-vs-base.md)
- [plot](bm-20230320-linux-x86_64-itamaro-eager_tasks_factory-3.12.0a6%2B-bcf40dc-vs-base.png)

