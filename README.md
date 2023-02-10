# Faster CPython Ideas

Discussion and work tracker for Faster CPython project.

New ideas should be created as new [issues](https://github.com/faster-cpython/ideas/issues/new/choose).  It is ok if the idea is not fully formed -- we treat them as discussions to arrive at something actionable.  (We had previously used discussions for this, but that is now deprecated).

The [CPython issue tracker](https://github.com/python/cpython/issues) should be used for actual work-in-progress. 

Some links to presentations and other preliminary documentation:

- [Guido's slides at the 2021 Python Language Summit](FasterCPythonDark.pdf)
- [Mark's slides explaining Tiers of Execution](https://docs.google.com/presentation/d/1_cvQUwO2WWsaySyCmIy9nj9by4JKnkbiPCqtluLP3Mg)
- [PEP 659](https://peps.python.org/pep-0659/)

## Published Results

<!-- START table -->
## linux x86_64
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-02-10](results/bm-20230210-3.12.0a5%2B-685d559) | faster-cpython | specialize | 3.12.0a5+ | 685d559 | [1.30x faster \*](results/bm-20230210-3.12.0a5%2B-685d559/bm-20230210-linux-x86_64-faster%252dcpython-specialized_send-3.12.0a5%2B-685d559-vs-3.10.4.md) | [1.04x faster \*](results/bm-20230210-3.12.0a5%2B-685d559/bm-20230210-linux-x86_64-faster%252dcpython-specialized_send-3.12.0a5%2B-685d559-vs-3.11.0.md) | [1.01x faster](results/bm-20230210-3.12.0a5%2B-685d559/bm-20230210-linux-x86_64-faster%252dcpython-specialized_send-3.12.0a5%2B-685d559-vs-base.md) |
| [2023-02-10](results/bm-20230210-3.12.0a5%2B-d40a23c) | python | d40a23c0a1 | 3.12.0a5+ | d40a23c | [1.29x faster \*](results/bm-20230210-3.12.0a5%2B-d40a23c/bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5%2B-d40a23c-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230210-3.12.0a5%2B-d40a23c/bm-20230210-linux-x86_64-python-d40a23c0a11060ba7fa0-3.12.0a5%2B-d40a23c-vs-3.11.0.md) |  |
| [2023-02-09](results/bm-20230209-3.12.0a5%2B-825f42a) | faster-cpython | pep_669_in | 3.12.0a5+ | 825f42a | [1.31x faster \*](results/bm-20230209-3.12.0a5%2B-825f42a/bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-3.10.4.md) | [1.04x faster \*](results/bm-20230209-3.12.0a5%2B-825f42a/bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-3.11.0.md) | [1.01x faster](results/bm-20230209-3.12.0a5%2B-825f42a/bm-20230209-linux-x86_64-faster%252dcpython-pep_669_incremental-3.12.0a5%2B-825f42a-vs-base.md) |
| [2023-02-08](results/bm-20230208-3.12.0a5%2B-feec49c) | python | feec49c407 | 3.12.0a5+ | feec49c | [1.29x faster \*](results/bm-20230208-3.12.0a5%2B-feec49c/bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5%2B-feec49c-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230208-3.12.0a5%2B-feec49c/bm-20230208-linux-x86_64-python-feec49c40736fc05626a-3.12.0a5%2B-feec49c-vs-3.11.0.md) |  |
| [2023-02-08](results/bm-20230208-3.12.0a5%2B-cd69634) | gvanrossum | call_famil | 3.12.0a5+ | cd69634 | [1.30x faster \*](results/bm-20230208-3.12.0a5%2B-cd69634/bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-cd69634-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230208-3.12.0a5%2B-cd69634/bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-cd69634-vs-3.11.0.md) | [1.00x slower](results/bm-20230208-3.12.0a5%2B-cd69634/bm-20230208-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-cd69634-vs-base.md) |
| [2023-02-07](results/bm-20230207-3.12.0a5%2B-9595e01) | gvanrossum | call_famil | 3.12.0a5+ | 9595e01 | [1.29x faster \*](results/bm-20230207-3.12.0a5%2B-9595e01/bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230207-3.12.0a5%2B-9595e01/bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-3.11.0.md) | [1.00x slower](results/bm-20230207-3.12.0a5%2B-9595e01/bm-20230207-linux-x86_64-gvanrossum-call_family-3.12.0a5%2B-9595e01-vs-base.md) |
| [2023-02-07](results/bm-20230207-3.12.0a5%2B-a9f0144) | python | a9f01448a9 | 3.12.0a5+ | a9f0144 | [1.30x faster \*](results/bm-20230207-3.12.0a5%2B-a9f0144/bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5%2B-a9f0144-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230207-3.12.0a5%2B-a9f0144/bm-20230207-linux-x86_64-python-a9f01448a99c6a2ae34d-3.12.0a5%2B-a9f0144-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | v3.11.0 | 3.11.0 | deaf509 | [1.26x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.26x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |

## darwin arm64
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-02-04](results/bm-20230204-3.12.0a4%2B-5a2b984) | python | main | 3.12.0a4+ | 5a2b984 | [1.23x faster \*](results/bm-20230204-3.12.0a4%2B-5a2b984/bm-20230204-darwin-arm64-python-main-3.12.0a4%2B-5a2b984-vs-3.10.4.md) | [1.01x faster \*](results/bm-20230204-3.12.0a4%2B-5a2b984/bm-20230204-darwin-arm64-python-main-3.12.0a4%2B-5a2b984-vs-3.11.0.md) |  |
| [2023-01-28](results/bm-20230128-3.12.0a4%2B-666c084) | python | main | 3.12.0a4+ | 666c084 | [1.23x faster \*](results/bm-20230128-3.12.0a4%2B-666c084/bm-20230128-darwin-arm64-python-main-3.12.0a4%2B-666c084-vs-3.10.4.md) | [1.00x faster \*](results/bm-20230128-3.12.0a4%2B-666c084/bm-20230128-darwin-arm64-python-main-3.12.0a4%2B-666c084-vs-3.11.0.md) |  |
| [2023-01-21](results/bm-20230121-3.12.0a4%2B-c1c5882) | python | main | 3.12.0a4+ | c1c5882 | [1.22x faster \*](results/bm-20230121-3.12.0a4%2B-c1c5882/bm-20230121-darwin-arm64-python-main-3.12.0a4%2B-c1c5882-vs-3.10.4.md) | [1.00x faster \*](results/bm-20230121-3.12.0a4%2B-c1c5882/bm-20230121-darwin-arm64-python-main-3.12.0a4%2B-c1c5882-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.22x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.22x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |


<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
