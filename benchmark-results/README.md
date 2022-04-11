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
