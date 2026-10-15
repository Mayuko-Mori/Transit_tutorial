# Transit Photometry Tutorials

This repository contains Jupyter notebooks accompanying **Chapter 3:
Transit Photometry**. The tutorials provide practical examples of
transit light-curve analysis using Python.

Full bibliographic information for the chapter will be added here.

## Tutorials

### Tutorial 1: Transit analysis with a simple baseline model

**Chapter section: 3.4.1**

[Open Tutorial 1](Tutorial_1_single_transit_TOI519.ipynb)

This tutorial demonstrates the analysis of a single transit of
TOI-519 b using a simple baseline model.

### Tutorial 2: TESS data retrieval and multiple-transit analysis with a Gaussian process

**Chapter section: 3.4.2**

This tutorial demonstrates how to retrieve TESS light curves and
analyze multiple transits of π Men c while modeling baseline
variations with a Gaussian process (GP).

Two implementations are provided:

- [Tutorial 2 using celerite](Tutorial_2_TESS_transit_GP_PiMen-celerite.ipynb)
- [Tutorial 2 using celerite2](Tutorial_2_TESS_transit_GP_PiMen-celerite2.ipynb)

These are alternative versions of Tutorial 2; it is not necessary
to run both.

## Environment

The reference environment uses **Python 3.11.17 on Linux (x86_64)**.

The main packages include NumPy, pandas, Matplotlib, SciPy,
Astropy, LDTk, batman, emcee, corner, Lightkurve, celerite,
and celerite2.

- `requirements.txt` records package versions, including dependencies,
  for recreating the reference Python environment.
- [Package version information.ipynb](Package%20version%20information.ipynb)
  displays the Python version and versions of the main packages.

Pinned versions help reproduce the software environment, but
installation compatibility can differ across operating systems
and CPU architectures.

## Installation

The following instructions use conda, available through Miniconda
or Anaconda. Run these commands in a terminal.

### 1. Download the repository

```bash
git clone https://github.com/Mayuko-Mori/Transit_tutorial.git
cd Transit_tutorial
```

Alternatively, download and extract the repository using
**Code → Download ZIP**, then open a terminal in the extracted folder.

### 2. Create an environment

```bash
conda create -n transit-textbook python=3.11.17 pip
conda activate transit-textbook
```

### 3. Install the packages

```bash
python -m pip install -r requirements.txt
python -m pip check
```

The `-r requirements.txt` option tells pip to install the packages
and versions listed in that file.

### 4. Register the Jupyter kernel

```bash
python -m ipykernel install --user \
    --name transit-textbook \
    --display-name "Python (transit-textbook)"
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open a tutorial and select the **Python (transit-textbook)** kernel.

To check which Python environment the notebook is using, run:

```python
import sys
print(sys.executable)
```

The path should point to the `transit-textbook` environment.

## Running the tutorials

Start with Tutorial 1, then proceed to either version of Tutorial 2.
Run the cells in order from the beginning, preferably after
restarting the kernel.

Keep the repository's directory structure unchanged so that
relative paths to files continue to work.

An internet connection is required for downloading TESS data in
Tutorial 2 and any stellar-atmosphere data requested by LDTk.
These external datasets are not included in `requirements.txt`.

MCMC sampling can take time, and results may vary slightly between
runs because of stochastic sampling.

## Reference

Full reference information for **Chapter 3: Transit Photometry**
will be added here.
