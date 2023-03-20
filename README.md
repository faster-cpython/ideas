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
| [2023-03-18](results/bm-20230318-3.12.0a6%2B-3adb23a) | python | main | 3.12.0a6+ | 3adb23a | [1.31x faster \*](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.md) | [1.04x faster \*](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-linux-x86_64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.md) |  |
| [2023-03-17](results/bm-20230317-3.12.0a6%2B-4f5774f) | python | 4f5774f648 | 3.12.0a6+ | 4f5774f | [1.31x faster \*](results/bm-20230317-3.12.0a6%2B-4f5774f/bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6%2B-4f5774f-vs-3.10.4.md) | [1.04x faster \*](results/bm-20230317-3.12.0a6%2B-4f5774f/bm-20230317-linux-x86_64-python-4f5774f648eafd1a7076-3.12.0a6%2B-4f5774f-vs-3.11.0.md) |  |
| [2023-03-16](results/bm-20230316-3.12.0a6%2B-76326f3) | faster-cpython | no_deep_fr | 3.12.0a6+ | 76326f3 | [1.30x faster \*](results/bm-20230316-3.12.0a6%2B-76326f3/bm-20230316-linux-x86_64-faster%252dcpython-no_deep_freeze-3.12.0a6%2B-76326f3-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230316-3.12.0a6%2B-76326f3/bm-20230316-linux-x86_64-faster%252dcpython-no_deep_freeze-3.12.0a6%2B-76326f3-vs-3.11.0.md) | [1.01x slower](results/bm-20230316-3.12.0a6%2B-76326f3/bm-20230316-linux-x86_64-faster%252dcpython-no_deep_freeze-3.12.0a6%2B-76326f3-vs-base.md) |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | v3.11.0 | 3.11.0 | deaf509 | [1.26x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.26x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |

## darwin arm64 (darwin)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-03-18](results/bm-20230318-3.12.0a6%2B-3adb23a) | python | main | 3.12.0a6+ | 3adb23a | [1.20x faster \*](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.md) | [1.02x slower \*](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.md) |  |
| [2023-03-11](results/bm-20230311-3.12.0a6%2B-bb396ee) | python | main | 3.12.0a6+ | bb396ee | [1.19x faster \*](results/bm-20230311-3.12.0a6%2B-bb396ee/bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.10.4.md) | [1.02x slower \*](results/bm-20230311-3.12.0a6%2B-bb396ee/bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.11.0.md) |  |
| [2023-03-06](results/bm-20230306-3.12.0a5%2B-d3ca042) | python | main | 3.12.0a5+ | d3ca042 | [1.20x faster \*](results/bm-20230306-3.12.0a5%2B-d3ca042/bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042-vs-3.10.4.md) | [1.02x slower \*](results/bm-20230306-3.12.0a5%2B-d3ca042/bm-20230306-darwin-arm64-python-main-3.12.0a5%2B-d3ca042-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.22x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.22x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |


<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
