---
layout: page
title: TomocuPy
permalink: software/tomocupy/
---

TomocuPy is a Python package and a command-line interface for GPU reconstruction of tomographic/laminographic data in 16-bit and 32-bit precision. All preprocessing operations are implemented on GPU with using CuPy library, the backprojection operation is implemented with CUDA C.

## Installation

TomocuPy is available through conda-forge:

Add conda-forge to anaconda channels:

```bash
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Create environment with installed tomocupy

```bash
conda create -n tomocupy tomocupy
```

Activate tomocupy environment

```bash
conda activate tomocupy
```

Test installation

```bash
tomocupy recon -h
```


## Usage

Examples can be found at: <https://tomocupy.readthedocs.io/en/latest/usage.html>.


## Publication

Viktor Nikitin. TomocuPy – efficient GPU-based tomographic reconstruction with asynchronous data processing. Journal of Synchrotron Radiation, 30(1):, Jan 2023

<https://doi.org/10.1107/S1600577522010311>

## Benchmarks

To be added...
