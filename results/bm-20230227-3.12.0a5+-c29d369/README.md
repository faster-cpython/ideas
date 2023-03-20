# Results

- fork: faster-cpython
- version: 3.12.0a5+
- commit hash: [c29d369](https://github.com/faster%2dcpython/cpython/commit/c29d369)
- commit date: 2023-02-27T12:43:09+00:00
- commit merge base: [e3c3f9fec099fe78d2f98912be337d632f6fcdd1](https://github.com/faster%2dcpython/cpython/commit/e3c3f9fec099fe78d2f98912be337d632f6fcdd1)
- ref: check_refcnt_in_bina

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4282488993)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369.json)

### vs. 3.10.4

- 1.31x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369-vs-3.10.4.md)
- [plot](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369-vs-3.11.0.md)
- [plot](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369-vs-3.11.0.png)

### vs. base

- 1.00x faster
- [table](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369-vs-base.md)
- [plot](bm-20230227-linux-x86_64-faster%252dcpython-check_refcnt_in_bina-3.12.0a5%2B-c29d369-vs-base.png)

