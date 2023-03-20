# Results

- fork: faster_cpython
- version: 3.9.10
- commit hash: [258cab1](https://github.com/faster_cpython/cpython/commit/258cab1)
- commit date: 2022-12-21T19:44:41-08:00
- ref: nogil

## linux x86_64 (linux)

- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1.json)

### vs. 3.10.4

- 1.00x faster
- missing benchmarks: pprint_safe_repr, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms
- [table](bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1-vs-3.10.4.md)
- [plot](bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1-vs-3.10.4.png)

### vs. 3.11.0

- 1.26x slower
- missing benchmarks: pprint_safe_repr, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms
- [table](bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1-vs-3.11.0.md)
- [plot](bm-20221221-linux-x86_64-faster_cpython-nogil-3.9.10-258cab1-vs-3.11.0.png)

