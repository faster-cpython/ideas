# Results

- fork: python
- ref: main
- version: 3.12.0a6+
- commit hash: [3adb23a](https://github.com/python/cpython/commit/3adb23a)
- commit date: 2023-03-18T12:21:48-05:00

## darwin arm64

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4458052230)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a.json)

### vs. 3.10.4

- 1.20x faster \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.md)
- [plot](bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x slower \*
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.md)
- [plot](bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.png)

## linux x86_64

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4458052230)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [pystats raw](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-pystats.json)
- [pystats table](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-pystats.md)
- [raw results](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a.json)

### vs. 3.10.4

- 1.31x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.md)
- [plot](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.md)
- [plot](bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.png)

