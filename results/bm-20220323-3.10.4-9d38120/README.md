# Results

- fork: python
- version: 3.10.4
- commit hash: [9d38120](https://github.com/python/cpython/commit/9d38120)
- commit date: 2022-03-23T20:12:04+00:00
- ref: 9d38120e335357a3b294, v3.10.4

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json)

### vs. 3.11.0

- 1.26x slower
- [table](bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md)
- [plot](bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4491158802)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120.json)

### vs. 3.11.0

- 1.11x slower
- [table](bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md)
- [plot](bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.png)

## darwin arm64 (darwin)

- cpu model: missing
- platform: macOS-12.6-arm64-arm-64bit
- [raw results](bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json)

### vs. 3.11.0

- 1.22x slower \*
- missing benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md)
- [plot](bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.png)

