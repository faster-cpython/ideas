# Results

- fork: gvanrossum
- ref: call_family
- version: 3.12.0a5+
- commit hash: [9595e01](https://github.com/gvanrossum/cpython/commit/9595e01)
- commit date: 2023-02-07T20:04:44-08:00
- commit merge base: [a9f01448a99c6a2ae34d448806176f2df3a5b323](https://github.com/gvanrossum/cpython/commit/a9f01448a99c6a2ae34d448806176f2df3a5b323)

## linux x86_64

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01.json)

### vs. 3.10.4

- 1.29x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-3.10.4.md)
- [plot](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, create_gc_cycles, djangocms, gc_traversal, mypy2
- [table](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-3.11.0.md)
- [plot](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-3.11.0.png)

### vs. base

- 1.00x slower
- [table](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-base.md)
- [plot](bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-base.png)

