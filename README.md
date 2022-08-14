# Faster CPython Ideas

Discussion and work tracker for Faster CPython project.

New ideas should be created as new [issues](https://github.com/faster-cpython/ideas/issues/new/choose).  It is ok if the idea is not fully formed -- we treat them as discussions to arrive at something actionable.  (We had previously used discussions for this, but that is now deprecated).

The [CPython issue tracker](https://github.com/python/cpython/issues) should be used for actual work-in-progress. 

Some links to presentations and other preliminary documentation:

- [Guido's slides at the 2021 Python Language Summit](FasterCPythonDark.pdf)
- [Mark's slides explaining Tiers of Execution](https://docs.google.com/presentation/d/1_cvQUwO2WWsaySyCmIy9nj9by4JKnkbiPCqtluLP3Mg)
- [PEP 659](https://peps.python.org/pep-0659/)

## Published Results

<!-- START results table -->

pyperformance:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:12 UTC)](benchmark-results/cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-07 (20:56 UTC)](benchmark-results/cpython-3.11.0a3-2e91dba437-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a3 | 2e91dba437 | fc_linux | 1.19x faster  |
|  [2022-06-07 (21:36 UTC)](benchmark-results/cpython-3.11.0a4-9471106fd5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a4 | 9471106fd5 | fc_linux | 1.21x faster  |
|  [2022-06-07 (22:16 UTC)](benchmark-results/cpython-3.11.0a5-c4e4b91557-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a5 | c4e4b91557 | fc_linux | 1.21x faster  |
|  [2022-06-07 (22:56 UTC)](benchmark-results/cpython-3.11.0a6-3ddfa55df4-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a6 | 3ddfa55df4 | fc_linux | 1.19x faster  |
|  [2022-06-07 (23:37 UTC)](benchmark-results/cpython-3.11.0a7-2e49bd06c5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a7 | 2e49bd06c5 | fc_linux | 1.23x faster  |
|  [2022-05-24 (20:23 UTC)](benchmark-results/cpython-3.11.0b1-8d32a5c8c4-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b1 | 8d32a5c8c4 | fc_linux | 1.28x faster  |
|  [2022-05-31 (16:17 UTC)](benchmark-results/cpython-3.11.0b2-72f00f420a-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b2 | 72f00f420a | fc_linux | 1.28x faster  |
|  [2022-06-06 (22:23 UTC)](benchmark-results/cpython-3.11.0b3-eb0004c271-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b3 | eb0004c271 | fc_linux | 1.29x faster  |
|  [2022-08-07 (02:19 UTC)](benchmark-results/cpython-3.12.0a0-330f1d5828-fc_linux-91a1d1ba98b7-pyperformance.json) | cpython 3.12.0a0 | 330f1d5828 | fc_linux | 1.31x faster  |
|  [2022-08-14 (02:19 UTC)](benchmark-results/cpython-3.12.0a0-32ac98e899-fc_linux-91a1d1ba98b7-pyperformance.json) | cpython 3.12.0a0 | 32ac98e899 | fc_linux | 1.31x faster  |
|  [2022-06-12 (02:21 UTC)](benchmark-results/cpython-3.12.0a0-733e15f170-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 733e15f170 | fc_linux | 1.30x faster  |
|  [2022-06-26 (02:22 UTC)](benchmark-results/cpython-3.12.0a0-38612a05b5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 38612a05b5 | fc_linux | 1.31x faster  |
|  [2022-07-03 (02:21 UTC)](benchmark-results/cpython-3.12.0a0-7db1d2eaf3-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 7db1d2eaf3 | fc_linux | 1.31x faster  |
|  [2022-07-10 (02:20 UTC)](benchmark-results/cpython-3.12.0a0-264b3ddfd5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 264b3ddfd5 | fc_linux | 1.30x faster  |
|  [2022-07-17 (02:20 UTC)](benchmark-results/cpython-3.12.0a0-c20186c397-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | c20186c397 | fc_linux | 1.31x faster  |

pyston:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:12 UTC)](benchmark-results/cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyston.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-07 (20:56 UTC)](benchmark-results/cpython-3.11.0a3-2e91dba437-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a3 | 2e91dba437 | fc_linux | 1.19x faster  |
|  [2022-06-07 (21:36 UTC)](benchmark-results/cpython-3.11.0a4-9471106fd5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a4 | 9471106fd5 | fc_linux | 1.21x faster  |
|  [2022-06-07 (22:16 UTC)](benchmark-results/cpython-3.11.0a5-c4e4b91557-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a5 | c4e4b91557 | fc_linux | 1.21x faster  |
|  [2022-06-07 (22:56 UTC)](benchmark-results/cpython-3.11.0a6-3ddfa55df4-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a6 | 3ddfa55df4 | fc_linux | 1.19x faster  |
|  [2022-06-07 (23:37 UTC)](benchmark-results/cpython-3.11.0a7-2e49bd06c5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a7 | 2e49bd06c5 | fc_linux | 1.23x faster  |
|  [2022-05-24 (20:23 UTC)](benchmark-results/cpython-3.11.0b1-8d32a5c8c4-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b1 | 8d32a5c8c4 | fc_linux | 1.28x faster  |
|  [2022-05-31 (16:17 UTC)](benchmark-results/cpython-3.11.0b2-72f00f420a-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b2 | 72f00f420a | fc_linux | 1.28x faster  |
|  [2022-06-06 (22:23 UTC)](benchmark-results/cpython-3.11.0b3-eb0004c271-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b3 | eb0004c271 | fc_linux | 1.29x faster  |
|  [2022-08-07 (02:19 UTC)](benchmark-results/cpython-3.12.0a0-330f1d5828-fc_linux-91a1d1ba98b7-pyston.json) | cpython 3.12.0a0 | 330f1d5828 | fc_linux | 1.31x faster  |
|  [2022-08-14 (02:19 UTC)](benchmark-results/cpython-3.12.0a0-32ac98e899-fc_linux-91a1d1ba98b7-pyston.json) | cpython 3.12.0a0 | 32ac98e899 | fc_linux | 1.31x faster  |
|  [2022-06-12 (02:21 UTC)](benchmark-results/cpython-3.12.0a0-733e15f170-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 733e15f170 | fc_linux | 1.30x faster  |
|  [2022-06-26 (02:22 UTC)](benchmark-results/cpython-3.12.0a0-38612a05b5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 38612a05b5 | fc_linux | 1.31x faster  |
|  [2022-07-03 (02:21 UTC)](benchmark-results/cpython-3.12.0a0-7db1d2eaf3-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 7db1d2eaf3 | fc_linux | 1.31x faster  |
|  [2022-07-10 (02:20 UTC)](benchmark-results/cpython-3.12.0a0-264b3ddfd5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 264b3ddfd5 | fc_linux | 1.30x faster  |
|  [2022-07-17 (02:20 UTC)](benchmark-results/cpython-3.12.0a0-c20186c397-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | c20186c397 | fc_linux | 1.31x faster  |

<!-- END results table -->
