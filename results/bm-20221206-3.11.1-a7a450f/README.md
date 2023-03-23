# Results

- fork: python
- version: 3.11.1
- commit hash: [a7a450f](https://github.com/python/cpython/commit/a7a450f)
- commit date: 2022-12-06T19:05:27+00:00
- ref: a7a450f84a0874216031

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20221206-linux-x86_64-python-a7a450f84a0874216031-3.11.1-a7a450f.json)

### vs. 3.10.4

- 1.25x faster
- [table](bm-20221206-linux-x86_64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.10.4.md)
- [plot](bm-20221206-linux-x86_64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x slower
- [table](bm-20221206-linux-x86_64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.11.0.md)
- [plot](bm-20221206-linux-x86_64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411626)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20221206-pythonperf1-amd64-python-a7a450f84a0874216031-3.11.1-a7a450f.json)

### vs. 3.10.4

- 1.10x faster
- [table](bm-20221206-pythonperf1-amd64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.10.4.md)
- [plot](bm-20221206-pythonperf1-amd64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x slower
- [table](bm-20221206-pythonperf1-amd64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.11.0.md)
- [plot](bm-20221206-pythonperf1-amd64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.11.0.png)

## darwin arm64 (darwin)

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20221206-darwin-arm64-python-a7a450f84a0874216031-3.11.1-a7a450f.json)

### vs. 3.10.4

- 1.22x faster
- [table](bm-20221206-darwin-arm64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.10.4.md)
- [plot](bm-20221206-darwin-arm64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20221206-darwin-arm64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.11.0.md)
- [plot](bm-20221206-darwin-arm64-python-a7a450f84a0874216031-3.11.1-a7a450f-vs-3.11.0.png)

