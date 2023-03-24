# Results

- fork: python
- version: 3.11.0a1
- commit hash: [7c12e48](https://github.com/python/cpython/commit/7c12e48)
- commit date: 2021-10-05T13:44:05+01:00
- ref: 7c12e4835ebe52287acd

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20211005-linux-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48.json)

### vs. 3.10.4

- 1.12x faster \*
- missing benchmarks: aiohttp, asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20211005-linux-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.10.4.md)
- [plot](bm-20211005-linux-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.10.4.png)

### vs. 3.11.0

- 1.12x slower \*
- missing benchmarks: aiohttp, asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20211005-linux-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.11.0.md)
- [plot](bm-20211005-linux-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.11.0.png)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4513535079)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-67-generic-x86_64-with-glibc2.35
- [raw results](bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48.json)

### vs. 3.10.4

- 1.09x faster
- missing benchmarks: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.10.4.md)
- [plot](bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.10.4.png)

### vs. 3.11.0

- 1.16x slower
- missing benchmarks: aiohttp, asyncio_tcp, djangocms, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.11.0.md)
- [plot](bm-20211005-pythonperf2-x86_64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.11.0.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4483410660)
- cpu model: missing
- platform: Windows-10-10.0.22000-SP0
- [raw results](bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48.json)

### vs. 3.10.4

- 1.01x faster
- missing benchmarks: aiohttp, mypy2
- [table](bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.10.4.md)
- [plot](bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.10.4.png)

### vs. 3.11.0

- 1.09x slower
- missing benchmarks: aiohttp, mypy2
- [table](bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.11.0.md)
- [plot](bm-20211005-pythonperf1-amd64-python-7c12e4835ebe52287acd-3.11.0a1-7c12e48-vs-3.11.0.png)

