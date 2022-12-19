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

pyperformance:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:12 UTC)](benchmark-results/cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-06 (22:23 UTC)](benchmark-results/cpython-3.11.0b3-eb0004c271-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b3 | eb0004c271 | fc_linux | 1.28x faster  |
|  [2022-11-20 (02:15 UTC)](benchmark-results/cpython-3.12.0a0-b0e1f9c241-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | b0e1f9c241 | fc_linux | 1.31x faster  |

pyston:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:16 UTC)](benchmark-results/cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyston.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-06 (22:26 UTC)](benchmark-results/cpython-3.11.0b3-eb0004c271-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b3 | eb0004c271 | fc_linux | 1.29x faster  |
|  [2022-11-20 (02:15 UTC)](benchmark-results/cpython-3.12.0a0-b0e1f9c241-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | b0e1f9c241 | fc_linux | 1.30x faster  |

<!-- END table -->

There is also a [complete list of published results](results/README.md) (and [legacy results](benchmark-results/README.md)).
