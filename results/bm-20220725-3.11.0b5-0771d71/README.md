# Results

- fork: python
- version: 3.11.0b5
- commit hash: [0771d71](https://github.com/python/cpython/commit/0771d71)
- commit date: 2022-07-25T23:21:18+01:00
- ref: 0771d71eea30316020a8

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20220725-linux-x86_64-python-0771d71eea30316020a8-3.11.0b5-0771d71.json)

### vs. 3.10.4

- 1.27x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, coverage, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20220725-linux-x86_64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.10.4.md)
- [plot](bm-20220725-linux-x86_64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x faster \*
- missing benchmarks: asyncio_tcp, comprehensions, coverage, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- new benchmarks: mypy
- [table](bm-20220725-linux-x86_64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.11.0.md)
- [plot](bm-20220725-linux-x86_64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513536218)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20220725-pythonperf2-x86_64-python-0771d71eea30316020a8-3.11.0b5-0771d71.json)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483411382)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20220725-pythonperf1-amd64-python-0771d71eea30316020a8-3.11.0b5-0771d71.json)

### vs. 3.10.4

- 1.10x faster
- [table](bm-20220725-pythonperf1-amd64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.10.4.md)
- [plot](bm-20220725-pythonperf1-amd64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.10.4.png)

### vs. 3.11.0

- 1.00x slower
- [table](bm-20220725-pythonperf1-amd64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.11.0.md)
- [plot](bm-20220725-pythonperf1-amd64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.11.0.png)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4494503968)
- cpu model: missing
- platform: macOS-13.2.1-arm64-arm-64bit
- [raw results](bm-20220725-darwin-arm64-python-0771d71eea30316020a8-3.11.0b5-0771d71.json)

### vs. 3.10.4

- 1.23x faster \*
- missing benchmarks: coverage, mypy
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, gc_traversal, mypy2
- [table](bm-20220725-darwin-arm64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.10.4.md)
- [plot](bm-20220725-darwin-arm64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.10.4.png)

### vs. 3.11.0

- 1.01x faster
- missing benchmarks: coverage
- [table](bm-20220725-darwin-arm64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.11.0.md)
- [plot](bm-20220725-darwin-arm64-python-0771d71eea30316020a8-3.11.0b5-0771d71-vs-3.11.0.png)

