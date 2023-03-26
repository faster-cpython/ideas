# Results

- fork: python
- version: 3.10.10
- commit hash: [aad5f6a](https://github.com/python/cpython/commit/aad5f6a)
- commit date: 2023-02-07T12:05:45+00:00
- ref: aad5f6a89125ad4529ab

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513537895)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a.json)

### vs. 3.11.0

- 1.22x slower
- [table](bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.11.0.md)
- [plot](bm-20230207-pythonperf2-x86_64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4500951050)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a.json)

### vs. 3.10.4

- 1.01x slower
- [table](bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.10.4.md)
- [plot](bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.10.4.png)

### vs. 3.11.0

- 1.12x slower
- [table](bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.11.0.md)
- [plot](bm-20230207-pythonperf1-amd64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505736)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a.json)

### vs. 3.10.4

- 1.02x slower \*
- missing benchmarks: mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.10.4.md)
- [plot](bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.10.4.png)

### vs. 3.11.0

- 1.22x slower
- [table](bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.11.0.md)
- [plot](bm-20230207-darwin-arm64-python-aad5f6a89125ad4529ab-3.10.10-aad5f6a-vs-3.11.0.png)

