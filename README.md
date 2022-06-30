# Faster CPython Ideas

Discussion and work tracker for Faster CPython project.

New ideas and discussions of existing ideas should be done in the [discussions](https://github.com/faster-cpython/ideas/discussions) section.

Please reserve [issues](https://github.com/faster-cpython/ideas/issues) for actual work-in-progress. 

Some links to presentations and other preliminary documentation:

- [Guido's slides at the 2021 Python Language Summit](FasterCPythonDark.pdf)
- [Mark's slides explaining Tiers of Execution](https://docs.google.com/presentation/d/1_cvQUwO2WWsaySyCmIy9nj9by4JKnkbiPCqtluLP3Mg)
- [PEP 659](https://peps.python.org/pep-0659/)

<!-- START results table -->

pyperformance:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:12 UTC)](benchmark-results/cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-07 (20:56 UTC)](benchmark-results/cpython-3.11.0a3-2e91dba437-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a3 | 2e91dba437 | fc_linux | 1.19x faster  |
|  [2022-06-07 (21:36 UTC)](benchmark-results/cpython-3.11.0a4-9471106fd5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a4 | 9471106fd5 | fc_linux | 1.21x faster  |

pyston:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:12 UTC)](benchmark-results/cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyston.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-07 (20:56 UTC)](benchmark-results/cpython-3.11.0a3-2e91dba437-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a3 | 2e91dba437 | fc_linux | 1.19x faster  |
|  [2022-06-07 (21:36 UTC)](benchmark-results/cpython-3.11.0a4-9471106fd5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a4 | 9471106fd5 | fc_linux | 1.21x faster  |

<!-- END results table -->
