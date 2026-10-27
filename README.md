# DATA71011 Lab 1 — Binder notebook

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/marksoda/python-intermediate-inflammation/HEAD?urlpath=%2Fdoc%2Ftree%2Finflammation_lab1.ipynb)

This fork adds a reproducible notebook and pinned Binder configuration for the Week 5 workshop.
Open the badge and use Run → Restart Kernel and Run All Cells.

## Files added for the workshop
- `requirements.txt`: NumPy 1.25.0 and Matplotlib 3.10.9 (versions observed in the working Binder environment).
- `runtime.txt`: Python 3.10. The tested Binder kernel reported Python 3.10.19.
- `inflammation_lab1.ipynb`: reuses the original `inflammation.models` and `inflammation.views` functions on `data/small-01.csv` and `data/inflammation-01.csv`.

## Command-line exercise
Open File → New Launcher → Terminal and run:
```bash
python inflammation-analysis.py
python inflammation-analysis.py data/small-01.csv
```
The first command requires the `infiles` positional argument. The second supplies it.
In a server container there is no local desktop window for `plt.show()`; the notebook displays the graphs inline.

The original `pyproject.toml` specifies Python >=3.9 and a setuptools build but omits runtime dependencies. The added requirements file captures the NumPy and Matplotlib imports without changing the original scientific functions.

## Validation
The notebook was executed in Binder: all six code cells completed without errors. The small dataset has shape (2, 3); the larger dataset has shape (60, 40). Daily summary checks passed.
Prepared with AI assistance; review and understand the changes for the workshop.

---
## Original upstream README (retained)

# Introduction

This is a template software project repository used by the [Intermediate Research Software Development Skills In Python](https://github.com/carpentries-incubator/python-intermediate-development).

## Purpose

This repository is intended to be used as an example software project which is copied by learners of the 
[Intermediate Research Software Development Skills In Python](https://github.com/carpentries-incubator/python-intermediate-development) course.

This software project is not finished, does not contain a LICENCE file, the code is currently failing to run and contains some code style issues. 
It is used as a starting point for the course - issues will be fixed and code will be added in a number of places during the course by learners in their own copies of the repository, as course topics are introduced.

## Tests

Several tests have been implemented already, some of which are currently failing.
These failing tests set out the requirements for the additional code to be implemented during the workshop.

The tests should be run using `pytest`, which will be introduced during the workshop.
