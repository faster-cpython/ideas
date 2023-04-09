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
## linux x86_64 (linux)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-08](results/bm-20230408-3.12.0a7%2B-3516704) | python | main | 3.12.0a7+ | 3516704 | [1.31x faster](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.md) | [1.04x faster](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-linux-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md) |  |
| [2023-04-06](results/bm-20230406-3.12.0a6%2B-030016a) | eduardo-elizondo | immortal_r | 3.12.0a6+ | 030016a | [1.22x faster](results/bm-20230406-3.12.0a6%2B-030016a/bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.10.4.md) | [1.03x slower](results/bm-20230406-3.12.0a6%2B-030016a/bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.11.0.md) | [1.06x slower](results/bm-20230406-3.12.0a6%2B-030016a/bm-20230406-linux-x86_64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-base.md) |
| [2023-04-02](results/bm-20230402-3.12.0a6%2B-385b5d6) | python | 385b5d6e09 | 3.12.0a6+ | 385b5d6 | [1.30x faster](results/bm-20230402-3.12.0a6%2B-385b5d6/bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6%2B-385b5d6-vs-3.10.4.md) | [1.03x faster](results/bm-20230402-3.12.0a6%2B-385b5d6/bm-20230402-linux-x86_64-python-385b5d6e091da454c3e0-3.12.0a6%2B-385b5d6-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.25x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | 9d38120e33 | 3.10.4 | 9d38120 |  | [1.27x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md) |  |

## linux x86_64 (pythonperf2)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-08](results/bm-20230408-3.12.0a7%2B-3516704) | python | main | 3.12.0a7+ | 3516704 |  | [1.04x faster](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-pythonperf2-x86_64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md) |  |
| [2023-04-01](results/bm-20230401-3.12.0a6%2B-06249ec) | python | main | 3.12.0a6+ | 06249ec |  | [1.02x faster](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6%2B-06249ec-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c |  | [1.03x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 |  |  |  |

## windows amd64 (pythonperf1)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-08](results/bm-20230408-3.12.0a7%2B-3516704) | python | main | 3.12.0a7+ | 3516704 | [1.20x faster](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.md) | [1.08x faster](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-pythonperf1-amd64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md) |  |
| [2023-04-06](results/bm-20230406-3.12.0a6%2B-030016a) | eduardo-elizondo | immortal_r | 3.12.0a6+ | 030016a | [1.02x faster](results/bm-20230406-3.12.0a6%2B-030016a/bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.10.4.md) | [1.09x slower](results/bm-20230406-3.12.0a6%2B-030016a/bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-3.11.0.md) | [1.20x slower](results/bm-20230406-3.12.0a6%2B-030016a/bm-20230406-pythonperf1-amd64-eduardo%252delizondo-immortal_references-3.12.0a6%2B-030016a-vs-base.md) |
| [2023-04-02](results/bm-20230402-3.12.0a6%2B-385b5d6) | python | 385b5d6e09 | 3.12.0a6+ | 385b5d6 | [1.22x faster](results/bm-20230402-3.12.0a6%2B-385b5d6/bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6%2B-385b5d6-vs-3.10.4.md) | [1.10x faster](results/bm-20230402-3.12.0a6%2B-385b5d6/bm-20230402-pythonperf1-amd64-python-385b5d6e091da454c3e0-3.12.0a6%2B-385b5d6-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.11x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | 9d38120e33 | 3.10.4 | 9d38120 |  | [1.11x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md) |  |

## darwin arm64 (darwin)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-08](results/bm-20230408-3.12.0a7%2B-3516704) | python | main | 3.12.0a7+ | 3516704 | [1.20x faster \*](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704-vs-3.10.4.md) | [1.01x slower](results/bm-20230408-3.12.0a7%2B-3516704/bm-20230408-darwin-arm64-python-main-3.12.0a7%2B-3516704-vs-3.11.0.md) |  |
| [2023-04-01](results/bm-20230401-3.12.0a6%2B-06249ec) | python | main | 3.12.0a6+ | 06249ec | [1.19x faster \*](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-darwin-arm64-python-main-3.12.0a6%2B-06249ec-vs-3.10.4.md) | [1.01x slower](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-darwin-arm64-python-main-3.12.0a6%2B-06249ec-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c | [1.19x faster \*](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md) | [1.02x slower](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.22x faster \*](results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.22x slower \*](results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |


<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
