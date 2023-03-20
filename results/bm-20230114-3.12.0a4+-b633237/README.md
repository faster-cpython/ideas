# Results

- fork: brandtbucher
- version: 3.12.0a4+
- commit hash: [b633237](https://github.com/brandtbucher/cpython/commit/b633237)
- commit date: 2023-01-14T17:42:48-08:00
- commit merge base: [8a2d4f4e8eea86352de37d2ce28117e13b3dfaed](https://github.com/brandtbucher/cpython/commit/8a2d4f4e8eea86352de37d2ce28117e13b3dfaed)
- ref: no_superinstructions

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237.json)

### vs. 3.10.4

- 1.29x faster \*
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
- [table](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237-vs-3.10.4.md)
- [plot](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237-vs-3.10.4.png)

### vs. 3.11.0

- 1.02x faster \*
- missing benchmarks: flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: asyncio_tcp, create_gc_cycles, dask, djangocms, gc_traversal
- [table](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237-vs-3.11.0.md)
- [plot](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237-vs-3.11.0.png)

### vs. base

- 1.01x slower
- [table](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237-vs-base.md)
- [plot](bm-20230114-linux-x86_64-brandtbucher-no_superinstructions-3.12.0a4%2B-b633237-vs-base.png)

