# Results

- fork: eduardo-elizondo
- version: 3.12.0a6+
- commit hash: [030016a](https://github.com/eduardo%2delizondo/cpython/commit/030016a)
- commit date: 2023-04-06T01:51:16-04:00
- commit merge base: [385b5d6e091da454c3e0d3f7271acf3af26d8532](https://github.com/eduardo%2delizondo/cpython/commit/385b5d6e091da454c3e0d3f7271acf3af26d8532)
- ref: immortal_references

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4627236855)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-122-generic-x86_64-with-glibc2.31
- [raw results](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a.json)

### vs. 3.10.4

- 1.22x faster
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.10.4.md)
- [plot](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.10.4.png)

### vs. 3.11.0

- 1.03x slower
- missing benchmarks: aiohttp, flaskblogging, gunicorn, pylint
- [table](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.11.0.md)
- [plot](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.11.0.png)

### vs. base

- 1.06x slower
- missing benchmarks: 🔴 aiohttp, gunicorn
- [table](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-base.md)
- [plot](bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-base.png)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/4627792073)
- cpu model: missing
- platform: Windows-11-10.0.22000-SP0
- [raw results](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a.json)

### vs. 3.10.4

- 1.02x faster
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.10.4.md)
- [plot](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.10.4.png)

### vs. 3.11.0

- 1.09x slower
- missing benchmarks: aiohttp, flaskblogging, pylint, sqlalchemy_declarative, sqlalchemy_imperative
- [table](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.11.0.md)
- [plot](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.11.0.png)

### vs. base

- 1.20x slower
- [table](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-base.md)
- [plot](bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-base.png)

