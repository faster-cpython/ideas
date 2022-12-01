This directory contains output from Python built using `--enable-pystats` and run over the pyperformance test suite.

Results are automatically added every Sunday at midnight UTC.

To manually generate a set of results you have write permissions to this repository, you can do one of the following:

- Visit [the pystats workflow](https://github.com/faster-cpython/ideas/actions/workflows/pystats.yml) and press the "Run workflow" button. You can manually select a different fork and branch of CPython to test.
- In a checkout of this repo, use the `gh` tool:

```bash
gh workflow run pystats.yml
```

To manually select a different fork and branch:

```bash
gh workflow run pystats.yml -f fork=mdboom -f branch=my-changes
```

Two sets of pystats output can be compared using the [`Tools/scripts/summarize_stats.py`](https://github.com/python/cpython/blob/main/Tools/scripts/summarize_stats.py) script:

```bash
Tools/scripts/summarize_stats.py pystats-python-abcdef1-2022-01-01.json pystats-python-fedc132-2022-01-03.json
```
