# Results

- fork: python
- version: 3.11.2
- commit hash: [878ead1](https://github.com/python/cpython/commit/878ead1)
- commit date: 2023-02-07T13:37:51+00:00
- ref: 878ead1ac16519651263

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513537912)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20230207-pythonperf2-x86_64-python-878ead1ac16519651263-3.11.2-878ead1.json)

### vs. 3.11.0

- 1.01x slower
- [table](bm-20230207-pythonperf2-x86_64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.11.0.md)
- [plot](bm-20230207-pythonperf2-x86_64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411696)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20230207-pythonperf1-amd64-python-878ead1ac16519651263-3.11.2-878ead1.json)

### vs. 3.10.4

- 1.11x faster
- [table](bm-20230207-pythonperf1-amd64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.10.4.md)
- [plot](bm-20230207-pythonperf1-amd64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster
- [table](bm-20230207-pythonperf1-amd64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.11.0.md)
- [plot](bm-20230207-pythonperf1-amd64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494505838)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20230207-darwin-arm64-python-878ead1ac16519651263-3.11.2-878ead1.json)

### vs. 3.10.4

- 1.20x faster \*
- missing benchmarks: mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20230207-darwin-arm64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.10.4.md)
- [plot](bm-20230207-darwin-arm64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x slower
- [table](bm-20230207-darwin-arm64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.11.0.md)
- [plot](bm-20230207-darwin-arm64-python-878ead1ac16519651263-3.11.2-878ead1-vs-3.11.0.png)

