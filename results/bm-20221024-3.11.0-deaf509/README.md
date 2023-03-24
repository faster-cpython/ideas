# Results

- fork: python
- version: 3.11.0
- commit hash: [deaf509](https://github.com/python/cpython/commit/deaf509)
- commit date: 2022-10-24T18:35:39+01:00
- ref: deaf509e8fc6e0363bd6, v3.11.0

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json)

### vs. 3.10.4

- 1.26x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509-vs-3.10.4.md)
- [plot](bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509-vs-3.10.4.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411576)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json)

### vs. 3.10.4

- 1.11x faster
- [table](bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md)
- [plot](bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494504276)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json)

### vs. 3.10.4

- 1.22x faster \*
- missing benchmarks: mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md)
- [plot](bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.png)

