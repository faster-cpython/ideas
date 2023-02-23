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
| [2023-02-23](results/bm-20230223-3.12.0a5%2B-d579d2e) | faster-cpython | pep_669 | 3.12.0a5+ | d579d2e | [1.31x faster \*](results/bm-20230223-3.12.0a5%2B-d579d2e/bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-3.10.4.md) | [1.04x faster \*](results/bm-20230223-3.12.0a5%2B-d579d2e/bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-3.11.0.md) | [1.01x faster](results/bm-20230223-3.12.0a5%2B-d579d2e/bm-20230223-linux-x86_64-faster%252dcpython-pep_669-3.12.0a5%2B-d579d2e-vs-base.md) |
| [2023-02-23](results/bm-20230223-3.12.0a5%2B-22b8d77) | python | 22b8d77b98 | 3.12.0a5+ | 22b8d77 | [1.30x faster \*](results/bm-20230223-3.12.0a5%2B-22b8d77/bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5%2B-22b8d77-vs-3.10.4.md) | [1.03x faster \*](results/bm-20230223-3.12.0a5%2B-22b8d77/bm-20230223-linux-x86_64-python-22b8d77b98a5944e688b-3.12.0a5%2B-22b8d77-vs-3.11.0.md) |  |
| [2023-02-20](results/bm-20230220-3.12.0a5%2B-022b44f) | python | 022b44f254 | 3.12.0a5+ | 022b44f | [1.31x faster \*](results/bm-20230220-3.12.0a5%2B-022b44f/bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5%2B-022b44f-vs-3.10.4.md) | [1.04x faster \*](results/bm-20230220-3.12.0a5%2B-022b44f/bm-20230220-linux-x86_64-python-022b44f2546c44183e4d-3.12.0a5%2B-022b44f-vs-3.11.0.md) |  |
| [2023-02-20](results/bm-20230220-3.12.0a5%2B-9f0fc5b) | carljm | inlinecomp | 3.12.0a5+ | 9f0fc5b | [1.32x faster \*](results/bm-20230220-3.12.0a5%2B-9f0fc5b/bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5%2B-9f0fc5b-vs-3.10.4.md) | [1.05x faster \*](results/bm-20230220-3.12.0a5%2B-9f0fc5b/bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5%2B-9f0fc5b-vs-3.11.0.md) | [1.00x faster](results/bm-20230220-3.12.0a5%2B-9f0fc5b/bm-20230220-linux-x86_64-carljm-inlinecomp2-3.12.0a5%2B-9f0fc5b-vs-base.md) |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | v3.11.0 | 3.11.0 | deaf509 | [1.26x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.26x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |

## darwin arm64
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-02-18](results/bm-20230218-3.12.0a5%2B-61f1e67) | python | main | 3.12.0a5+ | 61f1e67 | [1.21x faster \*](results/bm-20230218-3.12.0a5%2B-61f1e67/bm-20230218-darwin-arm64-python-main-3.12.0a5%2B-61f1e67-vs-3.10.4.md) | [1.01x slower \*](results/bm-20230218-3.12.0a5%2B-61f1e67/bm-20230218-darwin-arm64-python-main-3.12.0a5%2B-61f1e67-vs-3.11.0.md) |  |
| [2023-02-11](results/bm-20230211-3.12.0a5%2B-3eb12df) | python | main | 3.12.0a5+ | 3eb12df | [1.24x faster \*](results/bm-20230211-3.12.0a5%2B-3eb12df/bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df-vs-3.10.4.md) | [1.02x faster \*](results/bm-20230211-3.12.0a5%2B-3eb12df/bm-20230211-darwin-arm64-python-main-3.12.0a5%2B-3eb12df-vs-3.11.0.md) |  |
| [2023-02-04](results/bm-20230204-3.12.0a4%2B-5a2b984) | python | main | 3.12.0a4+ | 5a2b984 | [1.23x faster \*](results/bm-20230204-3.12.0a4%2B-5a2b984/bm-20230204-darwin-arm64-python-main-3.12.0a4%2B-5a2b984-vs-3.10.4.md) | [1.01x faster \*](results/bm-20230204-3.12.0a4%2B-5a2b984/bm-20230204-darwin-arm64-python-main-3.12.0a4%2B-5a2b984-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.22x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.22x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |


<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
