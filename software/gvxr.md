---
layout: page
title: gVirtualXray (gVXR)
permalink: software/gvxr/
---

[gVirtualXRay (gVXR)](https://gvirtualxray.sourceforge.io/) is a C++ library to simulate X-ray imaging. It is based on the Beer-Lambert law to compute the absorption of light (i.e. photons) by 3D objects (here polygon meshes). It is implemented on the graphics processing unit (GPU) using the OpenGL Shading Language (GLSL). 
It provides wrappers to Python, R, Ruby, Tcl, C#, Java, and GNU Octave. 

## Installation

gVXR is easily available via the Python Package Index (PyPI) for GNU/Linux and Windows for  X86-64 processors (i.e. AMD and Intel CPUs), but it can also be compiled on ARM-based processors (at least on GNU/Linux). It can be installed with the command:

```bash
pip install gvxr
```

## Usage

A simple example is given on [PyPI](https://pypi.org/project/gvxr/). Further examples are given on the project's [website](https://gvirtualxray.sourceforge.io/tutorials/).

## Benchmarks

The paper below provides a quantitative comparison of images created using gVXR to both Monte Carlo (MC) and real images of clinically realistic phantoms.

Pointon J.L., Wen T., Tugwell-Allsup J., Sújar A., Létang J.M., Vidal F.P.
Simulation of X-ray projections on GPU: Benchmarking gVirtualXray with clinically realistic phantoms
*Comput. Methods Programs Biomed.*, 234 (2023), Article 107500, [10.1016/j.cmpb.2023.107500](https://doi.org/10.1016/j.cmpb.2023.107500)
