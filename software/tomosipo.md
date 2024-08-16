---
layout: page
title: Tomosipo
permalink: software/tomosipo/
---

Tomosipo is a pythonic wrapper for the ASTRA-toolbox of high-performance GPU primitives for 3D tomography.


## Installation

A minimal installation requires:

```
python >= 3.6
ASTRA-toolbox >= 2.0
CUDA
```

The requirements can be installed using the anaconda package manager. The following snippet creates a new conda environment named tomosipo (replace X.X by your CUDA version)

```
conda create -n tomosipo cudatoolkit=<X.X> tomosipo -c astra-toolbox -c aahendriksen -c defaults
```

## Usage

see [github](https://github.com/ahendriksen/tomosipo?tab=readme-ov-file#usage)

## Benchmarks

To be added...
