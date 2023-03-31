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
| [2023-03-26](results/bm-20230326-3.12.0a6%2B-2cdc518) | python | 2cdc5189a6 | 3.12.0a6+ | 2cdc518 | [1.30x faster](results/bm-20230326-3.12.0a6%2B-2cdc518/bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6%2B-2cdc518-vs-3.10.4.md) | [1.03x faster](results/bm-20230326-3.12.0a6%2B-2cdc518/bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6%2B-2cdc518-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-662c16c) | faster-cpython | pep_669 | 3.12.0a6+ | 662c16c | [1.32x faster](results/bm-20230325-3.12.0a6%2B-662c16c/bm-20230325-linux-x86_64-faster%252dcpython-pep_669-3.12.0a6%2B-662c16c-vs-3.10.4.md) | [1.05x faster](results/bm-20230325-3.12.0a6%2B-662c16c/bm-20230325-linux-x86_64-faster%252dcpython-pep_669-3.12.0a6%2B-662c16c-vs-3.11.0.md) | [1.02x faster](results/bm-20230325-3.12.0a6%2B-662c16c/bm-20230325-linux-x86_64-faster%252dcpython-pep_669-3.12.0a6%2B-662c16c-vs-base.md) |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c | [1.30x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md) | [1.03x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-linux-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2023-03-07](results/bm-20230307-3.12.0a6-f9774e5) | python | f9774e57d8 | 3.12.0a6 | f9774e5 | [1.29x faster](results/bm-20230307-3.12.0a6-f9774e5/bm-20230307-linux-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5-vs-3.10.4.md) | [1.03x faster](results/bm-20230307-3.12.0a6-f9774e5/bm-20230307-linux-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5-vs-3.11.0.md) |  |
| [2023-02-07](results/bm-20230207-3.12.0a5-3c67ec3) | python | 3c67ec394f | 3.12.0a5 | 3c67ec3 | [1.30x faster](results/bm-20230207-3.12.0a5-3c67ec3/bm-20230207-linux-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.10.4.md) | [1.04x faster](results/bm-20230207-3.12.0a5-3c67ec3/bm-20230207-linux-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.md) |  |
| [2023-01-10](results/bm-20230110-3.12.0a4-3d5d3f7) | python | 3d5d3f7af6 | 3.12.0a4 | 3d5d3f7 | [1.30x faster](results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7-vs-3.10.4.md) | [1.04x faster](results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-linux-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7-vs-3.11.0.md) |  |
| [2022-12-06](results/bm-20221206-3.12.0a3-b6bd7ff) | python | b6bd7ffcbc | 3.12.0a3 | b6bd7ff | [1.29x faster](results/bm-20221206-3.12.0a3-b6bd7ff/bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff-vs-3.10.4.md) | [1.03x faster](results/bm-20221206-3.12.0a3-b6bd7ff/bm-20221206-linux-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff-vs-3.11.0.md) |  |
| [2022-11-14](results/bm-20221114-3.12.0a2-3b9d793) | python | 3b9d793efc | 3.12.0a2 | 3b9d793 | [1.30x faster](results/bm-20221114-3.12.0a2-3b9d793/bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793-vs-3.10.4.md) | [1.04x faster](results/bm-20221114-3.12.0a2-3b9d793/bm-20221114-linux-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793-vs-3.11.0.md) |  |
| [2022-10-25](results/bm-20221025-3.12.0a1-4ae1a0e) | python | 4ae1a0ecaf | 3.12.0a1 | 4ae1a0e | [1.30x faster](results/bm-20221025-3.12.0a1-4ae1a0e/bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.10.4.md) | [1.03x faster](results/bm-20221025-3.12.0a1-4ae1a0e/bm-20221025-linux-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.25x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | 9d38120e33 | 3.10.4 | 9d38120 |  | [1.27x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md) |  |

## linux x86_64 (pythonperf2)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c |  | [1.03x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2023-03-06](results/bm-20230306-3.12.0a5%2B-f533f21) | python | f533f216e6 | 3.12.0a5+ | f533f21 |  | [1.03x faster](results/bm-20230306-3.12.0a5%2B-f533f21/bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.11.0.md) |  |
| [2023-02-26](results/bm-20230226-3.12.0a5%2B-f3cb15c) | python | f3cb15c88a | 3.12.0a5+ | f3cb15c |  | [1.03x faster](results/bm-20230226-3.12.0a5%2B-f3cb15c/bm-20230226-pythonperf2-x86_64-python-f3cb15c88afa2e87067d-3.12.0a5%2B-f3cb15c-vs-3.11.0.md) |  |
| [2023-03-07](results/bm-20230307-3.12.0a6-f9774e5) | python | f9774e57d8 | 3.12.0a6 | f9774e5 |  | [1.04x faster](results/bm-20230307-3.12.0a6-f9774e5/bm-20230307-pythonperf2-x86_64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5-vs-3.11.0.md) |  |
| [2023-02-07](results/bm-20230207-3.12.0a5-3c67ec3) | python | 3c67ec394f | 3.12.0a5 | 3c67ec3 |  | [1.04x faster](results/bm-20230207-3.12.0a5-3c67ec3/bm-20230207-pythonperf2-x86_64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.md) |  |
| [2023-01-10](results/bm-20230110-3.12.0a4-3d5d3f7) | python | 3d5d3f7af6 | 3.12.0a4 | 3d5d3f7 |  | [1.03x faster](results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-pythonperf2-x86_64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7-vs-3.11.0.md) |  |
| [2022-12-06](results/bm-20221206-3.12.0a3-b6bd7ff) | python | b6bd7ffcbc | 3.12.0a3 | b6bd7ff |  | [1.01x faster](results/bm-20221206-3.12.0a3-b6bd7ff/bm-20221206-pythonperf2-x86_64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff-vs-3.11.0.md) |  |
| [2022-11-14](results/bm-20221114-3.12.0a2-3b9d793) | python | 3b9d793efc | 3.12.0a2 | 3b9d793 |  | [1.03x faster](results/bm-20221114-3.12.0a2-3b9d793/bm-20221114-pythonperf2-x86_64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793-vs-3.11.0.md) |  |
| [2022-10-25](results/bm-20221025-3.12.0a1-4ae1a0e) | python | 4ae1a0ecaf | 3.12.0a1 | 4ae1a0e |  | [1.03x faster](results/bm-20221025-3.12.0a1-4ae1a0e/bm-20221025-pythonperf2-x86_64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 |  |  |  |

## windows amd64 (pythonperf1)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c | [1.21x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md) | [1.09x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2022-11-11](results/bm-20221111-3.12.0a1%2B-3dd6ee2) | python | 3dd6ee2c00 | 3.12.0a1+ | 3dd6ee2 | [1.16x faster](results/bm-20221111-3.12.0a1%2B-3dd6ee2/bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1%2B-3dd6ee2-vs-3.10.4.md) | [1.05x faster](results/bm-20221111-3.12.0a1%2B-3dd6ee2/bm-20221111-pythonperf1-amd64-python-3dd6ee2c0022cb49e5cb-3.12.0a1%2B-3dd6ee2-vs-3.11.0.md) |  |
| [2022-11-09](results/bm-20221109-3.12.0a1%2B-c03e05c) | python | c03e05c2e7 | 3.12.0a1+ | c03e05c | [1.09x faster](results/bm-20221109-3.12.0a1%2B-c03e05c/bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1%2B-c03e05c-vs-3.10.4.md) | [1.01x slower](results/bm-20221109-3.12.0a1%2B-c03e05c/bm-20221109-pythonperf1-amd64-python-c03e05c2e72f3ea5e797-3.12.0a1%2B-c03e05c-vs-3.11.0.md) |  |
| [2022-11-04](results/bm-20221104-3.12.0a1%2B-044bcc1) | python | 044bcc1771 | 3.12.0a1+ | 044bcc1 | [1.11x faster](results/bm-20221104-3.12.0a1%2B-044bcc1/bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1%2B-044bcc1-vs-3.10.4.md) | [1.00x slower](results/bm-20221104-3.12.0a1%2B-044bcc1/bm-20221104-pythonperf1-amd64-python-044bcc1771fe7e2f8eba-3.12.0a1%2B-044bcc1-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.11x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | 9d38120e33 | 3.10.4 | 9d38120 |  | [1.11x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md) |  |

## darwin arm64 (darwin)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c | [1.19x faster \*](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md) | [1.02x slower](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2023-03-18](results/bm-20230318-3.12.0a6%2B-3adb23a) | python | main | 3.12.0a6+ | 3adb23a | [1.20x faster \*](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.md) | [1.02x slower](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.md) |  |
| [2023-03-11](results/bm-20230311-3.12.0a6%2B-bb396ee) | python | main | 3.12.0a6+ | bb396ee | [1.19x faster \*](results/bm-20230311-3.12.0a6%2B-bb396ee/bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.10.4.md) | [1.02x slower](results/bm-20230311-3.12.0a6%2B-bb396ee/bm-20230311-darwin-arm64-python-main-3.12.0a6%2B-bb396ee-vs-3.11.0.md) |  |
| [2023-03-07](results/bm-20230307-3.12.0a6-f9774e5) | python | f9774e57d8 | 3.12.0a6 | f9774e5 | [1.19x faster \*](results/bm-20230307-3.12.0a6-f9774e5/bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5-vs-3.10.4.md) | [1.01x slower](results/bm-20230307-3.12.0a6-f9774e5/bm-20230307-darwin-arm64-python-f9774e57d84162ff0cba-3.12.0a6-f9774e5-vs-3.11.0.md) |  |
| [2023-02-07](results/bm-20230207-3.12.0a5-3c67ec3) | python | 3c67ec394f | 3.12.0a5 | 3c67ec3 | [1.21x faster \*](results/bm-20230207-3.12.0a5-3c67ec3/bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.10.4.md) | [1.01x faster](results/bm-20230207-3.12.0a5-3c67ec3/bm-20230207-darwin-arm64-python-3c67ec394faac79d2608-3.12.0a5-3c67ec3-vs-3.11.0.md) |  |
| [2023-01-10](results/bm-20230110-3.12.0a4-3d5d3f7) | python | 3d5d3f7af6 | 3.12.0a4 | 3d5d3f7 | [1.21x faster \*](results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7-vs-3.10.4.md) | [1.01x faster](results/bm-20230110-3.12.0a4-3d5d3f7/bm-20230110-darwin-arm64-python-3d5d3f7af6498effbc60-3.12.0a4-3d5d3f7-vs-3.11.0.md) |  |
| [2022-12-06](results/bm-20221206-3.12.0a3-b6bd7ff) | python | b6bd7ffcbc | 3.12.0a3 | b6bd7ff | [1.09x faster \*](results/bm-20221206-3.12.0a3-b6bd7ff/bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff-vs-3.10.4.md) | [1.10x slower](results/bm-20221206-3.12.0a3-b6bd7ff/bm-20221206-darwin-arm64-python-b6bd7ffcbc1ffaa68e34-3.12.0a3-b6bd7ff-vs-3.11.0.md) |  |
| [2022-11-14](results/bm-20221114-3.12.0a2-3b9d793) | python | 3b9d793efc | 3.12.0a2 | 3b9d793 | [1.17x faster \*](results/bm-20221114-3.12.0a2-3b9d793/bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793-vs-3.10.4.md) | [1.03x slower](results/bm-20221114-3.12.0a2-3b9d793/bm-20221114-darwin-arm64-python-3b9d793efcfd2c00c14f-3.12.0a2-3b9d793-vs-3.11.0.md) |  |
| [2022-10-25](results/bm-20221025-3.12.0a1-4ae1a0e) | python | 4ae1a0ecaf | 3.12.0a1 | 4ae1a0e | [1.18x faster \*](results/bm-20221025-3.12.0a1-4ae1a0e/bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.10.4.md) | [1.02x slower](results/bm-20221025-3.12.0a1-4ae1a0e/bm-20221025-darwin-arm64-python-4ae1a0ecaffe4320fe97-3.12.0a1-4ae1a0e-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.22x faster \*](results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.22x slower \*](results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |


<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
