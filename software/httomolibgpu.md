---
layout: page
title: HTTomoLibGPU
permalink: software/httomolibgpu/
---

HTTomoLibGPU is a library of data processing methods and reconstruction tools that are tailored for the GPU-efficient computations using [CuPy](https://cupy.dev/) API. Most of the methods were ported from the CPU implementations in [TomoPy](/tomopy/) and [Savu](/savu/).

The reconstruction part in HTTomoLibGPU relies on [ToMoBAR](/tomobar) package which wraps [ASTRA](/astra) toolbox modules for parallel-beam geometry. The reconstruction modules use CuPy to support
device-to-device operations.


## Installation

HTTomoLibGPU is easily available via conda for Linux, but will be changed to support all OS's. It can be installed with the command:

```bash
conda install -c httomo httomolibgpu
```


## Usage

It is worth checking some [tests](https://github.com/DiamondLightSource/httomolibgpu/tree/main/tests), but simply import the module in Python and run it. The API reference is to be added... 

## Benchmarks

To be added...
