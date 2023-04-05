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
| [2023-04-01](results/bm-20230401-3.12.0a6%2B-06249ec) | python | main | 3.12.0a6+ | 06249ec | [1.29x faster](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-linux-x86_64-python-main-3.12.0a6%2B-06249ec-vs-3.10.4.md) | [1.03x faster](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-linux-x86_64-python-main-3.12.0a6%2B-06249ec-vs-3.11.0.md) |  |
| [2023-03-26](results/bm-20230326-3.12.0a6%2B-2cdc518) | python | 2cdc5189a6 | 3.12.0a6+ | 2cdc518 | [1.30x faster](results/bm-20230326-3.12.0a6%2B-2cdc518/bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6%2B-2cdc518-vs-3.10.4.md) | [1.03x faster](results/bm-20230326-3.12.0a6%2B-2cdc518/bm-20230326-linux-x86_64-python-2cdc5189a6bc3157fddd-3.12.0a6%2B-2cdc518-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-662c16c) | faster-cpython | pep_669 | 3.12.0a6+ | 662c16c | [1.32x faster](results/bm-20230325-3.12.0a6%2B-662c16c/bm-20230325-linux-x86_64-faster%252dcpython-pep_669-3.12.0a6%2B-662c16c-vs-3.10.4.md) | [1.05x faster](results/bm-20230325-3.12.0a6%2B-662c16c/bm-20230325-linux-x86_64-faster%252dcpython-pep_669-3.12.0a6%2B-662c16c-vs-3.11.0.md) | [1.02x faster](results/bm-20230325-3.12.0a6%2B-662c16c/bm-20230325-linux-x86_64-faster%252dcpython-pep_669-3.12.0a6%2B-662c16c-vs-base.md) |
| [2022-11-10](results/bm-20221110-3.12.0a1%2B-2e343fc) | python | 2e343fc465 | 3.12.0a1+ | 2e343fc | [1.30x faster](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-linux-x86_64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.10.4.md) | [1.03x faster](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-linux-x86_64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.25x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | 9d38120e33 | 3.10.4 | 9d38120 |  | [1.27x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md) |  |

## linux x86_64 (pythonperf2)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-01](results/bm-20230401-3.12.0a6%2B-06249ec) | python | main | 3.12.0a6+ | 06249ec |  | [1.02x faster](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-pythonperf2-x86_64-python-main-3.12.0a6%2B-06249ec-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c |  | [1.03x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf2-x86_64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2023-03-06](results/bm-20230306-3.12.0a5%2B-f533f21) | python | f533f216e6 | 3.12.0a5+ | f533f21 |  | [1.03x faster](results/bm-20230306-3.12.0a5%2B-f533f21/bm-20230306-pythonperf2-x86_64-python-f533f216e6aaba3f3663-3.12.0a5%2B-f533f21-vs-3.11.0.md) |  |
| [2022-11-10](results/bm-20221110-3.12.0a1%2B-2e343fc) | python | 2e343fc465 | 3.12.0a1+ | 2e343fc |  | [1.03x faster](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-pythonperf2-x86_64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 |  |  |  |

## windows amd64 (pythonperf1)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-01](results/bm-20230401-3.12.0a6%2B-06249ec) | python | main | 3.12.0a6+ | 06249ec | [1.19x faster](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-pythonperf1-amd64-python-main-3.12.0a6%2B-06249ec-vs-3.10.4.md) | [1.07x faster](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-pythonperf1-amd64-python-main-3.12.0a6%2B-06249ec-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c | [1.21x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md) | [1.09x faster](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-pythonperf1-amd64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2023-01-29](results/bm-20230129-3.12.0a4%2B-c4170c3) | python | c4170c36b0 | 3.12.0a4+ | c4170c3 | [1.21x faster](results/bm-20230129-3.12.0a4%2B-c4170c3/bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3-vs-3.10.4.md) | [1.10x faster](results/bm-20230129-3.12.0a4%2B-c4170c3/bm-20230129-pythonperf1-amd64-python-c4170c36b0b54c10456f-3.12.0a4%2B-c4170c3-vs-3.11.0.md) |  |
| [2023-01-22](results/bm-20230122-3.12.0a4%2B-d717be0) | python | d717be04dc | 3.12.0a4+ | d717be0 | [1.21x faster](results/bm-20230122-3.12.0a4%2B-d717be0/bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4%2B-d717be0-vs-3.10.4.md) | [1.09x faster](results/bm-20230122-3.12.0a4%2B-d717be0/bm-20230122-pythonperf1-amd64-python-d717be04dc7876696cb2-3.12.0a4%2B-d717be0-vs-3.11.0.md) |  |
| [2023-01-16](results/bm-20230116-3.12.0a4%2B-7b14c2e) | python | 7b14c2ef19 | 3.12.0a4+ | 7b14c2e | [1.22x faster](results/bm-20230116-3.12.0a4%2B-7b14c2e/bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.10.4.md) | [1.10x faster](results/bm-20230116-3.12.0a4%2B-7b14c2e/bm-20230116-pythonperf1-amd64-python-7b14c2ef194b6eed7967-3.12.0a4%2B-7b14c2e-vs-3.11.0.md) |  |
| [2023-01-13](results/bm-20230113-3.12.0a4%2B-010576c) | python | 010576c6ea | 3.12.0a4+ | 010576c | [1.20x faster](results/bm-20230113-3.12.0a4%2B-010576c/bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4%2B-010576c-vs-3.10.4.md) | [1.09x faster](results/bm-20230113-3.12.0a4%2B-010576c/bm-20230113-pythonperf1-amd64-python-010576c6ea7e687cf2cb-3.12.0a4%2B-010576c-vs-3.11.0.md) |  |
| [2023-01-08](results/bm-20230108-3.12.0a3%2B-e47b139) | python | e47b13934b | 3.12.0a3+ | e47b139 | [1.21x faster](results/bm-20230108-3.12.0a3%2B-e47b139/bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.10.4.md) | [1.09x faster](results/bm-20230108-3.12.0a3%2B-e47b139/bm-20230108-pythonperf1-amd64-python-e47b13934b2eb50914e4-3.12.0a3%2B-e47b139-vs-3.11.0.md) |  |
| [2023-01-01](results/bm-20230101-3.12.0a3%2B-edfbf56) | python | edfbf56f4c | 3.12.0a3+ | edfbf56 | [1.17x faster](results/bm-20230101-3.12.0a3%2B-edfbf56/bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.10.4.md) | [1.06x faster](results/bm-20230101-3.12.0a3%2B-edfbf56/bm-20230101-pythonperf1-amd64-python-edfbf56f4ca6588dfd20-3.12.0a3%2B-edfbf56-vs-3.11.0.md) |  |
| [2022-12-26](results/bm-20221226-3.12.0a3%2B-ad3c99e) | python | ad3c99e521 | 3.12.0a3+ | ad3c99e | [1.16x faster](results/bm-20221226-3.12.0a3%2B-ad3c99e/bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e-vs-3.10.4.md) | [1.05x faster](results/bm-20221226-3.12.0a3%2B-ad3c99e/bm-20221226-pythonperf1-amd64-python-ad3c99e521151680afc6-3.12.0a3%2B-ad3c99e-vs-3.11.0.md) |  |
| [2022-12-19](results/bm-20221219-3.12.0a3%2B-702a5bc) | python | 702a5bc463 | 3.12.0a3+ | 702a5bc | [1.17x faster](results/bm-20221219-3.12.0a3%2B-702a5bc/bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3%2B-702a5bc-vs-3.10.4.md) | [1.06x faster](results/bm-20221219-3.12.0a3%2B-702a5bc/bm-20221219-pythonperf1-amd64-python-702a5bc4637c82dc011e-3.12.0a3%2B-702a5bc-vs-3.11.0.md) |  |
| [2022-12-11](results/bm-20221211-3.12.0a3%2B-70be5e4) | python | 70be5e42f6 | 3.12.0a3+ | 70be5e4 | [1.17x faster](results/bm-20221211-3.12.0a3%2B-70be5e4/bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3%2B-70be5e4-vs-3.10.4.md) | [1.06x faster](results/bm-20221211-3.12.0a3%2B-70be5e4/bm-20221211-pythonperf1-amd64-python-70be5e42f6e288de32e0-3.12.0a3%2B-70be5e4-vs-3.11.0.md) |  |
| [2022-12-05](results/bm-20221205-3.12.0a2%2B-e3a3863) | python | e3a3863cb9 | 3.12.0a2+ | e3a3863 | [1.19x faster](results/bm-20221205-3.12.0a2%2B-e3a3863/bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.10.4.md) | [1.07x faster](results/bm-20221205-3.12.0a2%2B-e3a3863/bm-20221205-pythonperf1-amd64-python-e3a3863cb9561705d3dd-3.12.0a2%2B-e3a3863-vs-3.11.0.md) |  |
| [2022-11-28](results/bm-20221128-3.12.0a2%2B-594de16) | python | 594de165bf | 3.12.0a2+ | 594de16 | [1.21x faster](results/bm-20221128-3.12.0a2%2B-594de16/bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2%2B-594de16-vs-3.10.4.md) | [1.09x faster](results/bm-20221128-3.12.0a2%2B-594de16/bm-20221128-pythonperf1-amd64-python-594de165bf2f21d6b28e-3.12.0a2%2B-594de16-vs-3.11.0.md) |  |
| [2022-11-21](results/bm-20221121-3.12.0a2%2B-cdde29d) | python | cdde29dde9 | 3.12.0a2+ | cdde29d | [1.19x faster](results/bm-20221121-3.12.0a2%2B-cdde29d/bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.10.4.md) | [1.08x faster](results/bm-20221121-3.12.0a2%2B-cdde29d/bm-20221121-pythonperf1-amd64-python-cdde29dde90947df9bac-3.12.0a2%2B-cdde29d-vs-3.11.0.md) |  |
| [2022-11-12](results/bm-20221112-3.12.0a1%2B-99972dc) | python | 99972dc745 | 3.12.0a1+ | 99972dc | [1.16x faster](results/bm-20221112-3.12.0a1%2B-99972dc/bm-20221112-pythonperf1-amd64-python-99972dc7450f1266e392-3.12.0a1%2B-99972dc-vs-3.10.4.md) | [1.05x faster](results/bm-20221112-3.12.0a1%2B-99972dc/bm-20221112-pythonperf1-amd64-python-99972dc7450f1266e392-3.12.0a1%2B-99972dc-vs-3.11.0.md) |  |
| [2022-11-10](results/bm-20221110-3.12.0a1%2B-6dedf42) | python | 6dedf42527 | 3.12.0a1+ | 6dedf42 | [1.16x faster](results/bm-20221110-3.12.0a1%2B-6dedf42/bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1%2B-6dedf42-vs-3.10.4.md) | [1.05x faster](results/bm-20221110-3.12.0a1%2B-6dedf42/bm-20221110-pythonperf1-amd64-python-6dedf42527fddbed8ef6-3.12.0a1%2B-6dedf42-vs-3.11.0.md) |  |
| [2022-11-10](results/bm-20221110-3.12.0a1%2B-2e343fc) | python | 2e343fc465 | 3.12.0a1+ | 2e343fc | [1.15x faster](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.10.4.md) | [1.04x faster](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-pythonperf1-amd64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.11.0.md) |  |
| [2022-11-09](results/bm-20221109-3.12.0a1%2B-87f5180) | python | 87f5180cd7 | 3.12.0a1+ | 87f5180 | [1.14x faster](results/bm-20221109-3.12.0a1%2B-87f5180/bm-20221109-pythonperf1-amd64-python-87f5180cd79617223ac5-3.12.0a1%2B-87f5180-vs-3.10.4.md) | [1.03x faster](results/bm-20221109-3.12.0a1%2B-87f5180/bm-20221109-pythonperf1-amd64-python-87f5180cd79617223ac5-3.12.0a1%2B-87f5180-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.11x faster](results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | 9d38120e33 | 3.10.4 | 9d38120 |  | [1.11x slower](results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-9d38120e335357a3b294-3.10.4-9d38120-vs-3.11.0.md) |  |

## darwin arm64 (darwin)
| date | fork | ref | version | hash | vs. 3.10.4: | vs. 3.11.0: | vs. base: |
| --- | --- | --- | --- | --- | ---: | ---: | ---: |
| [2023-04-01](results/bm-20230401-3.12.0a6%2B-06249ec) | python | main | 3.12.0a6+ | 06249ec | [1.19x faster \*](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-darwin-arm64-python-main-3.12.0a6%2B-06249ec-vs-3.10.4.md) | [1.01x slower](results/bm-20230401-3.12.0a6%2B-06249ec/bm-20230401-darwin-arm64-python-main-3.12.0a6%2B-06249ec-vs-3.11.0.md) |  |
| [2023-03-25](results/bm-20230325-3.12.0a6%2B-30a306c) | python | main | 3.12.0a6+ | 30a306c | [1.19x faster \*](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.10.4.md) | [1.02x slower](results/bm-20230325-3.12.0a6%2B-30a306c/bm-20230325-darwin-arm64-python-main-3.12.0a6%2B-30a306c-vs-3.11.0.md) |  |
| [2023-03-18](results/bm-20230318-3.12.0a6%2B-3adb23a) | python | main | 3.12.0a6+ | 3adb23a | [1.20x faster \*](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.10.4.md) | [1.02x slower](results/bm-20230318-3.12.0a6%2B-3adb23a/bm-20230318-darwin-arm64-python-main-3.12.0a6%2B-3adb23a-vs-3.11.0.md) |  |
| [2022-11-10](results/bm-20221110-3.12.0a1%2B-2e343fc) | python | 2e343fc465 | 3.12.0a1+ | 2e343fc | [1.19x faster \*](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-darwin-arm64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.10.4.md) | [1.01x slower](results/bm-20221110-3.12.0a1%2B-2e343fc/bm-20221110-darwin-arm64-python-2e343fc465ed0206340c-3.12.0a1%2B-2e343fc-vs-3.11.0.md) |  |
| [2022-10-24](results/bm-20221024-3.11.0-deaf509) | python | deaf509e8f | 3.11.0 | deaf509 | [1.22x faster \*](results/bm-20221024-3.11.0-deaf509/bm-20221024-darwin-arm64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509-vs-3.10.4.md) |  |  |
| [2022-03-23](results/bm-20220323-3.10.4-9d38120) | python | v3.10.4 | 3.10.4 | 9d38120 |  | [1.22x slower \*](results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120-vs-3.11.0.md) |  |


<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
