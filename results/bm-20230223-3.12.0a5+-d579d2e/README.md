# Results

- fork: faster-cpython
- ref: pep_669
- version: 3.12.0a5+
- commit hash: [d579d2e](https://github.com/faster%2dcpython/cpython/commit/d579d2e)
- commit date: 2023-02-23T13:14:05+00:00
- commit merge base: [22b8d77b98a5944e688be0927b8139c49d4a7257](https://github.com/faster%2dcpython/cpython/commit/22b8d77b98a5944e688be0927b8139c49d4a7257)

## linux x86_64

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4253128438)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e.json)

### vs. 3.10.4

- 1.31x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-3.10.4.md)
- [plot](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-3.10.4.png)

### vs. 3.11.0

- 1.04x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-3.11.0.md)
- [plot](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-3.11.0.png)

### vs. base

- 1.01x faster
- [table](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-base.md)
- [plot](bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-base.png)

