# Results

- fork: python
- version: 3.11.0a2
- commit hash: [e2b4e4b](https://github.com/python/cpython/commit/e2b4e4b)
- commit date: 2021-11-05T19:04:04+00:00
- ref: e2b4e4bab90b69fbd361

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b.json)

### vs. 3.10.4

- 1.15x faster \*
- missing benchmarks: aiohttp, asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.10.4.md)
- [plot](bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.10.4.png)

### vs. 3.11.0

- 1.09x slower
- missing benchmarks: aiohttp, mypy
- [table](bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.11.0.md)
- [plot](bm-20211105-linux-x86_64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4491158300)
- cpu model: missing
- platform: Windows-10-10.0.22000
- [raw results](bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b.json)

### vs. 3.10.4

- 1.02x faster
- missing benchmarks: aiohttp, mypy2
- [table](bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.10.4.md)
- [plot](bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.10.4.png)

### vs. 3.11.0

- 1.08x slower
- missing benchmarks: aiohttp, mypy2
- [table](bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.11.0.md)
- [plot](bm-20211105-pythonperf1-amd64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494503166)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b.json)

### vs. 3.10.4

- 1.15x faster \*
- missing benchmarks: aiohttp, mypy
- new benchmarks: comprehensions, create_gc_cycles, dask, gc_traversal
- [table](bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.10.4.md)
- [plot](bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.10.4.png)

### vs. 3.11.0

- 1.05x slower
- missing benchmarks: aiohttp, asyncio_tcp, mypy2
- [table](bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.11.0.md)
- [plot](bm-20211105-darwin-arm64-python-e2b4e4bab90b69fbd361-3.11.0a2-e2b4e4b-vs-3.11.0.png)

