# Results

- fork: faster-cpython
- version: 3.12.0a5+
- commit hash: [5629a3e](https://github.com/faster%2dcpython/cpython/commit/5629a3e)
- commit date: 2023-02-17T16:01:37+00:00
- commit merge base: [d9199175c7386a95aaac91822a2197b9365eb0e8](https://github.com/faster%2dcpython/cpython/commit/d9199175c7386a95aaac91822a2197b9365eb0e8)
- ref: pep_669_incremental

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4205439451)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e.json)

### vs. 3.10.4

- 1.32x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e-vs-3.10.4.md)
- [plot](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e-vs-3.10.4.png)

### vs. 3.11.0

- 1.05x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e-vs-3.11.0.md)
- [plot](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e-vs-3.11.0.png)

### vs. base

- 1.01x faster
- [table](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e-vs-base.md)
- [plot](bm-20230217-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-5629a3e-vs-base.png)

