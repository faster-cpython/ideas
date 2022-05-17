# Faster CPython benchmarking automation infrastructure

This is a requirements gathering brainstorm exercise for the benchmarking infrastructure for the Faster CPython project.

## Goals

To make anyone contributing to make CPython faster more efficient and effective by automating away some of the tedious or error-prone tasks related to benchmarking.

Visualization of the results should be designed to understand the nuance of specific performance improvements.

Growing and improving the benchmark suite is going to be important over time.
There should be an easy way to regenerate baselines as the suite is evolved so that existing results are not invalidated.

The wider Python community should be able to easily track the progress of CPython performance.

## Guardrail Requirements

Ensure that this infrastructure is a community resource: the results are visible by everyone, and usable and maintainable by anyone with a demonstrated interest, regardless of their employment status.

All parts of the system should be replicatable locally at the command line, and not require any complicated setup.

## Out of scope

We aren't aiming to support an "implementation shootout", e.g. between PyPy, Pyston and CPython.
The pyperformance benchmark suite will continue to be designed for this, but the rest of the tooling described here may not necessarily support it.

## Block diagram

The following is a block diagram of the proposed system.

While this is not intended as a description of current functionality, existing tools that provide some of this functionality are noted.
Importantly, there isn't currently a connection between the benchmark runner and `speed.python.org` -- these are currently distinct efforts.

![Block diagram](/benchmark-automation/Benchmark Infrastructure Block Diagram.png)

## Definitions

### Results

"Results", all of which come from running `pyperformance` in the same configuration, come in the following flavors:

- **Nightly**: Run once a day on the current `main` branch of CPython.
- **Tag**: Run on tagged releases of Python. The most recent tag for all feature branches and all alphas from the current `main` cycle.
- **Manual**: Run on a specific commit or pull request of CPython. Usually created in response to Github automation or using a CLI tool.

## Requirements

### Requesting a manual benchmark run at the commandline

Using a commandline tool available on PyPI, a developer could request a benchmark run on a specific commit in their published fork of CPython.
The results would be uploaded to the results database and viewable on the public website, with an option to download the complete raw data.

For example:

```
$ run_benchmark myname/cpython@135abf
Results will be available at https://example.com/pyspeed/myname/135abf
```

For security and scaling reasons, users would need to be granted explicit permission to do this. There may be a way to piggy back on Github authentication (which would let permitted users be managed there), but TBD whether this is possible.

### Requesting a manual benchmark in a pull request

When a contributor submits a pull request where a performance impact is expected, a developer with sufficient permissions could request a benchmark run.
This could be done with, for example, optional Github Actions or a bot that monitors pull requests.

### Benchmark suite evolution

We expect the benchmark suite to evolve rapidly in the near future as we add more real-world workloads to it.
When a new release of `pyperformance` ships, the following will happen automatically:

- Rerun all **Tag** results.
- Rerun the last two weeks of **Nightly** results.
- **Manual** results will be invalidated, and will need to be re-requested against the new benchmark suite.

To avoid problems, the front-end analysis tools will be designed to never allow comparing results from two different releases of `pyperformance`.

The limiting factor of this approach will be how long it takes to run the benchmark suite.  It currently takes 20 minutes (on my machine), and assuming around 10 **Tag** results and 14 **Nightly** results, it would take approximately 8 hours.  Even assuming the benchmark runs increase significantly, this could be completed over a weekend when **Manual** requests are less likely.

### Detecting unintentional performance changes

While the previous two requirements are about measuring intentional performance changes, it would also be useful to detect unintentional performance changes.
The **Nightly** results feed into a dashboard showing performance changes over time.
This dashboard would be viewed at a weekly meeting, and when regressions are discovered, bugs filed to investigate.
The dashboard would provide a range of commits that could be bisected to find the exact point of regression.

### Show statistical ambiguity in the data

Some benchmark runs have significant variability, which makes it harder to be certain of an improvement.  Using `box` or `violin` plots, which show a distribution of multiple samples, would be an improvement over using only the mean (current behavior of codespeed).

For example:

![Demo visualization](/benchmark-automation/demo.png)

There is an [interactive prototype](https://droettboom.com/speed-prototype) of this visualization.

While web-based visualizations are the best way to publish the results, they should also be usable from the commandline so developers doing one off benchmark runs on their own hardware have access to the same visualizations as those using the benchmark running machine.

### Aggregate benchmarks appropriately

We currently use the geometric mean of the percentage improvement across all benchmarks as the "range" of improvements to report in the [release highlights](https://docs.python.org/3.11/whatsnew/3.11.html#summary-release-highlights), e.g. "10-60% faster".

This is imperfect in a few ways:

- Not all benchmarks are good examples of "real life workloads". Those that aren't are still useful for development, but maybe not to make up the aggregate.  We should tag the benchmarks that feed into the aggregate and use only those by default in the visualization.

- We should produce full data sets and visualizations so developers can decide for themselves which benchmarks most apply to their workloads.

### Track non-runtime data points
 
It would be useful to also track non-runtime data points from the benchmarks, such as:

- max_rss (already collected by pyperformance)
- memory usage of various important object types (e.g. from memray)
- cache misses and other telemetry obtainable from the CPU
- `--enable-pystats` statistics

This implies running the benchmark suite multiple times. For some, the cost of measurement may invalidate the timings. For others, special, non-optimized, builds would be required.

### Increase platform support

We currently have a single benchmark-running machine running Linux.

It might be useful to measure on different OSes (Windows, Mac) and architectures (aarch64).

