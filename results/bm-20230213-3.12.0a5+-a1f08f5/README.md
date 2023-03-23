# Results

- fork: python
- version: 3.12.0a5+
- commit hash: [a1f08f5](https://github.com/python/cpython/commit/a1f08f5)
- commit date: 2023-02-13T11:11:43+02:00
- ref: a1f08f5f19753c7c9295

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505947)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230213-darwin-arm64-python-a1f08f5f19753c7c9295-3.12.0a5%2B-a1f08f5.json)

### vs. 3.10.4

- 1.23x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, gc_traversal, mypy2
- [table](bm-20230213-darwin-arm64-python-a1f08f5f19753c7c9295-3.12.0a5%2B-a1f08f5-vs-3.10.4.md)
- [plot](bm-20230213-darwin-arm64-python-a1f08f5f19753c7c9295-3.12.0a5%2B-a1f08f5-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x faster
- missing benchmarks: aiohttp, dask, flaskblogging, gunicorn, pylint
- [table](bm-20230213-darwin-arm64-python-a1f08f5f19753c7c9295-3.12.0a5%2B-a1f08f5-vs-3.11.0.md)
- [plot](bm-20230213-darwin-arm64-python-a1f08f5f19753c7c9295-3.12.0a5%2B-a1f08f5-vs-3.11.0.png)

