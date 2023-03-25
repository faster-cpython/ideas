# Results

- fork: python
- version: 3.11.0rc1
- commit hash: [41cb071](https://github.com/python/cpython/commit/41cb071)
- commit date: 2022-08-05T15:45:18+01:00
- ref: 41cb07120b7792eac641

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20220805-linux-x86_64-python-41cb07120b7792eac641-3.11.0rc1-41cb071.json)

### vs. 3.10.4

- 1.27x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, coverage, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20220805-linux-x86_64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.10.4.md)
- [plot](bm-20220805-linux-x86_64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, coverage, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20220805-linux-x86_64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.11.0.md)
- [plot](bm-20220805-linux-x86_64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513536357)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20220805-pythonperf2-x86_64-python-41cb07120b7792eac641-3.11.0rc1-41cb071.json)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411487)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071.json)

### vs. 3.10.4

- 1.11x faster
- [table](bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.10.4.md)
- [plot](bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x faster
- [table](bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.11.0.md)
- [plot](bm-20220805-pythonperf1-amd64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494504059)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20220805-darwin-arm64-python-41cb07120b7792eac641-3.11.0rc1-41cb071.json)

### vs. 3.10.4

- 1.23x faster \*
- missing benchmarks: coverage, mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20220805-darwin-arm64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.10.4.md)
- [plot](bm-20220805-darwin-arm64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x faster
- missing benchmarks: coverage
- [table](bm-20220805-darwin-arm64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.11.0.md)
- [plot](bm-20220805-darwin-arm64-python-41cb07120b7792eac641-3.11.0rc1-41cb071-vs-3.11.0.png)

