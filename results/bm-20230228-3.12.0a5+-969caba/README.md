# Results

- fork: ericsnowcurrently
- ref: isolate_interned_dic
- version: 3.12.0a5+
- commit hash: [969caba](https://github.com/ericsnowcurrently/cpython/commit/969caba)
- commit date: 2023-02-28T14:18:12-07:00
- commit merge base: [880437d4ec65ef35d505eeaff9dad5c6654dbc1a](https://github.com/ericsnowcurrently/cpython/commit/880437d4ec65ef35d505eeaff9dad5c6654dbc1a)

## linux x86_64

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4297757282)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba.json)

### vs. 3.10.4

- 1.30x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba-vs-3.10.4.md)
- [plot](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x faster \*
- missing benchmarks: flaskblogging, mypy, pylint
- new benchmarks: asyncio_tcp, comprehensions, create_gc_cycles, dask, djangocms, gc_traversal, mypy2
- [table](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba-vs-3.11.0.md)
- [plot](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba-vs-3.11.0.png)

### vs. base

- 1.01x faster
- [table](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba-vs-base.md)
- [plot](bm-20230228-linux-x86_64-ericsnowcurrently-isolate_interned_dic-3.12.0a5%2B-969caba-vs-base.png)

