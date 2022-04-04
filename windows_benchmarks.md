Running PyPerformance Benchmarks on Windows
===========================================

Background links:
- [PyPerformance docs](https://pyperformance.readthedocs.io/)
- [PyPerformance source](https://github.com/python/pyperformance)

Quick notes:
- Don't bother installing from PyPI, that version is out of date

Goals:
- Get reference benchmark numbers for CPython 3.10
- Get reliable benchmark numbers for CPython main (to become 3.11)
- Compare the two

Software to install:
- git (hopefully you have it installed already :-)
- CPython 3.10 from
  [python.org](https://www.python.org/ftp/python/3.10.4/python-3.10.4-amd64.exe)
  (I know there's a 3.10 on the Windows store,
  I don't know if it was built the same way;
  it might be worth comparing the two.)

Repos to clone:
- CPython: `git clone https://github.com/python/cpython`
- PyPerformance: `git clone https://github.com/python/pyperformance`
- Make sure you have the `main` branch for each repo

Silencing your machine:
- This should be done to *run* the benchmarks
- Close all apps except for a DOS box
- Do whatever else you can to shutdown background processes
  (Stop Windows Defender???)
- Enter airplane mode or disable networking
  once the first benchmark is running
  (I had to leave Bluetooth on since my mouse and keyboard are wireless)
- Note that on Linux, `pyperf system tune` will do a bunch
  of this; sadly this doesn't support Windows.

Getting 3.10 reference benchmark numbers
----------------------------------------

1. Check that you can run CPython 3.10 using the `py` runner
```
py -3.10 --version
```

2. Check that you have the latest version of `pip`
```
py -3.10 -m pip install -U pip setuptools
```

3. Install pyperformance from source
```
py -3.10 -m pip install ~\pyperformance\
```

4. Check that you can run one benchmark
```
py -3.10 -m pyperformance run --affinity 1 -b chaos
```
This should end by printing something like this:
```
.....................
chaos: Mean +- std dev: 121 ms +- 5 ms

Performance version: 1.0.4
Python version: 3.10.3 (64-bit) revision a342a49
Report on Windows-10-10.0.22000-SP0
Number of logical CPUs: 8
Start date: 2022-04-04 10:52:41.374884
End date: 2022-04-04 10:52:56.707208

### chaos ###
Mean +- std dev: 121 ms +- 5 ms
```
To be honest I have no idea if the `--affinity` flag has any effect.
Its argument is one or more CPU numbers (comma-separated).

5. Create the venv(s) for all benchmarks
```
py -3.10 -m pyperformance venv recreate
```
This will also seed the pip cache with all the downloads you need.

6. Run all benchmarks

Before starting this, silence the machine as much as you can
(see above).
This step will take 30-60 minutes.
```
py -3.10 -m pyperformance run --affinity 1 -o 310a.json
```
The `-o 310a.json` specifies the JSON file where the results are written.
The file must not already exist.

7. Repeat step 6 a few times with different JSON output files

This is so that we get some idea of how stable these numbers are.
Let's say we end up with files `310a.json`, `310b.json`, `310c.json`.

It might also be interesting to experiment with different values for `--affinity`.

8. Compare the 3.10 results to each other

To compare JSON files I prefer to use `pyperf`, not `pyperformance`.
```
py -m pyperf compare_to 310a.json 310b.json
```
This prints a geometric mean at the end.
Ideally that should be 1.00 faster/slower.
I suppose if we see 1.01 faster/slower that's acceptable too.
On my machine, alas, I see 1.06 faster, which I interpret as
the machine being too noisy to run decent benchmarks.

Try all three pairwise, or specify all JSON files together
(see [pyperf docs](https://pyperf.readthedocs.io/en/latest/analyze.html)
for more about this).

Getting 3.11 benchmark numbers
------------------------------

Here we have to build CPython first.

1. Build CPython in the cpython repo with PGO+LTO

This will take some time since the PGO training is running a subset
of the test suite.
```
cd ~\cpython
.\PCbuild\build.bat --pgo
```

2. Create an installable CPython tree
```
.\python.bat .\PC\layout\ --preset-default --copy installed
```
This creates a directory `installed` containing the `python.exe`
we want to use to run PyPerformance.

3. Ensure we have the latest pip for 3.11
```
.\installed\python.exe -m ensurepip
.\installed\python.exe -m pip install -U pip setuptools
```
If this fails, I've probably forgotten some steps.

4. Install pyperformance from source
```
.\installed\python.exe -m pip install ~\pyperformance\
```

5. Verify that one benchmark runs
```
.\installed\python.exe -m pyperformance run --affinity 1 -b chaos
```
Output should be similar as for 3.10.

6. Create the venv(s) for all benchmarks
```
.\installed\python.exe -m pyperformance venv recreate
```
This will also seed the pip cache with all the downloads you need
(which might be different than for 3.10 in some cases).

7. Run all benchmarks

Again, silence the machine as much as you can (see above).
```
.\installed\python.exe -m pyperformance run --affinity 1 -o 311a.json
```

8. Run a second time

Again, I'd like to have multiple results so a single fluke doesn't scare us
-- or to confirm that things really are as bad is they seem.
Compare them as shown above
(it doesn't matter which Python binary is used to do this part).

9. Compare 3.10 and 3.11 results

This should be something as simple as
```
py -3.10 -m pyperf compare_to 310a.json 311a.json
```
