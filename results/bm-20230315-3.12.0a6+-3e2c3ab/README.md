# Results

- fork: faster-cpython
- ref: allow_non_python_fra
- version: 3.12.0a6+
- commit hash: [3e2c3ab](https://github.com/faster%2dcpython/cpython/commit/3e2c3ab)
- commit date: 2023-03-15T19:10:51+00:00
- commit merge base: [b45d14b88611fefc6f054226d3e1117082d322c8](https://github.com/faster%2dcpython/cpython/commit/b45d14b88611fefc6f054226d3e1117082d322c8)

## linux x86_64

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4436926255)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230315-linux-x86_64-faster%252dcpython-allow_non_python_fra-3.12.0a6%2B-3e2c3ab.json)

### vs. 3.10.4

- 1.29x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230315-linux-x86_64-faster%252dcpython-allow_non_python_fra-3.12.0a6%2B-3e2c3ab-vs-3.10.4.md)
- [plot](bm-20230315-linux-x86_64-faster%252dcpython-allow_non_python_fra-3.12.0a6%2B-3e2c3ab-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230315-linux-x86_64-faster%252dcpython-allow_non_python_fra-3.12.0a6%2B-3e2c3ab-vs-3.11.0.md)
- [plot](bm-20230315-linux-x86_64-faster%252dcpython-allow_non_python_fra-3.12.0a6%2B-3e2c3ab-vs-3.11.0.png)

