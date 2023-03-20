# Results

- fork: faster-cpython
- version: 3.12.0a5+
- commit hash: [825f42a](https://github.com/faster%2dcpython/cpython/commit/825f42a)
- commit date: 2023-02-09T15:09:32+00:00
- commit merge base: [feec49c40736fc05626a183a8d14c4ebbea5ae28](https://github.com/faster%2dcpython/cpython/commit/feec49c40736fc05626a183a8d14c4ebbea5ae28)
- ref: pep_669_incremental

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a.json)

### vs. 3.10.4

- 1.31x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-3.10.4.md)
- [plot](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-3.11.0.md)
- [plot](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-3.11.0.png)

### vs. base

- 1.01x faster
- [table](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-base.md)
- [plot](bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-base.png)

