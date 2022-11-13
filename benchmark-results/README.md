# A Collection of CPython Benchmark Results

The files in this directory are all results from running pyperformance.
Each filename indicates the conditions under which the benchmarks were
run:

    `<impl>-<version>-<commit>-<host>-<compat ID>.json`
    `<impl>-<version>-<commit>-<host>-<compat ID>-<suites>.json`

* `<impl>` - the name of the Python implementation
* `<release>` - the Python version (or "main")
* `<commit>` - the git commit hash of the Python build
* `<host>` - a name that identifies where the benchmarks ran (see hosts.json)
* `<compat ID>` - a unique string based on the metadata in the results file
* `<suites>` - identifies the benchmark suites used (if not just the default)

Examples:

* example: `cpython-main-ada6B4cf8d-linux-cc12888f9B4b.json`
* example: `cpython-3.11a5-838b51a079-linux-cc12888f9B4b.json`
* example: `cpython-3.10.2-3571d41577-linux-cc12888f9B4b.json`

Also see https://github.com/faster-cpython/tools/tree/main/scripts/add-benchmark-results.py.

# Benchmark results

<!-- START results table -->

pyperformance:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:12 UTC)](cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-07 (20:56 UTC)](cpython-3.11.0a3-2e91dba437-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a3 | 2e91dba437 | fc_linux | 1.19x faster  |
|  [2022-06-07 (21:36 UTC)](cpython-3.11.0a4-9471106fd5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a4 | 9471106fd5 | fc_linux | 1.21x faster  |
|  [2022-06-07 (22:16 UTC)](cpython-3.11.0a5-c4e4b91557-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a5 | c4e4b91557 | fc_linux | 1.21x faster  |
|  [2022-06-07 (22:56 UTC)](cpython-3.11.0a6-3ddfa55df4-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a6 | 3ddfa55df4 | fc_linux | 1.19x faster  |
|  [2022-06-07 (23:37 UTC)](cpython-3.11.0a7-2e49bd06c5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0a7 | 2e49bd06c5 | fc_linux | 1.23x faster  |
|  [2022-05-24 (20:23 UTC)](cpython-3.11.0b1-8d32a5c8c4-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b1 | 8d32a5c8c4 | fc_linux | 1.28x faster  |
|  [2022-05-31 (16:17 UTC)](cpython-3.11.0b2-72f00f420a-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b2 | 72f00f420a | fc_linux | 1.28x faster  |
|  [2022-06-06 (22:23 UTC)](cpython-3.11.0b3-eb0004c271-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.11.0b3 | eb0004c271 | fc_linux | 1.28x faster  |
|  [2022-06-12 (02:21 UTC)](cpython-3.12.0a0-733e15f170-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 733e15f170 | fc_linux | 1.29x faster  |
|  [2022-06-26 (02:22 UTC)](cpython-3.12.0a0-38612a05b5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 38612a05b5 | fc_linux | 1.31x faster  |
|  [2022-07-03 (02:21 UTC)](cpython-3.12.0a0-7db1d2eaf3-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 7db1d2eaf3 | fc_linux | 1.31x faster  |
|  [2022-07-10 (02:20 UTC)](cpython-3.12.0a0-264b3ddfd5-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | 264b3ddfd5 | fc_linux | 1.30x faster  |
|  [2022-07-17 (02:20 UTC)](cpython-3.12.0a0-c20186c397-fc_linux-b2cf916db80e-pyperformance.json) | cpython 3.12.0a0 | c20186c397 | fc_linux | 1.31x faster  |
|  [2022-08-07 (02:19 UTC)](cpython-3.12.0a0-330f1d5828-fc_linux-91a1d1ba98b7-pyperformance.json) | cpython 3.12.0a0 | 330f1d5828 | fc_linux | 1.31x faster  |
|  [2022-08-14 (02:19 UTC)](cpython-3.12.0a0-32ac98e899-fc_linux-91a1d1ba98b7-pyperformance.json) | cpython 3.12.0a0 | 32ac98e899 | fc_linux | 1.31x faster  |
|  [2022-10-02 (02:15 UTC)](cpython-3.12.0a0-8baef8ae36-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | 8baef8ae36 | fc_linux | 1.31x faster  |
|  [2022-10-09 (02:15 UTC)](cpython-3.12.0a0-2d2e01aa4c-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | 2d2e01aa4c | fc_linux | 1.30x faster  |
|  [2022-10-16 (02:15 UTC)](cpython-3.12.0a0-660f10248b-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | 660f10248b | fc_linux | 1.30x faster  |
|  [2022-10-19 (14:03 UTC)](cpython-3.12.0a0-50553004fe-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | 50553004fe | fc_linux | 1.30x faster  |
|  [2022-10-23 (02:15 UTC)](cpython-3.12.0a0-f58631be11-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | f58631be11 | fc_linux | 1.30x faster  |
|  [2022-10-30 (02:15 UTC)](cpython-3.12.0a0-fc94d55ff4-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | fc94d55ff4 | fc_linux | 1.30x faster  |
|  [2022-11-13 (02:16 UTC)](cpython-3.12.0a0-57be545959-fc_linux-4119a1d33a43-pyperformance.json) | cpython 3.12.0a0 | 57be545959 | fc_linux | 1.30x faster  |

pyston:

|  date | release | commit | host | mean  |
|  --- | --- | --- | --- | ---  |
|  [2022-06-07 (20:16 UTC)](cpython-3.10.4-9d38120e33-fc_linux-b2cf916db80e-pyston.json) | cpython 3.10.4 | 9d38120e33 | fc_linux | (ref)  |
|  [2022-06-07 (20:59 UTC)](cpython-3.11.0a3-2e91dba437-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a3 | 2e91dba437 | fc_linux | 1.21x faster  |
|  [2022-06-07 (21:39 UTC)](cpython-3.11.0a4-9471106fd5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a4 | 9471106fd5 | fc_linux | 1.24x faster  |
|  [2022-06-07 (22:19 UTC)](cpython-3.11.0a5-c4e4b91557-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a5 | c4e4b91557 | fc_linux | 1.22x faster  |
|  [2022-06-07 (22:59 UTC)](cpython-3.11.0a6-3ddfa55df4-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a6 | 3ddfa55df4 | fc_linux | 1.21x faster  |
|  [2022-06-07 (23:41 UTC)](cpython-3.11.0a7-2e49bd06c5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0a7 | 2e49bd06c5 | fc_linux | 1.21x faster  |
|  [2022-05-24 (20:26 UTC)](cpython-3.11.0b1-8d32a5c8c4-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b1 | 8d32a5c8c4 | fc_linux | 1.26x faster  |
|  [2022-05-31 (16:20 UTC)](cpython-3.11.0b2-72f00f420a-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b2 | 72f00f420a | fc_linux | 1.30x faster  |
|  [2022-06-06 (22:26 UTC)](cpython-3.11.0b3-eb0004c271-fc_linux-b2cf916db80e-pyston.json) | cpython 3.11.0b3 | eb0004c271 | fc_linux | 1.29x faster  |
|  [2022-06-12 (02:24 UTC)](cpython-3.12.0a0-733e15f170-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 733e15f170 | fc_linux | 1.31x faster  |
|  [2022-06-26 (02:25 UTC)](cpython-3.12.0a0-38612a05b5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 38612a05b5 | fc_linux | 1.33x faster  |
|  [2022-07-03 (02:24 UTC)](cpython-3.12.0a0-7db1d2eaf3-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 7db1d2eaf3 | fc_linux | 1.31x faster  |
|  [2022-07-10 (02:24 UTC)](cpython-3.12.0a0-264b3ddfd5-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | 264b3ddfd5 | fc_linux | 1.34x faster  |
|  [2022-07-17 (02:23 UTC)](cpython-3.12.0a0-c20186c397-fc_linux-b2cf916db80e-pyston.json) | cpython 3.12.0a0 | c20186c397 | fc_linux | 1.34x faster  |
|  [2022-08-07 (02:22 UTC)](cpython-3.12.0a0-330f1d5828-fc_linux-91a1d1ba98b7-pyston.json) | cpython 3.12.0a0 | 330f1d5828 | fc_linux | 1.33x faster  |
|  [2022-08-14 (02:22 UTC)](cpython-3.12.0a0-32ac98e899-fc_linux-91a1d1ba98b7-pyston.json) | cpython 3.12.0a0 | 32ac98e899 | fc_linux | 1.34x faster  |
|  [2022-10-02 (02:16 UTC)](cpython-3.12.0a0-8baef8ae36-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | 8baef8ae36 | fc_linux | 1.32x faster  |
|  [2022-10-09 (02:16 UTC)](cpython-3.12.0a0-2d2e01aa4c-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | 2d2e01aa4c | fc_linux | 1.31x faster  |
|  [2022-10-16 (02:16 UTC)](cpython-3.12.0a0-660f10248b-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | 660f10248b | fc_linux | 1.30x faster  |
|  [2022-10-19 (14:04 UTC)](cpython-3.12.0a0-50553004fe-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | 50553004fe | fc_linux | 1.31x faster  |
|  [2022-10-23 (02:16 UTC)](cpython-3.12.0a0-f58631be11-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | f58631be11 | fc_linux | 1.33x faster  |
|  [2022-10-30 (02:16 UTC)](cpython-3.12.0a0-fc94d55ff4-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | fc94d55ff4 | fc_linux | 1.32x faster  |
|  [2022-11-13 (02:16 UTC)](cpython-3.12.0a0-57be545959-fc_linux-4119a1d33a43-pyston.json) | cpython 3.12.0a0 | 57be545959 | fc_linux | 1.30x faster  |

<!-- END results table -->

